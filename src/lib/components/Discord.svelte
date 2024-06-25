<section class="discord">
  <h2 class="discord__title">Le front populaire s'organise sur Discord</h2>

  <p>Le site a été entièrement conçu par des citoyens ayant rejoint le Discord du Front Populaire.<br/>Il reprend l'intégralité du programme officiel issu du contrat de législature du Nouveau Front Populaire.<br/>Rejoignez la mobilisation citoyenne sur Discord !</p>

  <a href="https://discord.gg/barricade" class="discord__button-link"><i class="fa-brands fa-discord"></i>Rejoindre le Discord<span class="discord__button-link-background"></span></a>
</section>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .discord {
    max-width: var(--bp-desktop);
    margin: auto;
    margin-block: 5rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    text-align: center;
  }

  .discord__title {
    font-size: var(--fs-title--large);
  }

  .discord__button-link {
    position: relative;
    z-index: 0;
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin-inline: auto;
    padding: 0.5rem 1.5rem;
    background-color: transparent;
    color: var(--c-background);
    font-weight: var(--fw--bold);
    text-decoration: none;
    border: transparent;
    text-transform: uppercase;

    &:hover,
    &:focus-visible {
      & .discord__button-link-background {
        opacity: 0.8;
      }
    }
  }
  
  .discord__button-link-background {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: -1;
    background-color: var(--c-text);
    transition: opacity 0.3s;
  }
</style>