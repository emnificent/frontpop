<script>
  // ignore ce script
  import '$lib/styles/reset.css';
  import '$lib/styles/global.css';

  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import ColorBar from '$lib/components/ColorBar.svelte';
</script>

<!-- ici j'importe le header, le footer et la barre de couleur, et je place le contenu de toutes les pages entre les deux -->
<Header />
<slot />
<Footer />

<ColorBar />