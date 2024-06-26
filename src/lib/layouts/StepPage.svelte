<script>
  // ignore ce script
  import Step from '../components/Step.svelte';
  import StepAside from '../components/StepAside.svelte';
</script>

<div class="step__layout">
  <!-- ici j'importe deux blocs de code -->
  <Step />
  <StepAside />
</div>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .step__layout {
    max-width: var(--bp-desktop--large);
    margin: auto;
    margin-block: 3.5rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    position: relative;

    @media screen and (width >= 768px) {
      margin-block: 5rem;
    }

    padding-inline: 2.5rem;
    @media screen and (width >= 1520px) {
      padding: 0;
    }
    
    @media screen and (width >= 1280px) {
      display: grid;
      grid-template: auto / 1.75fr 1fr;
      gap: 5rem;
    }
  }
</style>