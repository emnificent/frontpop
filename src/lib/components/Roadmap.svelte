<script>
	let tab = 'tab1';
  function tabSelect(event) {
    event.preventDefault();
    tab = event.currentTarget.attributes.href.value.replace('#', '');
    const tabSelectors = Array.from(document.getElementsByClassName('roadmap__tab'));
    tabSelectors.forEach(tabSelector => tabSelector.classList.remove('active'));
    document.getElementById(`selector-${tab}`).classList.add('active');
    document.getElementById('content-tab1').classList.add('hide');
    document.getElementById('content-tab2').classList.add('hide');
    document.getElementById('content-tab3').classList.add('hide');
    document.getElementById(`content-${tab}`).classList.remove('hide');
  }
</script>

<div class="roadmap">
  <nav class="roadmap__nav">
    <menu class="roadmap__tabs-container">
      <li class="roadmap__tab tab1 active" id="selector-tab1">
        <a href="#tab1" on:click={tabSelect} onclick="tabSelect()">
          <div>
            <p>15 premiers jours</p>
            <p class="roadmap__tab-title">La rupture</p>
          </div>
        </a>
        <span></span>
      </li>
      <li class="roadmap__tab tab2" id="selector-tab2">
        <a href="#tab2" on:click={tabSelect} onclick="tabSelect()">
          <div>
            <p>100 premiers jours</p>
            <p class="roadmap__tab-title">L'été des bifurcations</p>
          </div>
        </a>
        <span></span>
      </li>
      <li class="roadmap__tab tab3" id="selector-tab3">
        <a href="#tab3" on:click={tabSelect} onclick="tabSelect()">
          <div>
            <p>Les mois suivants</p>
            <p class="roadmap__tab-title">Les transformations</p>
          </div>
        </a>
        <span></span>
      </li>
    </menu>
  </nav>

  <div>
    <section class="roadmap__content" id="content-tab1">
      <h2 class="roadmap__title tab1">La rupture</h2>
      <p class="roadmap__introduction">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Error, optio laudantium architecto veniam quod iusto qui illo velit neque quas accusamus suscipit enim vitae cum earum incidunt dolores officia saepe rem, laborum nobis eos recusandae magnam corporis? Odio, quis. Vel sit quae officiis impedit repudiandae error expedita aliquam, perferendis molestiae, autem molestias dignissimos doloribus, repellat quibusdam? Reprehenderit tempora natus fugiat, ipsam sint aliquid non saepe at soluta sequi pariatur deserunt? Dolor necessitatibus incidunt harum velit nobis omnis voluptates commodi tenetur repellendus autem in neque officia amet ullam minus id deleniti doloribus, rem animi ab voluptate. Temporibus autem ipsa quis nemo rem totam sint unde iure maxime vero quidem, enim corporis laboriosam nam dolorum quia minus nostrum id ex? Non a animi dolore optio asperiores, suscipit quo dolorem ipsa ipsum atque quasi impedit earum. Maxime, necessitatibus error, officiis totam distinctio, veritatis soluta sint perferendis itaque numquam quia nam unde. Nihil, at.</p>
  
      <menu class="roadmap__steps">
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
      </menu>
    </section>
  
    <section class="roadmap__content hide" id="content-tab2">
      <h2 class="roadmap__title tab2">L'été des bifurcations</h2>
      <p class="roadmap__introduction">Passés les 15 premiers jours, une session extraordinaire s'ouvrira à l'Assemblée nationale, où les groupes du Nouveau Front Populaire sont majoritaires, puis une seconde à la rentrée, après la fin des Jeux Olympiques et Paralympiques. Le Parlement tient une place beaucoup plus importante dans le type de gouvernement promu par le Nouveau Front Populaire. Les députés sont particulièrement associés et / ou à l'initiative de 5 paquets législatifs pour amorcer les grandes bifurcations dont le pays a besoin. D'abord, à la suite des mesures d'urgence par décret, la présentation d'une grande loi permet de rattraper et d'améliorer la situation sociale des Français grandement paupérisés par 7 ans de macronisme et 3 ans d'inflation. Deux grandes lois permettront d'entamer la reconstruction des deux services publics les plus cruciaux : santé et éducation. Une loi énergie climat permettra de jeter les bases de la planification écologique. Enfin, le premier projet de loi de finances rectificative sera présenté pour abolir les privilèges des milliardaires.</p>
  
      <menu class="roadmap__steps">
        <li>
          <a href="/step">
            <div>
              <h3>Faire une grande loi pour le pouvoir d'achat</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Faire une grande loi pour la santé</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Faire une grande loi éducation</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Entamer la planification écologique</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lutter contre toutes les formes de racismes, contre l'antisémitisme et l'islamophobie</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Abolir les privilèges des milliardaires</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
      </menu>
    </section>
  
    <section class="roadmap__content hide" id="content-tab3">
      <h2 class="roadmap__title tab3">Les transformations</h2>
      <p class="roadmap__introduction">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Error, optio laudantium architecto veniam quod iusto qui illo velit neque quas accusamus suscipit enim vitae cum earum incidunt dolores officia saepe rem, laborum nobis eos recusandae magnam corporis? Odio, quis. Vel sit quae officiis impedit repudiandae error expedita aliquam, perferendis molestiae, autem molestias dignissimos doloribus, repellat quibusdam? Reprehenderit tempora natus fugiat, ipsam sint aliquid non saepe at soluta sequi pariatur deserunt? Dolor necessitatibus incidunt harum velit nobis omnis voluptates commodi tenetur repellendus autem in neque officia amet ullam minus id deleniti doloribus, rem animi ab voluptate. Temporibus autem ipsa quis nemo rem totam sint unde iure maxime vero quidem, enim corporis laboriosam nam dolorum quia minus nostrum id ex? Non a animi dolore optio asperiores, suscipit quo dolorem ipsa ipsum atque quasi impedit earum. Maxime, necessitatibus error, officiis totam distinctio, veritatis soluta sint perferendis itaque numquam quia nam unde. Nihil, at.</p>
  
      <menu class="roadmap__steps">
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
        <li>
          <a href="/step">
            <div>
              <h3>Lorem ipsum dolor sit amet.</h3>
              <p>En savoir plus<span class="arrow"></span></p>
              <span class="roadmap__steps-background"></span>
            </div>
          </a>
        </li>
      </menu>
    </section>
  </div>
</div>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
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
    border: 1px solid var(--c-text);
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
    text-transform: uppercase;
  }
    
  .roadmap__content {
    display: flex;
    flex-direction: column;
    gap: 2.5rem;

    &.hide {
      display: none;
    }
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
      display: inline-block;
      width: 100%;
    }

    & div {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 5rem;
    }

    & h3 {
      font-weight: var(--fw--bold);
      padding-block: 1rem;
      padding-left: 6.5rem;
      text-transform: initial;

      counter-increment: steps;
      &::before {
        content: counter(steps, decimal-leading-zero)'.';
        position: absolute;
        top: 0;
        left: 0;
        width: 5rem;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--c-background);
      }
    }

    & p {
      display: flex;
      align-items: center;
      gap: 0.35rem;
      margin-right: 2rem;
      font-size: var(--fs-text--small);
      white-space: nowrap;
      flex-wrap: nowrap;
      padding-block: 2px;
      border-bottom: 1px solid transparent;
      transition: border 0.3s;
    }

    & .arrow {
      flex-shrink: 0;
      display: inline-block;
      width: 1rem;
      height: 1px;
      position: relative;

      &::before,
      &::after {
        content: '';
        position: absolute;
        width: 0.5rem;
        height: 1px;
        right: -2.5px;
      }
      
      &::before {
        rotate: 45deg;
        top: -2.5px;
      }

      &::after {
        rotate: -45deg;
        bottom: -2.5px;
      }
    }

    & .roadmap__steps-background {
      position: absolute;
      width: 100%;
      height: 100%;
      left: 0;
      top: 0;
      opacity: 0.1;
      z-index: -1;
    }

    & li {
      &:nth-child(6n+1) {
        & div {
          color: var(--c-red);
          box-shadow: inset var(--c-red) 0 -1px;
        }

        & a {
          &:hover,
          &:focus-visible {
            & p {
            border-bottom: 1px solid var(--c-red);
            }
          }
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
        & div {
          color: var(--c-green);
          box-shadow: inset var(--c-green) 0 -1px;
        }

        & a {
          &:hover,
          &:focus-visible {
            & p {
            border-bottom: 1px solid var(--c-green);
            }
          }
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
        & div {
          color: var(--c-blue);
          box-shadow: inset var(--c-blue) 0 -1px;
        }

        & a {
          &:hover,
          &:focus-visible {
            & p {
            border-bottom: 1px solid var(--c-blue);
            }
          }
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
        & div {
          color: var(--c-purple);
          box-shadow: inset var(--c-purple) 0 -1px;
        }

        & a {
          &:hover,
          &:focus-visible {
            & p {
            border-bottom: 1px solid var(--c-purple);
            }
          }
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
        & div {
          color: var(--c-pink);
          box-shadow: inset var(--c-pink) 0 -1px;
        }

        & a {
          &:hover,
          &:focus-visible {
            & p {
            border-bottom: 1px solid var(--c-pink);
            }
          }
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
        & div {
          color: var(--c-text);
          box-shadow: inset var(--c-text) 0 -1px;
        }

        & a {
          &:hover,
          &:focus-visible {
            & p {
            border-bottom: 1px solid var(--c-text);
            }
          }
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