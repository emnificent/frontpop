<div class="colorful-bar"></div>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style>
  .colorful-bar {
    position: fixed;
    width: 100%;
    height: 2rem;
    bottom: 0;
    left: 0;
    z-index: 99999999;
    background: linear-gradient(110deg, var(--c-green) 0% 10%,
                                        var(--c-red) 10% 20%,
                                        var(--c-yellow) 20% 30%,
                                        var(--c-purple) 30% 40%,
                                        var(--c-pink) 40% 50%,
                                        var(--c-green) 50% 60%,
                                        var(--c-red) 60% 70%,
                                        var(--c-yellow) 70% 80%,
                                        var(--c-purple) 80% 90%,
                                        var(--c-pink) 90% 100%);
  }
</style>