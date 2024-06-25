<section class="search">
  <div class="search__container">
    <h2 class="search__title">Je veux connaître le programme du front populaire sur...</h2>
  
    <div class="search__shortcuts">
      <a href="/search?q=pouvoir d'achat">Pouvoir d'achat<span class="search__shortcuts-background"></span></a>
      <a href="/search?q=planification écologique">Planification écologique<span class="search__shortcuts-background"></span></a>
      <a href="/search?q=retraite">Retraite<span class="search__shortcuts-background"></span></a>
      <a href="/search?q=l'urgence de la paix">L'urgence de la paix<span class="search__shortcuts-background"></span></a>
    </div>
  
    <div class="search__input">
      <input type="search" name="" id="" placeholder="Cherchez par mots clés: économie, justice, écologie...">
      <button aria-label="lancer la recherche"><i class="fa-solid fa-magnifying-glass"></i></button>
    </div>
  </div>
</section>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .search {
    background-color: var(--c-green);
    padding-block: 5rem;
  }

  .search__container {
    max-width: var(--bp-tablet);
    margin: auto;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  .search__title {
    font-size: var(--fs-title--large);
    text-align: center;
    line-height: 1.1;
    color: var(--c-background);
  }

  .search__shortcuts {
    display: flex;
    justify-content: space-between;

    & a {
      position: relative;
      text-decoration: none;
      display: inline-block;
      z-index: 0;
      color: var(--c-background);
      background-color: transparent;
      padding: 0.5rem 1.5rem;
      border: transparent;
      width: fit-content;
      font-size: var(--fs-text--small);
      &::first-letter {
        text-transform: capitalize;
      }
      
      & .search__shortcuts-background {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: var(--c-text);
        z-index: -1;
        transition: opacity 0.3s;
      }

      &:hover,
      &:focus-visible {
        & .search__shortcuts-background {
          opacity: 0.8;
        }
      }
    }
  }

  .search__input {
    display: flex;
    gap: 1rem;
    background-color: var(--c-background);
    border-radius: 1rem;
    overflow: hidden;
    padding: 1rem 2rem;
    border: 1px solid var(--c-text);

    & input {
      background-color: transparent;
      color: var(--c-text);
      width: 100%;
      border: none;
      outline: none;
    }

    & button {
      width: 2rem;
      height: 2rem;
      display: flex;
      align-items: center;
      justify-content: center;
      border: transparent;
      background-color: transparent;
      font-size: var(--fs-text--large);
      opacity: 0.5;
      transition: opacity 0.3s;

      &:hover,
      &:focus-visible {
        opacity: 1;
      }
    }
  }
</style>