<template>
<div class='nav-container'>
    <nav
    class='nav-bar'>
        <ul
        class='ul-nav'>
            <li class='li-nav a'><a href='#'>About</a></li>
            <li class='li-nav b'><a href='#'>Skills</a></li>
            <li class='li-nav c'><a href='#'>Projects</a></li>
            <li class='li-nav d'>LinkedIn</li>
            <li class='li-nav e'>GitHub</li>
            <li class='li-nav a'>Email</li>
        </ul>
    </nav>
</div>
</template>

<style lang='scss'>

$lato: 'Lato', sans-serif;

$colors: (
  a: #D65394,
  b: #7C59AF,
  c: #3A5BAC,
  d: #FF6F61,
  e: #D65394
);

.nav-container {
    width: 100vw;
    height: 100vh;
    position: absolute;
}

.nav-bar {
    margin: auto;
    position: fixed;
    width: 100vw;
    // height: 4vw;
    background-color: #fff;
}

.ul-nav {
    display: flex;
    // justify-content: space-around;
    align-items: center;
    list-style-type: none;
    width: inherit;
}

.li-nav {
    margin: auto;
    font-family: $lato;
    transition: 0.25s;
    color: var(--color);
    font-size: 1.2vw;
    text-transform: lowercase;
    &:after {
        content: '';
        margin: 0 auto;
        display: block;
        width: 25%;
        border-bottom: .11vw solid;
        padding-bottom: .5rem;
    }
}

.a:hover,
.b:hover,
.a:focus-within,
.b:focus-within,
.c:hover,
.c:focus-within,
.d:hover,
.d:focus-within,
.e:hover,
.e:focus-within {
    transform: translateY(-0.2em);
    // border-color: var(--hover);
    // color: var(--hover);
}

@each $li, $color in $colors {
    .#{$li} {
      --color: #{$color};
    }
}

</style>