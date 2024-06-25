<script>
  // ignore ce script
  import logo from '$lib/images/frontpop_white_logo.png';
</script>

<footer class="footer">
  <nav class="footer__nav">
    <a href="/"><img src="{logo}" alt="logo du nouveau front populaire" class="footer__nav-home"></a>

    <menu class="footer__links">
      <li><a href="https://x.com/DiscordGauche" target="_blank"><i class="fa-brands fa-x-twitter"></i><span class="footer__links-background"></span></a></li>
      <li><a href="https://facebook.com/discordgauche" target="_blank"><i class="fa-brands fa-facebook-f"></i><span class="footer__links-background"></span></a></li>
      <li><a href="https://instagram.com/discord.barricade/" target="_blank"><i class="fa-brands fa-instagram"></i><span class="footer__links-background"></span></a></li>
      <li><a href="https://youtube.com/@la_barricade/videos" target="_blank"><i class="fa-brands fa-youtube"></i><span class="footer__links-background"></span></a></li>
      <li><a href="https://tiktok.com/@distok_populaire" target="_blank"><i class="fa-brands fa-tiktok"></i><span class="footer__links-background"></span></a></li>
      <li><a href="https://twitch.tv/la_barricade" target="_blank"><i class="fa-brands fa-twitch"></i><span class="footer__links-background"></span></a></li>
      <li><a href="https://discord.gg/barricade" target="_blank"><i class="fa-brands fa-discord"></i><span class="footer__links-background"></span></a></li>
    </menu>
    
    <a href="/legal" class="footer__legal">Mentions légales</a>
  </nav>
</footer>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .footer {
    background-color: var(--c-text);
    margin-bottom: 2rem;
    /* margin-top + global to put footer where it belongs */
    margin-top: auto;
  }

  :global(body) {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    overflow-x: hidden;
  }

  .footer__nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: var(--bp-desktop--large);
    margin: auto;
    display: grid;
    grid-template: auto / repeat(3, 1fr);

    & > * {
      margin-inline: auto;

      &:first-child {
        margin-left: 0;
      }

      &:last-child {
        margin-right: 0;
      }
    }
  }

  .footer__nav-home {
    height: var(--fs-title--large);
    padding-block: 1.5rem;
  }

  .footer__links {
    display: flex;
    gap: 1.5rem;
    
    & li {
      position: relative;
      overflow: hidden;
      background-color: transparent;
      border-radius: 50%;
      width: 2rem;
      aspect-ratio: 1/1;
      display: flex;
      justify-content: center;
      align-items: center;
      
      & a {
        color: var(--c-text);
        z-index: 0;

        &:hover,
        &:focus-visible {
          & .footer__links-background {
            opacity: 0.8;
          }
        }
      }
    }
  }

  .footer__links-background {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background-color: var(--c-background);
    z-index: -1;
    transition: opacity 0.3s;
  }

  .footer__legal {
    color: var(--c-background);
    text-decoration: underline solid transparent 1px;
    transition: text-decoration-color 0.3s;

    &:hover,
    &:focus-visible {
      text-decoration-color: var(--c-background);
    }
  }
</style>