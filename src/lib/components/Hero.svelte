<script>
  // ignore ce script
  import logo from '$lib/images/frontpop_logo.png';
  import hero from '$lib/images/mathurin-napoly-matnapo-6dEyX6VzrnM-unsplash.jpg';
</script>

<section class="hero">
  <div class="hero__content">
    <h2 class="hero__subtitle">Élections législatives 2024</h2>
    <img src="{logo}" alt="logo du nouveau front populaire" class="hero__logo">
  
    <h1 class="hero__title">Un programme de rupture</h1>
    <p class="hero__text">Le Nouveau Front Populaire rassemble des femmes et des hommes issus d'organisations politiques, syndicales, associatives et citoyennes qui s'unissent pour construire un programme de rupture avec la politique d'Emmanuel Macron, répondant aux urgences sociales, écologiques, démocratiques et pour la paix.</p>
  
    <a href="/programme" class="hero__button-link">Découvrir le programme<span class="arrow"></span></a>
  </div>

  <div class="hero__background">
    <img src="{hero}" alt="personnes tenant une banderole pendant la journée">
  </div>
</section>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .hero {
    height: calc(100vh - 10rem);
    display: flex;
    flex-direction: column;
    position: relative;
    
    @media screen and (width >= 768px) {
      height: calc(100vh - 7.5rem);
    }
    @media screen and (width >= 1440px) {
      height: calc(100vh - 8.5rem);
    }
  }

  .hero__content {
    max-width: var(--bp-desktop);
    margin: auto;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    text-align: center;
    color: var(--c-background);

    padding-inline: 2.5rem;
    @media screen and (width >= 1280px) {
      padding-inline: 10.75rem;
    }
  }

  .hero__logo {
    margin-inline: auto;
    height: 6rem;
    
    @media screen and (width >= 1440px) {
      height: 12rem;
    }
  }

  .hero__title {
    font-size: var(--fs-title--larger);
  }

  .hero__subtitle {
    text-transform: initial;
    display: none;

    @media screen and (width >= 768px) {
      display: initial;
    }
    @media screen and (width >= 1280px) {
      display: none;
    }
    @media screen and (width >= 1440px) {
      display: initial;
    }
  }

  .hero__button-link {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin-inline: auto;
    background-color: var(--c-red);
    padding: 0.5rem 1.5rem;
    color: var(--c-background);
    font-weight: var(--fw--bold);
    text-decoration: none;
    border: transparent;
    text-transform: uppercase;

    transition: gap 0.3s;
    &:hover,
    &:focus-visible {
      gap: 1.5rem;
    }

    & .arrow {
      display: inline-block;
      width: 1.5rem;
      height: 2px;
      background-color: var(--c-background);
      position: relative;

      &::before,
      &::after {
        content: '';
        position: absolute;
        width: 0.75rem;
        height: 2px;
        background-color: var(--c-background);
        right: -3.25px;
      }
      
      &::before {
        rotate: 45deg;
        top: -3.75px;
      }

      &::after {
        rotate: -45deg;
        bottom: -3.75px;
      }
    } 
  }

  .hero__background {
    position: absolute;
    background-color: var(--c-text);
    width: 100%;
    height: 100%;
    z-index: -1;
    
    & img {
      width: 100%;
      height: 110%;
      object-fit: cover;
      object-position: bottom;
      filter: blur(4px) brightness(0.5);
    }
  }
</style>