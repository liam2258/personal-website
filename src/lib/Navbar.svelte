<script lang="ts">
    let menuOpen = $state(false);

    function toggleMenu() {
        menuOpen = !menuOpen
    }
</script>

<nav class="desktop-nav">
    <a href="/">Home</a>
    <a href="/">Projects</a>
    <a href="/">Blog</a>
    <a href="/">Resume</a>
</nav>

<!-- Create menu navigation for mobile devices -->

<nav class="mobile-nav">
    <button onclick={toggleMenu}>☰</button>

    {#if menuOpen}
        <div class="mobile-nav">
            <a href="/" onclick={toggleMenu}>Home</a>
            <a href="/" onclick={toggleMenu}>Projects</a>
            <a href="/" onclick={toggleMenu}>Blog</a>
            <a href="/" onclick={toggleMenu}>Resume</a>
        </div>
    {/if}
</nav>

<!-- Set limits for desktop or mobile nav bar-->

<style>
    .mobile-nav {
        display: none;
    }

    @media (max-width: 768px) {
        .desktop-nav {
            display: none;
        }

        .mobile-nav {
            display: block;
        }
    }

</style>