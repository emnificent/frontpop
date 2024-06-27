<script>
  // ignore ce script
  import Roadmap from '$lib/components/Roadmap.svelte';
  import Search from '$lib/components/Search.svelte';
  import hero from '$lib/images/080_hl_stenani_2423101.jpg'
</script>

<main>
  <div class="roadmap-page__image">
    <img src="{hero}" alt="les négociateurs des partis de gauche réunis pour former le Nouveau Front Populaire">
  </div>

  <article class="roadmap-page__introduction">
    <h1 class="roadmap-page__introduction-title">Un cap clair pour le nouveau front populaire</h1>

    <p class="roadmap-page__introduction-text">Le Nouveau Front Populaire rassemble des femmes et des hommes issus d'organisations politiques, syndicales, associatives et citoyennes qui s'unissent pour construire un programme de rupture avec la politique d'Emmanuel Macron, répondant aux urgences sociales, écologiques, démocratiques et pour la paix.<br/><br/>Nous combattons le projet raciste et de casse sociale de l'extrême droite et voulons l'empêcher d'arriver au pouvoir.<br/><br/>Nous refusons les attaques contre nos libertés démocratiques et la répression vis à vis des forces sociales et associatives, particulièrement bafouées ces  dernières années.<br/><br/>Nous luttons contre la multiplication des discours de haine et contre la prolifération des menaces et des violences qui abîment notre démocratie.<br/><br/>C'est pourquoi notre majorité et nos parlementaires s'engagent à porter ces principes éthiques tout au long de la mandature en refusant la diffusion de fausses informations, la calomnie, le cyberharcèlement, et les incitations à la haine, y compris sur internet.<br/><br/>En donnant une majorité de députés au Nouveau Front Populaire, les Françaises et les Français écriront une nouvelle page de l'histoire de France.<br/><br/>Les 30 juin et 7 juillet, votez pour le Nouveau Front Populaire !</p>
  </article>

  <!-- ici j'importe deux blocs de code -->
  <Roadmap />
  <Search />
</main>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .roadmap-page__introduction {
    max-width: var(--bp-desktop--large);
    margin: auto;
    margin-block: 3.5rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    
    @media screen and (width >= 768px) {
      margin-block: 5rem;
    }

    padding-inline: 2.5rem;
    @media screen and (width >= 1280px) {
      padding-inline: 10.75rem;
    }
  }

  .roadmap-page__introduction-title {
    font-size: var(--fs-title--large);
  }

  .roadmap-page__introduction-text {
    text-align: justify;
    
    @media screen and (width >= 1280px) {
      column-count: 2;
      column-gap: 2.5rem;
    }
  }

  .roadmap-page__image {
    height: 14.5rem;
    overflow: hidden;
    
    & img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: bottom;

      @media screen and (width >= 768px) {
        height: 200%;
      }
      @media screen and (width >= 2560px) {
        height: 250%;
      }
    }
    
    @media screen and (width >= 1280px) {
      height: 34rem;
    }
  }
</style>