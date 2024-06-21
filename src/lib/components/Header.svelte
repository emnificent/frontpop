<script>
  // ignore ce script
  import logo from '$lib/images/frontpop_white_logo.png';
</script>

<header class="header">
  <nav class="header__nav">
    <a href="/"><img src="{logo}" alt="logo du nouveau front populaire" class="header__nav-home"></a>

    <div class="header__nav--group">
      <menu class="header__links">
        <li><a href="https://x.com/DiscordGauche" target="_blank"><i class="fa-brands fa-x-twitter"></i></a></li>
        <li><a href="https://facebook.com/discordgauche" target="_blank"><i class="fa-brands fa-facebook-f"></i></a></li>
        <li><a href="https://instagram.com/discord.barricade/" target="_blank"><i class="fa-brands fa-instagram"></i></a></li>
        <li><a href="https://youtube.com/@la_barricade/videos" target="_blank"><i class="fa-brands fa-youtube"></i></a></li>
        <li><a href="https://tiktok.com/@distok_populaire" target="_blank"><i class="fa-brands fa-tiktok"></i></a></li>
        <li><a href="https://twitch.tv/la_barricade" target="_blank"><i class="fa-brands fa-twitch"></i></a></li>
        <li><a href="https://discord.gg/barricade" target="_blank"><i class="fa-brands fa-discord"></i></a></li>
      </menu>
  
      <div class="header__nav--search">
        <input type="search" name="" id="" placeholder="Économie, justice, écologie...">
        <button><i class="fa-solid fa-magnifying-glass"></i></button>
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
    border: 2px solid var(--c-text);

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
      background-color: var(--c-background);
      border-radius: 50%;
      width: 2rem;
      aspect-ratio: 1/1;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: background-color 0.3s;
      
      & a {
        color: var(--c-text);
        transition: color 0.3s;
      }

      &:hover,
      &:focus-within {
        background-color: var(--c-text);

        & a {
          color: var(--c-background);
        }
      }
    }
  }
</style>