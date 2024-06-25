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

  function copyUrl(event) {
    event.preventDefault();
    navigator.clipboard.writeText(window.location.href);
  }
</script>

<main class="step">
  <div>
    <h2 class="step__subtitle">L'été des bifurcations</h2>
    <h1 class="step__title">Faire une grande loi pour le pouvoir d'achat</h1>
  </div>

  <div class="step__details">
    <div class="step__share">
      <p>Partager :</p>
      <a href="https://x.com/intent/tweet?text=https://host.fr" target="_blank"><i class="fa-brands fa-x-twitter"></i><span class="step__share-background"></span></a>
      <a href="https://facebook.com/sharer/sharer.php?u=https://host.fr/" target="_blank"><i class="fa-brands fa-facebook-f"></i><span class="step__share-background"></span></a>
      <button aria-label="copier le lien de la page" on:click={copyUrl} onclick="copyUrl()"><i class="fa-solid fa-link"></i><span class="step__share-background"></span></button>
    </div>

    <div class="step__text" tabindex="0" on:click={showModal} on:keypress={showModalKeyboard} role="button" aria-label="partager (ouvre une popup)" onclick="showModal()" onkeypress="showModalKeyboard()">
      <p>Indexer les salaires sur l'inflation et porter l'Allocation aux adultes handicapés (AAH) au niveau du SMIC</p>
      <p class="step__share-highlight">Partager</p>
      <span class="step__text-background"></span>
    </div>
    <div class="step__text" tabindex="0" on:click={showModal} on:keypress={showModalKeyboard} role="button" aria-label="partager (ouvre une popup)" onclick="showModal()" onkeypress="showModalKeyboard()">
      <p>Abolir la monarchie présidentielle dans la pratique des institutions :</p>
      <ul>
        <li>Instaurer la proportionnelle</li>
        <li>Revitaliser le parlement</li>
        <li>Abroger le 49.3</li>
        <li>Défendre la décentralisation effective en renforçant la démocratie locale dans l'unité de la République</li>
      </ul>
      <p class="step__share-highlight">Partager</p>
      <span class="step__text-background"></span>
    </div>
    <div class="step__text" tabindex="0" on:click={showModal} on:keypress={showModalKeyboard} role="button" aria-label="partager (ouvre une popup)" onclick="showModal()" onkeypress="showModalKeyboard()">
      <p>Abolir la taxe Macron de 10% sur les factures d'énergie, annuler la hausse programmée du prix du gaz au 1er juillet, plafonner les frais bancaires, faire la gratuité des premiers KwH, abolir les coupures d'électricité, de chaleur et de gaz (hors trêve hivernale), annuler les réformes Macron sur le revenu de solidarité active (RSA)</p>
      <p class="step__share-highlight">Partager</p>
      <span class="step__text-background"></span>
    </div>

    <div class="step__navigation">
      <a href="/step">
        <span class="step__navigation-arrow"><span class="arrow"></span></span>
        <span class="step__navigation-text">Précédent<span class="step__navigation-text-background"></span></span>
        <span class="step__navigation-background"></span>
      </a>
      <a href="/step">
        <span class="step__navigation-text">Suivant<span class="step__navigation-text-background"></span></span>
        <span class="step__navigation-arrow"><span class="arrow"></span></span>
        <span class="step__navigation-background"></span>
      </a>
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

  .step__subtitle {
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
      position: relative;
      z-index: 0;
      text-decoration: none;
      width: 2rem;
      height: 2rem;
      border-radius: 50%;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      box-sizing: border-box;
      border: none;
      padding: 4px;
      background-color: transparent;
      color: var(--c-background);

      &:hover,
      &:focus-visible {
        & .step__share-background {
          opacity: 0.8;
        }
      }
    }

    & .step__share-background {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      background-color: var(--c-text);
      transition: opacity 0.3s;
    }
  }

  .step__text {
    padding-block: 1.5rem;
    padding-inline: 2.5rem 2rem;
    position: relative;
    box-shadow: inset 0 -1px var(--c-red),
                inset 8px 0 var(--c-red);

    &:hover,
    &:focus-visible {
      & .step__share-highlight {
        border: unset;
        padding: unset;
        clip-path: rect(0 100% 100% 0);
        height: auto;
        width: auto;
        margin: 0px;
        overflow: unset;

        width: fit-content;
        padding-block: 1rem 2px;
        border-bottom: 1px solid var(--c-red);
      }
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

  .step__share-highlight {
    color: var(--c-red);
    cursor: default;
    transition: clip-path 0.3s, height 0.3s, margin 0.3s, padding 0.3s, border 0.3s;

    border: 0px;
    padding: 0px;
    clip-path: rect(0 0% 0% 0);
    height: 1px;
    width: 1px;
    margin: -1px;
    overflow: hidden;
  }

  .step__navigation {
    display: flex;
    justify-content: space-between;

    & a {
      text-decoration: none;
      position: relative;
      z-index: 0;
      color: var(--c-red);
      background-color: transparent;
      border: 1px solid var(--c-red);
      display: flex;
      align-items: center;

      &:hover,
      &:focus-visible {
        & .step__navigation-text-background {
          opacity: 0.8;
        }

        & .step__navigation-background {
          opacity: 0.8;
        }
      }

      &:first-child {
        & .arrow {
          transform: scale(-1, -1);
        }
      }
    }

    & .step__navigation-background {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      background-color: var(--c-red);
      transition: opacity 0.3s;
    }
    
    & .step__navigation-text {
      position: relative;
      z-index: 0;
      display: inline-block;
      background-color: transparent;
      padding: 0.5rem 1rem;
      width: 5.75rem;
      display: flex;
      justify-content: center;
      transition: color 0.3s, background-color 0.3s;
      
      & .step__navigation-text-background {
        position: absolute;
        z-index: -1;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: var(--c-background);
        transition: opacity 0.3s;
      }
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