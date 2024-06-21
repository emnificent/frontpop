<section class="discord">
  <h2 class="discord__title">Le front populaire s'organise sur Discord</h2>

  <p>Le site a été entièrement conçu par des citoyens ayant rejoint le Discord du Front Populaire.<br/>Il reprend l'intégralité du programme officiel issu du contrat de législature du Nouveau Front Populaire.<br/>Rejoignez la mobilisation citoyenne sur Discord !</p>

  <a href="https://discord.gg/barricade" class="discord__button-link"><i class="fa-brands fa-discord"></i>Rejoindre le Discord</a>
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
    display: flex;
    align-items: center;
    gap: 0.5rem;
    margin-inline: auto;
    background-color: var(--c-text);
    padding: 0.5rem 1.5rem;
    color: var(--c-background);
    font-weight: var(--fw--bold);
    text-decoration: none;
    border: transparent;
    transition: box-shadow 0.3s;
    text-transform: uppercase;

    &:hover,
    &:focus-visible {
      box-shadow: var(--c-text) 0 4px 8px -2px;
    }   
  }
</style>