<script>
  function closeModalOnBackdropClick(event) {
    const dialog = event.target;
    const dialogArea = dialog.getBoundingClientRect();
    const isClickInDialog = dialogArea.top <= event.clientY
                            && event.clientY <= dialogArea.top + dialogArea.height 
                            && dialogArea.left <= event.clientX
                            && event.clientX <= dialogArea.left + dialogArea.width;
    if (!isClickInDialog) dialog.close();
  }
</script>

<!-- ignore les deux commentaires ci-dessous -->
<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<dialog class="step-dialog" id="step-modal" on:click={closeModalOnBackdropClick} onclick="closeModalOnBackdropClick()">
  <form class="step-dialog__content" method="dialog">
    <div>
      <h2 class="step-dialog__subtitle">L'été des bifurcations</h2>
      <h1 class="step-dialog__title">Faire une grande loi pour le pouvoir d'achat</h1>
    </div>

    <div>
      <div class="step-dialog__text">
        <p>Abolir la taxe Macron de 10% sur les factures d'énergie, annuler la hausse programmée du prix du gaz au 1er juillet, plafonner les frais bancaires, faire la gratuité des premiers KwH, abolir les coupures d'électricité, de chaleur et de gaz (hors trêve hivernale), annuler les réformes Macron sur le revenu de solidarité active (RSA)</p>
      </div>
    
      <div class="step-dialog__share">
        <p>Partager :</p>
        <a href="https://x.com/DiscordGauche" target="_blank"><i class="fa-brands fa-x-twitter"></i></a>
        <a href="https://facebook.com/discordgauche" target="_blank"><i class="fa-brands fa-facebook-f"></i></a>
        <button><i class="fa-solid fa-link"></i></button>
      </div>
    </div>
  
  
    <button class="step-dialog__close-button"></button>
  </form>
  <span class="step-dialog__background"></span>
</dialog>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .step-dialog {
    max-width: var(--bp-desktop);
    border: none;
    position: fixed;
    top: 50%;
    left: 50%;
    translate: -50% -50%;
    padding: 2rem;

    &::backdrop {
      background-color: var(--c-red);
      opacity: 0.75;
    }
  }

  .step-dialog__content {
    position: relative;
    z-index: 99999;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .step-dialog__background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: var(--c-red);
    opacity: 0.1;
    z-index: 999;
  }

  .step-dialog__title {
    color: var(--c-red);
    text-transform: initial;
  }

  .step-dialog__subtitle {
    font-size: var(--fs-text);
    color: var(--c-green);
  }

  .step-dialog__text {
    padding-block: 1.5rem;
    padding-inline: 2.5rem 2rem;
    position: relative;
    background-color: var(--c-background);
    box-shadow: inset 0 -2px var(--c-red),
                inset 8px 0 var(--c-red);

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
  }

  .step-dialog__share {
    margin-top: 1rem;
    display: flex;
    align-items: center;
    justify-content: flex-end;
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
      border: 4px solid var(--c-background);
      background-color: var(--c-background);
      color: var(--c-text);
    }
  }

  .step-dialog__close-button {
    position: absolute;
    width: 2rem;
    height: 2rem;
    top: 0;
    right: 0;
    border: none;
    background-color: transparent;
    display: flex;
    align-items: center;
    justify-content: center;

    &::before,
    &::after {
      content: '';
      position: absolute;
      width: 2rem;
      height: 2px;
      background-color: var(--c-text);
    }

    &::before {
      rotate: 45deg;
    }

    &::after {
      rotate: -45deg;
    }
  }
</style>