<script>
  import Step from '../components/Step.svelte';
  import StepAside from '../components/StepAside.svelte';
</script>

<div class="step__layout">
  <Step />

  <StepAside />
</div>

<style lang="scss">
  .step__layout {
    max-width: var(--bp-desktop--large);
    margin: auto;
    margin-block: 5rem;
    display: grid;
    grid-template: auto / 1.75fr 1fr;
    gap: 5rem;
    position: relative;
  }
</style>