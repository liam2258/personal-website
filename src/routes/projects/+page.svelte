<script>
  import offenderProfile from '$lib/assets/offenderProfileCover.png';
</script>

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

  <section class="projects-list">

    <!-- TODO Need to lower the requirements for the image and text to stop being side by side, the text gets too smooshed -->
     <!-- TODO There's some kind of backround card or something behind the image when the screen gets too small, need to get rid of that -->

    <div class="project">
      <h2 class="project-title">Offender Profile 2025</h2>
      <div class="project-card">
        <div class="project-summary">
          <p>
            The Offender Profile is the premiere report for the Research & Records team at the Alaska DOC.
            <br><br>
            With the support of my supervisor I became the lead developer of this project and lead a modernization effort. The previous profiles were non-interactive PDFs
            that were manually assembled using image editing software. The 2025 Profile was completely redesigned to be an interactive web experience with numerous
            quality of life features like interactive graphs, downloadable aggregated data sets, better web accessibility for disabled folk and more!
            <br><br>
            The entire data collection process was pipelined using T-SQL and Python, while the report itself was developed using Quarto, a technical publishing system
            that combines Python, HTML/CSS, and Markdown to creative replicatable scientific publications!
          </p>
        </div>
        <div class="project-image">
          <img src={offenderProfile} alt="Offender Profile Cover Page" />
        </div>
      </div>
      <div class="project-tags">
        <span class="tag">Quarto</span>
        <span class="tag">Python</span>
        <span class="tag">HTML</span>
        <span class="tag">CSS</span>
      </div>
    </div>

  </section>
</div>

<style>
  .projects-page {
    padding: 4rem 2rem;
    max-width: 1300px;
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

  .projects-list {
    display: flex;
    flex-direction: column;
    gap: 3.5rem;
  }

  .project-title {
    font-size: clamp(1.4rem, 3vw, 1.9rem);
    font-weight: 600;
    color: var(--color-text);
    margin-bottom: 1rem;
  }

  .project-card {
    display: flex;
    gap: 2rem;
    background-color: var(--color-background);
    border: 1px solid var(--color-border);
    border-radius: 12px;
    padding: 1.75rem;
    align-items: center;
  }

  .project-summary {
    flex: 1;
    display: flex;
    align-items: center;
  }

  .project-summary p {
    font-size: clamp(0.95rem, 1.5vw, 1.1rem);
    line-height: 1.75;
    color: var(--color-text-muted);
  }

  .project-image {
    flex: 1.2;
    border-radius: 8px;
    overflow: hidden;
    background-color: var(--color-border);
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .project-image img {
    width: 100%;
    height: auto;
    object-fit: contain;
    display: block;
    border-radius: 8px;
  }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 1rem;
  }

  .tag {
    background-color: rgba(59, 130, 246, 0.12);
    color: var(--color-accent);
    font-size: 0.82rem;
    font-weight: 500;
    padding: 0.3rem 0.85rem;
    border-radius: 999px;
    border: 1px solid rgba(59, 130, 246, 0.2);
    letter-spacing: 0.01em;
  }

  @media (max-width: 640px) {
    .projects-page {
      padding: 2.5rem 1.25rem;
    }

    .project-card {
      flex-direction: column;
      padding: 1.25rem;
    }

    .project-image {
      aspect-ratio: 16 / 9;
    }
  }
</style>