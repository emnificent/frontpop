<aside class="step-aside-menu">
  <h2 class="step-aside-menu__title">Découvrez d'autres mesures</h2>

  <menu class="step-aside-menu__links">
    <li>
      <a href="/step">
        <h3>Faire une grande loi pour la santé<span class="arrow"></span></h3>
        <span class="step-aside-menu__links-background"></span>
      </a>
    </li>
    <li>
      <a href="/step">
        <h3>Faire une grande loi éducation<span class="arrow"></span></h3>
        <span class="step-aside-menu__links-background"></span>
      </a>
    </li>
    <li>
      <a href="/step">
        <h3>Entamer la planification écologique<span class="arrow"></span></h3>
        <span class="step-aside-menu__links-background"></span>
      </a>
    </li>
    <li>
      <a href="/step">
        <h3>Lutter contre toutes les formes de racismes, contre l'antisémitisme et l'islamophobie<span class="arrow"></span></h3>
        <span class="step-aside-menu__links-background"></span>
      </a>
    </li>
  </menu>
</aside>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .step-aside-menu {
    border: 1px solid var(--c-green);
    border-radius: 1.5rem;
    padding: 1.5rem;
    height: fit-content;
    display: flex;
    flex-direction: column;
    gap: 2.5rem;
    
    & h2, h3 {
      text-transform: initial;
    }
    
    @media screen and (width >= 768px) {
      border-radius: 2rem;
      padding: 3rem;
      gap: 3rem;
    }
    
    @media screen and (width >= 1280px) {
      width: 21.25rem;
      position: sticky;
      top: 3rem;
    }
  }

  .step-aside-menu__title {
    font-weight: var(--fw--bold);
    color: var(--c-green);
  }

  .step-aside-menu__links {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    @media screen and (width >= 768px) {
      gap: 1.5rem;
    }

    counter-set: steps 0;
    
    & a {
      position: relative;
      text-decoration: none;
      display: inline-block;
      width: 100%;

      &:hover,
      &:focus-visible {
        & .arrow {
          opacity: 1;
        }
      }
    }

    & h3 {
      position: relative;
      font-weight: var(--fw--bold);
      font-size: var(--fs-text);
      padding-block: 1rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      padding-inline: 6.5rem 1.5rem;

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

      & .arrow {
        @media screen and (width >= 1280px) {
          opacity: 0;
          transition: opacity 0.3s;
        }
      }
    }

    @media screen and (width < 768px) {
      & h3 {
        font-size: var(--fs-text--large);
        padding-left: 4.5rem;
        word-break: break-word;

        &::before {
          width: 3.5rem;
        }
      }
    }

    & .arrow {
      flex-shrink: 0;
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
        right: -3.25px;
      }
      
      &::before {
        rotate: 45deg;
        top: -3.75px;
      }

      &::after {
        rotate: -45deg;
        bottom: -3.75px;
      }
    }

    & .step-aside-menu__links-background {
      position: absolute;
      width: 100%;
      height: 100%;
      left: 0;
      top: 0;
      opacity: 0.1;
      z-index: -1;
    }

    & li {
      &:nth-child(4n+1) {
        & h3 {
          color: var(--c-red);
          box-shadow: inset var(--c-red) 0 -1px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .step-aside-menu__links-background {
          background-color: var(--c-red);
        }
      }
      &:nth-child(4n+2) {
        & h3 {
          color: var(--c-green);
          box-shadow: inset var(--c-green) 0 -1px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .step-aside-menu__links-background {
          background-color: var(--c-green);
        }
      }
      &:nth-child(4n+3) {
        & h3 {
          color: var(--c-blue);
          box-shadow: inset var(--c-blue) 0 -1px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .step-aside-menu__links-background {
          background-color: var(--c-blue);
        }
      }
      &:nth-child(4n+4) {
        & h3 {
          color: var(--c-purple);
          box-shadow: inset var(--c-purple) 0 -1px;
        }

        & h3::before,
        & .arrow,
        & .arrow::before,
        & .arrow::after,
        & .step-aside-menu__links-background {
          background-color: var(--c-purple);
        }
      }
    }
  }
</style>