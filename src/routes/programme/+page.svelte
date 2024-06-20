<script>
  import Roadmap from '$lib/components/Roadmap.svelte';
  import Search from '$lib/components/Search.svelte';
</script>

<main>
  <img src="" alt="">

  <article class="introduction">
    <h1 class="introduction__title">UN CAP CLAIR POUR LE NOUVEAU FRONT POPULAIRE</h1>

    <p class="introduction__text">Le Nouveau Front Populaire rassemble des femmes et des hommes issus d'organisations politiques, syndicales, associatives et citoyennes qui s'unissent pour construire un programme de rupture avec la politique d'Emmanuel Macron, répondant aux urgences sociales, écologiques, démocratiques et pour la paix.<br/><br/>Nous combattons le projet raciste et de casse sociale de l'extrême droite et voulons l'empêcher d'arriver au pouvoir.<br/><br/>Nous refusons les attaques contre nos libertés démocratiques et la répression vis à vis des forces sociales et associatives, particulièrement bafouées ces  dernières années.<br/><br/>Nous luttons contre la multiplication des discours de haine et contre la prolifération des menaces et des violences qui abîment notre démocratie.<br/><br/>C'est pourquoi notre majorité et nos parlementaires s'engagent à porter ces principes éthiques tout au long de la mandature en refusant la diffusion de fausses informations, la calomnie, le cyberharcèlement, et les incitations à la haine, y compris sur internet.<br/><br/>En donnant une majorité de députés au Nouveau Front Populaire, les Françaises et les Français écriront une nouvelle page de l'histoire de France.<br/><br/>Les 30 juin et 7 juillet, votez pour le Nouveau Front Populaire !</p>
  </article>

  <Roadmap />

  <Search />
</main>

<style lang="scss">
  .introduction {
    max-width: var(--bp-desktop--large);
    margin: auto;
    margin-block: 5rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  .introduction__title {
    font-size: var(--fs-title--large);
  }

  .introduction__text {
    column-count: 2;
    column-gap: 2.5rem;
    text-align: justify;
  }

  /* TEMP */
  img {
    height: 100%;
    width: 100%;
    height: 34rem;
    background: orange;
  }
</style>