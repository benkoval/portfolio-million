<template>
<div class='nav-container'>
    <nav
    class='nav-bar'>
        <ul
        class='ul-nav'>
            <li class='li-nav a'><a href='#about'>About</a></li>
            <li class='li-nav b'><a href='#resume'>Skills</a></li>
            <li class='li-nav c'><a href='#projects'
            @click='emitGlobalClickEvent()'>Projects</a></li>
        </ul>
    </nav>
</div>
</template>

<script>
import { EventBus } from './event-bus.js';

export default {
    name: 'Nav',
    data: () => {
        return {
            clicked: false
        }
    },
    methods: {
      emitGlobalClickEvent() {
        this.clicked = true,
        EventBus.$emit('i-got-clicked', this.clicked);
    }
  }
}
</script>