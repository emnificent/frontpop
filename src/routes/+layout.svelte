<script>
  // ignore ce script
  import '$lib/styles/reset.css';
  import '$lib/styles/global.css';

  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<!-- ici j'importe le header et le footer, et je place le contenu de toutes les pages entre les deux -->
<Header />
<slot />
<Footer />