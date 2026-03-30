<div class="intro">
  <h1>Greetings Fellow Humans! My name is...</h1>
  <h2>Liam Dyer</h2>
  <ul class="titles">
    <li>Software Developer</li>
    <li>Video Game Player</li>
    <li>Juneauian? Juneayan? Juneauite</li>
    <li><del>Vtuber Enthusiast</del> Japan Admirer</li>
  </ul>
</div>

<style>

  .intro {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 15vh;
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
</style>