<script>
	import { onMount } from 'svelte';
  import { page } from '$app/stores';

  let tab = 'tab1';
  function tabSelect(event) {
    tab = event.currentTarget.attributes.href.value.replace('#', '');
    const tabSelectors = Array.from(document.getElementsByClassName('roadmap__tab'));
    tabSelectors.forEach(tabSelector => tabSelector.classList.remove('active'));
    document.getElementById(`selector-${tab}`).classList.add('active');
    const roadmapTitle = document.getElementById('roadmap-title');
    roadmapTitle.classList.remove('tab1', 'tab2', 'tab3');
    roadmapTitle.classList.add(tab);
  }

  onMount(() => {
    tab = $page.url.hash.replace('#', '') || 'tab1';
    document.getElementById(`selector-${tab}`).classList.add('active');
    document.getElementById('roadmap-title').classList.add(tab);
  });
</script>

<div class="roadmap">
  <nav class="roadmap__nav">
    <menu class="roadmap__tabs-container">
      <li class="roadmap__tab tab1" id="selector-tab1">
        <a href="#tab1" on:click={tabSelect}>
          <div>
            <p>15 premiers jours</p>
            <p class="roadmap__tab-title">LA RUPTURE</p>
          </div>
        </a>
        <span></span>
      </li>
      <li class="roadmap__tab tab2" id="selector-tab2">
        <a href="#tab2" on:click={tabSelect}>
          <div>
            <p>100 premiers jours</p>
            <p class="roadmap__tab-title">L'ÉTÉ DES BIFURCATIONS</p>
          </div>
        </a>
        <span></span>
      </li>
      <li class="roadmap__tab tab3" id="selector-tab3">
        <a href="#tab3" on:click={tabSelect}>
          <div>
            <p>Les mois suivants</p>
            <p class="roadmap__tab-title">LES TRANSFORMATIONS</p>
          </div>
        </a>
        <span></span>
      </li>
    </menu>
  </nav>

  <section class="roadmap__content">
    <h2 class="roadmap__title" id="roadmap-title">L'ÉTÉ DES BIFURCATIONS</h2>
    <p class="roadmap__introduction">Passés les 15 premiers jours, une session extraordinaire s'ouvrira à l'Assemblée nationale, où les groupes du Nouveau Front Populaire sont majoritaires, puis une seconde à la rentrée, après la fin des Jeux Olympiques et Paralympiques. Le Parlement tient une place beaucoup plus importante dans le type de gouvernement promu par le Nouveau Front Populaire. Les députés sont particulièrement associés et / ou à l'initiative de 5 paquets législatifs pour amorcer les grandes bifurcations dont le pays a besoin. D'abord, à la suite des mesures d'urgence par décret, la présentation d'une grande loi permet de rattraper et d'améliorer la situation sociale des Français grandement paupérisés par 7 ans de macronisme et 3 ans d'inflation. Deux grandes lois permettront d'entamer la reconstruction des deux services publics les plus cruciaux : santé et éducation. Une loi énergie climat permettra de jeter les bases de la planification écologique. Enfin, le premier projet de loi de finances rectificative sera présenté pour abolir les privilèges des milliardaires.</p>

    <menu class="roadmap__steps">
      <li>
        <a href="">
          <h3>Faire une grande loi pour le pouvoir d'achat <span class="arrow"></span></h3>
          <span class="roadmap__steps-background"></span>
        </a>
      </li>
      <li>
        <a href="">
          <h3>Faire une grande loi pour la santé <span class="arrow"></span></h3>
          <span class="roadmap__steps-background"></span>
        </a>
      </li>
      <li>
        <a href="">
          <h3>Faire une grande loi éducation <span class="arrow"></span></h3>
          <span class="roadmap__steps-background"></span>
        </a>
      </li>
      <li>
        <a href="">
          <h3>Entamer la planification écologique <span class="arrow"></span></h3>
          <span class="roadmap__steps-background"></span>
        </a>
      </li>
      <li>
        <a href="">
          <h3>Lutter contre toutes les formes de racismes, contre l'antisémitisme et l'islamophobie <span class="arrow"></span></h3>
          <span class="roadmap__steps-background"></span>
        </a>
      </li>
      <li>
        <a href="">
          <h3>Abolir les privilèges des millairdaires <span class="arrow"></span></h3>
          <span class="roadmap__steps-background"></span>
        </a>
      </li>
    </menu>
  </section>
</div>

<style lang="scss">
  .roadmap {
    max-width: var(--bp-desktop--large);
    margin: auto;
    margin-block: 5rem;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  .roadmap__nav {
    position: sticky;
    top: 0;
    z-index: 99999;
    background-color: var(--c-background);
  }

  .roadmap__tabs-container {
    display: grid;
    grid-template: auto / repeat(3, 1fr);
    border: 2px solid var(--c-text);
  }

  .roadmap__tab {
    padding: 1.5rem;
    position: relative;
    transition: background-color 0.3s;

    & a {
      text-decoration: none;
      color: var(--c-text);
      opacity: 0.5;
      transition: color 0.3s, opacity 0.3s;
    }

    & p {
      text-align: center;
      font-weight: var(--fw--bolder);
    }

    & span {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      z-index: -1;
      opacity: 0;
      transition: opacity 0.3s;
    }

    &.tab1, &.tab2, &.tab3 {
      &:hover,
      &:focus-visible {
        & span {
          opacity: 0.2;
        }
      }

      &.active {
        & a {
          color: var(--c-background);
          opacity: 1;
        }
      }
    }
    &.tab1 {
      &:hover,
      &:focus-visible {
        & span {
          background-color: var(--c-red);
        }
      }

      &.active {
        background-color: var(--c-red);
      }
    }
    &.tab2 {
      &:hover,
      &:focus-visible {
        & span {
          background-color: var(--c-green);
        }
      }

      &.active {
        background-color: var(--c-green);
      }
    }
    &.tab3 {
      &:hover,
      &:focus-visible {
        & span {
          background-color: var(--c-purple);
        }
      }

      &.active {
        background-color: var(--c-purple);
      }
    }
  }

  .roadmap__tab-title {
    font-family: 'Barlow Condensed', 'sans-serif';
    font-size: var(--fs-title);
  }

  .roadmap__content {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
  }

  .roadmap__title {
    font-size: var(--fs-title--large);
    transition: color 0.3s;

    &.tab1 {
      color: var(--c-red);
    }
    &.tab2 {
      color: var(--c-green);
    }
    &.tab3 {
      color: var(--c-purple);
    }
  }

  .roadmap__introduction {
    text-align: justify;
  }

  .roadmap__steps {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    counter-set: steps 0;
    
    & a {
      position: relative;
      text-decoration: none;

      &:hover,
      &:focus-visible {
        & h3 {
          padding-inline: 7.5rem 1rem;
        }
      }
    }

    & h3 {
      position: relative;
      font-weight: var(--fw--bold);
      height: 5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-inline: 6.5rem 2rem;
      transition: padding 0.3s;

      counter-increment: steps;
      &::before {
        content: counter(steps, decimal-leading-zero)'.';
        position: absolute;
        top: 0;
        left: 0;
        width: 5rem;
        height: 5rem;
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--c-background);
      }
    }

    & .arrow {
      display: inline-block;
      width: 1.5rem;
      height: 2px;
      position: relative;

      &::before,
      &::after {
        content: '';
        position: absolute;
        width: 0.75rem;
        height: 2px;
        right: -3.5px;
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

    & .roadmap__steps-background {
      position: absolute;
      width: 100%;
      height: 100%;
      left: 0;
      top: 0;
      opacity: 0.2;
      z-index: -1;
    }

    & li {
      &:nth-child(6n+1) {
        & h3 {
          color: var(--c-red);
          box-shadow: inset var(--c-red) 0 -2px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .roadmap__steps-background {
          background-color: var(--c-red);
        }
      }
      &:nth-child(6n+2) {
        & h3 {
          color: var(--c-green);
          box-shadow: inset var(--c-green) 0 -2px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .roadmap__steps-background {
          background-color: var(--c-green);
        }
      }
      &:nth-child(6n+3) {
        & h3 {
          color: var(--c-blue);
          box-shadow: inset var(--c-blue) 0 -2px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .roadmap__steps-background {
          background-color: var(--c-blue);
        }
      }
      &:nth-child(6n+4) {
        & h3 {
          color: var(--c-purple);
          box-shadow: inset var(--c-purple) 0 -2px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .roadmap__steps-background {
          background-color: var(--c-purple);
        }
      }
      &:nth-child(6n+5) {
        & h3 {
          color: var(--c-pink);
          box-shadow: inset var(--c-pink) 0 -2px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .roadmap__steps-background {
          background-color: var(--c-pink);
        }
      }
      &:nth-child(6n+6) {
        & h3 {
          color: var(--c-text);
          box-shadow: inset var(--c-text) 0 -2px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .roadmap__steps-background {
          background-color: var(--c-text);
        }
      }
    }
  }
</style>