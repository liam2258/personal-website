<svelte:head>
  <title>Projects | Liam Dyer</title>
</svelte:head>

<div class="projects-page">
  <header class="projects-header">
    <h1>Projects</h1>
    <p>
      I've been fortunate enough to work on some pretty cool projects over the course of my coding career
      (and some not very cool ones, and some weird ones tbh...).
      Here is a collection of some of the big ones! What I learned, what tools I used, what it did — all of
      the traditional informative pieces found in a project collage!
    </p>
  </header>
</div>

<style>
  .projects-page {
    padding: 4rem 2rem;
    max-width: 960px;
    margin: 0 auto;
  }

  .projects-header {
    margin-bottom: 4rem;
  }

  .projects-header h1 {
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    font-weight: 700;
    color: var(--color-text);
    line-height: 1.1;
    margin-bottom: 1.5rem;
  }

  .projects-header p {
    font-size: clamp(1.05rem, 1.8vw, 1.35rem);
    line-height: 1.8;
    color: var(--color-text-muted);
    max-width: 1200px;
  }

  @media (max-width: 640px) {
    .projects-page {
      padding: 2.5rem 1.25rem;
    }
  }
</style>