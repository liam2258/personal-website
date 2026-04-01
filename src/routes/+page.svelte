<script>
  import meImage from '$lib/assets/me.jpg';
</script>
<svelte:head>
  <title>Liam Dyer</title>
</svelte:head>
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
  <div class="about-content">
    <div class="about-text">
      <p>By trade I'm a computer programmer, hacking together solutions for pay since 2025.
        It's kinda like being a cyber mercenary (but way cooler). I was born and raised in Juneau,
        had the University of Alaska Anchorage as my alma mater, and have worked for the state ever since.
        In other words I'm as Alaskan as it comes!
        <br><br>
        Outside of that I love video games of all kinds but have a special passion for text heavy games that bore my girlfriend to tears,
        torturing myself with heavy weights, binging weeb media, and spending exorbatant amounts of unmarked bills on computer hardware!
        <br><br>
        Some would say I'm living the dream but I would say... I'm living my dream.
      </p>
    </div>
    <div class="about-image">
      <img src={meImage} alt="Liam Dyer" />
    </div>
  </div>
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
  .titles li:nth-child(4) { color: #ffb3e6; }
  .titles del {
    opacity: 0.75;
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
    padding: 4rem 2rem;
    text-align: center;
  }
  .about-content {
    display: flex;
    align-items: center;
    gap: 3rem;
    max-width: 1200px;
    margin: 2rem auto 0;
    text-align: left;
  }
  .about-text {
    flex: 1;
    font-size: clamp(1rem, 1.5vw, 1.25rem);
    line-height: 1.8;
  }
  .about-image {
    flex-shrink: 0;
    width: clamp(250px, 30vw, 400px);
  }
  .about-image img {
    width: 100%;
    height: auto;
    border-radius: 0.5rem;
    display: block;
  }
  @media (max-width: 640px) {
    .about-content {
      flex-direction: column-reverse;
      text-align: center;
    }
    .about-image {
      width: 60%;
    }
  }
</style>