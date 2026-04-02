<script lang="ts">
    import { resolve } from '$app/paths';
    import favicon from '$lib/assets/favicon.svg';
    let menuOpen = $state(false);
    function toggleMenu() {
        menuOpen = !menuOpen;
    }
</script>
<nav class="desktop-nav">
    <a href={resolve('/')} class="brand">
        <img src={favicon} alt="Home" class="brand-icon" />
    </a>
    <div class="nav-links">
        <a href={resolve('/projects')}>Projects</a>
        <a href={resolve('/')}>Blog</a>
        <a href={resolve('/')}>Resume</a>
    </div>
</nav>
<nav class="mobile-nav">
    <a href={resolve('/')} class="brand">Home</a>
    <button class="hamburger" onclick={toggleMenu} aria-label="Toggle menu">☰</button>
    {#if menuOpen}
        <div class="mobile-dropdown">
            <a href={resolve('/projects')} onclick={toggleMenu}>Projects</a>
            <a href={resolve('/')} onclick={toggleMenu}>Blog</a>
            <a href={resolve('/')} onclick={toggleMenu}>Resume</a>
        </div>
    {/if}
</nav>
<style>
    /* ---- Desktop ---- */
    .desktop-nav {
        display: flex;
        align-items: center;
        height: 56px;
        padding: 0 2rem;
        background: var(--color-surface);
        border-bottom: 1px solid var(--color-border);
    }
    .brand-icon {
        height: 40px;
        width: auto;
    }
    .desktop-nav .brand {
        margin-right: auto;
        font-weight: 700;
        font-size: 1.1rem;
        color: var(--color-accent);
        text-decoration: none;
        letter-spacing: 0.02em;
    }
    .nav-links {
        display: flex;
        gap: 2rem;
    }
    .nav-links a {
        color: var(--color-text-muted);
        text-decoration: none;
        font-size: 0.925rem;
        font-weight: 500;
        padding: 0.25rem 0;
        position: relative;
        transition: color 0.2s ease;
    }
    .nav-links a::after {
        content: '';
        position: absolute;
        bottom: -2px;
        left: 0;
        width: 0;
        height: 2px;
        background: var(--color-primary);
        transition: width 0.25s ease;
    }
    .nav-links a:hover {
        color: var(--color-text);
    }
    .nav-links a:hover::after {
        width: 100%;
    }
    /* ---- Mobile ---- */
    .mobile-nav {
        display: none;
        align-items: center;
        height: 56px;
        padding: 0 1.25rem;
        background: var(--color-surface);
        border-bottom: 1px solid var(--color-border);
        position: relative;
    }
    .mobile-nav .brand {
        margin-right: auto;
        font-weight: 700;
        color: var(--color-accent);
        text-decoration: none;
    }
    .hamburger {
        background: none;
        border: none;
        color: var(--color-text-muted);
        font-size: 1.5rem;
        cursor: pointer;
        padding: 0.25rem;
    }
    .mobile-dropdown {
        position: absolute;
        top: 56px;
        left: 0;
        right: 0;
        background: var(--color-surface);
        display: flex;
        flex-direction: column;
        padding: 0.5rem 0;
        border-bottom: 1px solid var(--color-border);
        z-index: 100;
    }
    .mobile-dropdown a {
        color: var(--color-text-muted);
        text-decoration: none;
        padding: 0.75rem 1.5rem;
        transition: background 0.15s ease;
    }
    .mobile-dropdown a:hover {
        background: var(--color-background);
        color: var(--color-text);
    }
    @media (max-width: 768px) {
        .desktop-nav {
            display: none;
        }
        .mobile-nav {
            display: flex;
        }
    }
</style>