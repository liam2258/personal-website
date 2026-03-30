<div class="intro">
  <h1>Greetings Fellow Humans! I am...</h1>
  <h2>Liam Dyer</h2>
  <ul class="titles">
    <li>Software Developer</li>
    <li>Video Game Player</li>
    <li>Juneauian? Juneayan? Juneauite</li>
    <li><del>Vtuber Enthusiast</del> Japan Admirer</li>
  </ul>
  <button class="scroll-arrow" onclick={() => document.getElementById('about')?.scrollIntoView({ behavior: 'smooth' })}>
    ▼
  </button>
</div>

<section id="about">
  <h2 class="section-heading">About Me</h2>
  <p>Your content here...</p>
</section>

<style>
  .intro {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 15vh;
    min-height: 100vh;
  }

  h1 {
    font-size: clamp(1rem, 2.5vw, 1.75rem);
    font-weight: 400;
    color: var(--color-text-muted);
  }

  h2 {
    font-size: clamp(3rem, 8vw, 7rem);
    font-weight: 700;
    color: var(--color-text);
    line-height: 1.1;
  }

  .section-heading {
    font-size: clamp(1.5rem, 3vw, 2.5rem);
    font-weight: 600;
    color: var(--color-text);
    line-height: 1.3;
  }

  .titles {
    list-style: none;
    text-align: center;
    font-size: clamp(0.75rem, 1.5vw, 1.1rem);
    margin-top: 1.5rem;
    line-height: 1.8;
  }

  .titles li:nth-child(1) { color: #3b82f6; }
  .titles li:nth-child(2) { color: #f59e0b; }
  .titles li:nth-child(3) { color: #10b981; }
  .titles li:nth-child(4) { color: #ec4899; }

  .titles del {
    opacity: 0.5;
  }

  .scroll-arrow {
    margin-top: 4rem;
    background: none;
    border: none;
    color: var(--color-accent);
    font-size: 1.5rem;
    cursor: pointer;
    animation: bob 2s ease-in-out infinite;
  }

  .scroll-arrow:hover {
    color: var(--color-primary);
  }

  @keyframes bob {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(0.5rem); }
  }

  #about {
    padding: 4rem 1rem;
    text-align: center;
  }
</style>