<script>
  import logo from '$lib/images/frontpop_logo.png';
</script>

<section class="hero">
  <h2 class="hero__subtitle">Élections législatives 2024</h2>
  <img src="{logo}" alt="logo du nouveau front populaire" class="hero__logo">

  <h1 class="hero__title">UN PROGRAMME DE RUPTURE</h1>
  <p class="hero__text">Le Nouveau Front Populaire rassemble des femmes et des hommes issus d'organisations politiques, syndicales, associatives et citoyennes qui s'unissent pour construire un programme de rupture avec la politique d'Emmanuel Macron, répondant aux urgences sociales, écologiques, démocratiques et pour la paix.</p>

  <a href="/programme" class="hero__button-link">DÉCOUVRIR LE PROGRAMME <span class="arrow"></span></a>
</section>

<style lang="scss">
  .hero {
    max-width: var(--bp-desktop);
    margin: auto;
    margin-block: 5rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    text-align: center;
  }

  .hero__logo {
    height: 12rem;
    margin-inline: auto;
  }

  .hero__title {
    font-size: var(--fs-title--larger);
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
        right: -3.5px;
      }
      
      &::before {
        rotate: 45deg;
        top: -3.5px;
      }

      &::after {
        rotate: -45deg;
        bottom: -3.5px;
      }
    } 
  }
</style>