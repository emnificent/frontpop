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

  function copyUrl(event) {
    event.preventDefault();
    navigator.clipboard.writeText(window.location.href);
  }
</script>

<!-- ignore les commentaires ci-dessous -->
<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-autofocus -->
<dialog class="step-dialog" id="step-modal" autofocus on:click={closeModalOnBackdropClick} onclick="closeModalOnBackdropClick()">
  <form class="step-dialog__content" method="dialog">
    <div>
      <h2 class="step-dialog__subtitle" id="step-modal-subtitle"> </h2>
      <h1 class="step-dialog__title" id="step-modal-title"> </h1>
    </div>

    <div>
      <div class="step-dialog__text" id="step-modal-text"></div>
    
      <div class="step-dialog__share">
        <p>Partager :</p>
        <a href="https://x.com/intent/tweet?text=https://host.fr" target="_blank"><i class="fa-brands fa-x-twitter"></i><span class="step-dialog__share-background"></span></a>
        <a href="https://facebook.com/sharer/sharer.php?u=https://host.fr/" target="_blank"><i class="fa-brands fa-facebook-f"></i><span class="step-dialog__share-background"></span></a>
        <button aria-label="copier le lien de la mesure" on:click={copyUrl} onclick="copyUrl()"><i class="fa-solid fa-link"></i><span class="step-dialog__share-background"></span></button>
      </div>
    </div>
  
  
    <button class="step-dialog__close-button" aria-label="fermer la popup"></button>
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

    min-width: 65vw;
    @media screen and (width >= 768px) {
      min-width: 80vw;
    }
    @media screen and (width >= 1280px) {
      min-width: auto;
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
    color: var(--c-subtitle);
  }

  .step-dialog__text {
    padding-block: 1.5rem;
    padding-inline: 2.5rem 2rem;
    position: relative;
    background-color: var(--c-background);
    box-shadow: inset 0 -1px var(--c-red),
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
        & .step-dialog__share-background {
          opacity: 0.8;
        }
      }
    }

    & .step-dialog__share-background {
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

  .step-dialog__close-button {
    position: absolute;
    width: 2rem;
    height: 2rem;
    border: none;
    background-color: transparent;
    display: flex;
    align-items: center;
    justify-content: center;
    outline: transparent solid 2px;
    transition: outline 0.3s;

    scale: 0.5;
    top: -0.5rem;
    right: -0.5rem;

    @media screen and (width >= 768px) {
      scale: 1;
      top: 0;
      right: 0;
    }

    &:hover,
    &:focus-visible {
      outline: var(--c-text) solid 2px;
    }

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

  .step-dialog {
    &::backdrop {
      background-color: var(--c-style);
    }
    & .step-dialog__background {
      background-color: var(--c-style);
    }
    & .step-dialog__title {
      color: var(--c-style);
    }
    & .step-dialog__text {
      box-shadow: inset 0 -1px var(--c-style),
                  inset 8px 0 var(--c-style);
      & ul > li::before {
        color: var(--c-style);
      }
    }
  }
</style>