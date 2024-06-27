<div class="search-page__background">
  <main class="search-page">
    <div class="search-page__header">
      <div class="search-page__input">
        <input type="search" name="" id="" placeholder="Cherchez par mots clés: économie, justice, écologie...">
        <button aria-label="lancer la recherche"><i class="fa-solid fa-magnifying-glass"></i></button>
      </div>
      <p>38 résultats pour "planification écologique"</p>
    </div>

    <div class="search-page__results">
      <article>
        <h2>Entamer la <mark>planification écologique</mark></h2>
        <p>Abolir la taxe Macron de 10% sur les factures d’énergie, annuler la hausse programmée du prix du gaz au 1er juillet, plafonner les frais bancaires, faire la gratuité des premiers KwH, abolir les coupures d’électricité, de chaleur et de gaz (hors trêve hivernale), annuler les réformes Macron sur le revenu de solidarité active (RSA)</p>
        <a href="/step">Lire la suite<span class="arrow"></span></a>
      </article>
      <article>
        <h2>Entamer la <mark>planification écologique</mark></h2>
        <p>Abolir la taxe Macron de 10% sur les factures d’énergie, annuler la hausse programmée du prix du gaz au 1er juillet, plafonner les frais bancaires, faire la gratuité des premiers KwH, abolir les coupures d’électricité, de chaleur et de gaz (hors trêve hivernale), annuler les réformes Macron sur le revenu de solidarité active (RSA)</p>
        <a href="/step">Lire la suite<span class="arrow"></span></a>
      </article>
      <article>
        <h2>Entamer la <mark>planification écologique</mark></h2>
        <p>Abolir la taxe Macron de 10% sur les factures d’énergie, annuler la hausse programmée du prix du gaz au 1er juillet, plafonner les frais bancaires, faire la gratuité des premiers KwH, abolir les coupures d’électricité, de chaleur et de gaz (hors trêve hivernale), annuler les réformes Macron sur le revenu de solidarité active (RSA)</p>
        <a href="/step">Lire la suite<span class="arrow"></span></a>
      </article>
      <article>
        <h2>Entamer la <mark>planification écologique</mark></h2>
        <p>Abolir la taxe Macron de 10% sur les factures d’énergie, annuler la hausse programmée du prix du gaz au 1er juillet, plafonner les frais bancaires, faire la gratuité des premiers KwH, abolir les coupures d’électricité, de chaleur et de gaz (hors trêve hivernale), annuler les réformes Macron sur le revenu de solidarité active (RSA)</p>
        <a href="/step">Lire la suite<span class="arrow"></span></a>
      </article>
    </div>
  </main>
</div>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .search-page__background {
    background-color: var(--c-green);
    min-height: calc(100vh - 8.5rem);
    display: flex;
  }

  .search-page {
    width: 100%;
    max-width: var(--bp-desktop--large);
    margin: auto;
    margin-block: 3.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2.5rem;

    @media screen and (width >= 768px) {
      margin-block: 5rem;
    }

    padding-inline: 2.5rem;
    @media screen and (width >= 1280px) {
      padding-inline: 10.75rem;
    }
  }

  .search-page__header {
    width: 100%;
    max-width: var(--bp-tablet);

    & p {
      text-align: center;
      margin-top: 1rem;
      color: var(--c-background);
    }
  }

  .search-page__input {
    display: flex;
    gap: 1rem;
    background-color: var(--c-background);
    border-radius: 1rem;
    overflow: hidden;
    padding: 0.5rem 1rem;
    border: 1px solid var(--c-text);
    
    @media screen and (width >= 768px) {
      padding: 1rem 2rem;
    }
    
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

  .search-page__results {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;

    & article {
      background-color: var(--c-background);
      border: 1px solid var(--c-text);
      padding: 2.5rem;
      display: flex;
      flex-direction: column;
      gap: 2rem;

      & h2 {
        text-transform: initial;
        font-weight: var(--fw--bold);
      }

      & a {
        text-decoration: none;
        color: var(--c-text);
        font-weight: var(--fw--bold);
        display: flex;
        align-items: center;
        gap: 0.35rem;
        width: fit-content;
        border-bottom: 1px solid transparent;
        transition: border 0.3s;
        
        &:hover,
        &:focus-visible {
          border-bottom: 1px solid var(--c-text);
        }
      }

      & .arrow {
        background-color: var(--c-text);
        width: 1.5rem;
        height: 2px;
        position: relative;

        &::before,
        &::after {
          content: '';
          position: absolute;
          background-color: var(--c-text);
          width: 0.75rem;
          height: 2px;
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
  }
</style>