<script>
  // ignore cette ligne
  import StepDialog from './StepDialog.svelte';

  // prends le code ci-dessous
  function showModalKeyboard(event) {
    if (![' ', 'Enter'].includes(event.key)) return;
    event.preventDefault();
    showModal();
  }

  function showModal() {
    document.getElementById('step-modal').showModal();
  }
</script>

<main class="step">
  <div>
    <a href="/programme#tab2" class="step__back-link"><h2>L'été des bifurcations</h2></a>
    <h1 class="step__title">Faire une grande loi pour le pouvoir d'achat</h1>
  </div>

  <div class="step__details">
    <div class="step__share">
      <p>Partager :</p>
      <a href="https://x.com/DiscordGauche" target="_blank"><i class="fa-brands fa-x-twitter"></i></a>
      <a href="https://facebook.com/discordgauche" target="_blank"><i class="fa-brands fa-facebook-f"></i></a>
      <button><i class="fa-solid fa-link"></i></button>
    </div>

    <div class="step__text" tabindex="0" on:click={showModal} on:keypress={showModalKeyboard} role="button" onclick="showModal()" onkeypress="showModalKeyboard()">
      <p>Indexer les salaires sur l'inflation et porter l'Allocation aux adultes handicapés (AAH) au niveau du SMIC</p>
      <span class="step__text-background"></span>
    </div>
    <div class="step__text" tabindex="0" on:click={showModal} on:keypress={showModalKeyboard} role="button" onclick="showModal()" onkeypress="showModalKeyboard()">
      <p>Abolir la monarchie présidentielle dans la pratique des institutions :</p>
      <ul>
        <li>Instaurer la proportionnelle</li>
        <li>Revitaliser le parlement</li>
        <li>Abroger le 49.3</li>
        <li>Défendre la décentralisation effective en renforçant la démocratie locale dans l'unité de la République</li>
      </ul>
      <span class="step__text-background"></span>
    </div>
    <div class="step__text" tabindex="0" on:click={showModal} on:keypress={showModalKeyboard} role="button" onclick="showModal()" onkeypress="showModalKeyboard()">
      <p>Abolir la taxe Macron de 10% sur les factures d'énergie, annuler la hausse programmée du prix du gaz au 1er juillet, plafonner les frais bancaires, faire la gratuité des premiers KwH, abolir les coupures d'électricité, de chaleur et de gaz (hors trêve hivernale), annuler les réformes Macron sur le revenu de solidarité active (RSA)</p>
      <span class="step__text-background"></span>
    </div>

    <div class="step__navigation">
      <button>
        <span class="step__navigation-arrow"><span class="arrow"></span></span>
        <span class="step__navigation-text">Précédent</span>
      </button>
      <button>
        <span class="step__navigation-text">Suivant</span>
        <span class="step__navigation-arrow"><span class="arrow"></span></span>
      </button>
    </div>
  </div>
</main>

<!-- ici j'importe un bloc de code -->
<StepDialog />

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .step {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  .step__back-link {
    text-decoration: none;
    font-weight: var(--fw--bold);
    color: var(--c-green);
  }

  .step__title {
    font-size: var(--fs-title--large);
    line-height: 1.1;
    color: var(--c-red);
  }

  .step__details {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .step__share {
    display: flex;
    align-items: center;
    gap: 0.5rem;

    & a,
    & button {
      text-decoration: none;
      width: 2rem;
      aspect-ratio: 1/1;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      box-sizing: border-box;
      border: 4px solid var(--c-text);
      background-color: var(--c-text);
      color: var(--c-background);
    }
  }

  .step__text {
    padding-block: 1.5rem;
    padding-inline: 2.5rem 2rem;
    position: relative;
    box-shadow: inset 0 -2px var(--c-red),
                inset 8px 0 var(--c-red);
    transition: box-shadow 0.3s;

    &:hover,
    &:focus-visible {
      box-shadow: inset 0 -2px var(--c-red),
                  inset 8px 0 var(--c-red),
                  0 4px 8px -4px var(--c-text);
      outline: transparent;
    }

    & ul {
      list-style: none;

      & li {
        position: relative;
        padding-left: 1rem;

        &::before {
          position: absolute;
          left: 0;
          top: 0;
          content: '•';
          color: var(--c-red);
        }
      }
    }

    & .step__text-background {
      background-color: var(--c-red);
      opacity: 0.1;
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: -1;
    }
  }

  .step__navigation {
    display: flex;
    justify-content: space-between;

    & button {
      color: var(--c-red);
      background-color: var(--c-red);
      border: 2px solid var(--c-red);
      display: flex;
      align-items: center;

      &:hover,
      &:focus-visible {
        & .step__navigation-text {
          color: var(--c-background);
          background-color: var(--c-red);
        }
      }

      &:first-child {
        & .arrow {
          transform: scale(-1, -1);
        }
      }
    }
    
    & .step__navigation-text {
      display: inline-block;
      padding: 0.5rem 1rem;
      background-color: var(--c-background);
      width: 5.75rem;
      transition: color 0.3s, background-color 0.3s;
    }

    & .step__navigation-arrow {
      display: inline-block;
      position: relative;
      width: 2.75rem;
    }

    & .arrow {
      display: inline-block;
      position: absolute;
      right: 25%;
      width: 1.5rem;
      height: 2px;
      background-color: var(--c-background);

      &::before,
      &::after {
        content: '';
        position: absolute;
        width: 0.75rem;
        height: 2px;
        right: -3.5px;
        background-color: var(--c-background);
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