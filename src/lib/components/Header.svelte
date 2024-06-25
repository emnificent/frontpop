<script>
  // ignore ce script
  import logo from '$lib/images/frontpop_white_logo.png';
</script>

<header class="header">
  <nav class="header__nav">
    <a href="/"><img src="{logo}" alt="logo du nouveau front populaire" class="header__nav-home"></a>

    <a href="/programme" class="header__nav-main">Le programme</a>

    <div class="header__nav--group">
      <menu class="header__links">
        <li><a href="https://x.com/DiscordGauche" target="_blank"><i class="fa-brands fa-x-twitter"></i><span class="header__links-background"></span></a></li>
        <li><a href="https://facebook.com/discordgauche" target="_blank"><i class="fa-brands fa-facebook-f"></i><span class="header__links-background"></span></a></li>
        <li><a href="https://instagram.com/discord.barricade/" target="_blank"><i class="fa-brands fa-instagram"></i><span class="header__links-background"></span></a></li>
        <li><a href="https://youtube.com/@la_barricade/videos" target="_blank"><i class="fa-brands fa-youtube"></i><span class="header__links-background"></span></a></li>
        <li><a href="https://tiktok.com/@distok_populaire" target="_blank"><i class="fa-brands fa-tiktok"></i><span class="header__links-background"></span></a></li>
        <li><a href="https://twitch.tv/la_barricade" target="_blank"><i class="fa-brands fa-twitch"></i><span class="header__links-background"></span></a></li>
        <li><a href="https://discord.gg/barricade" target="_blank"><i class="fa-brands fa-discord"></i><span class="header__links-background"></span></a></li>
      </menu>
  
      <div class="header__nav--search">
        <input type="search" name="" id="" placeholder="Économie, justice, écologie...">
        <button aria-label="lancer la recherche"><i class="fa-solid fa-magnifying-glass"></i></button>
      </div>
    </div>
  </nav>
</header>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .header {
    background-color: var(--c-red);
  }

  .header__nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: var(--bp-desktop--large);
    margin: auto;
  }

  .header__nav-home {
    height: var(--fs-title--large);
    padding-block: 1.5rem;
  }

  .header__nav-main {
    font-weight: var(--fw--bolder);
    color: var(--c-background);
    text-decoration: none;
    padding-block: 0.25rem;
    border-bottom: 1px solid transparent;
    transition: border 0.3s;

    &:hover,
    &:focus-visible {
      border-bottom: 1px solid var(--c-background);
    }
  }

  .header__nav--group {
    display: flex;
    gap: 1.5rem;
    align-items: center;
  }

  .header__nav--search {
    display: flex;
    gap: 1rem;
    background-color: var(--c-background);
    border-radius: 0.5rem;
    overflow: hidden;
    padding: 0.5rem 1.5rem;
    border: 1px solid var(--c-text);

    & input {
      background-color: transparent;
      color: var(--c-text);
      width: 13.5rem;
      border: transparent;
      outline: transparent;
      font-size: var(--fs-text--small);
    }

    & button {
      border: transparent;
      background-color: transparent;
      opacity: 0.5;
      transition: opacity 0.3s;

      &:hover,
      &:focus-visible {
        opacity: 1;
      }
    }
  }

  .header__links {
    display: flex;
    gap: 1.5rem;
    
    & li {
      position: relative;
      overflow: hidden;
      border-radius: 50%;
      width: 2rem;
      aspect-ratio: 1/1;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: transparent;
      
      & a {
        color: var(--c-text);
        z-index: 0;

        &:hover,
        &:focus-visible {
          & .header__links-background {
            opacity: 0.8;
          }
        }
      }
    }
  }
  
  .header__links-background {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background-color: var(--c-background);
    z-index: -1;
    transition: opacity 0.3s;
  }
</style>