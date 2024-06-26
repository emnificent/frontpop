<main class="legal">
  <h1>Mentions légales</h1>
  <p>Le site LAEC.fr est un service de communication au public en ligne qui est édité à titre non professionnel (au sens de l'article 6, III-2 de la Loi n° 2004-575 du 21 juin 2004 pour la confiance dans l'économie numérique). En accord avec les dispositions de l'article sus-cité, l'auteur de ces lignes a donc choisi de conserver l'anonymat. Ces informations ont toutefois été transmises à l'hébergeur de ce site qui saura les délivrer à qui de droit.</p>
  <h2>Hébergeur</h2>
  <p>Le prestataire technique qui assure l'hébergement de LAEC.FR est la société OVH, dont le siège social se situe à Roubaix.<br />Société OVH, 2 rue Kellermann 59100 Roubaix<br />Téléphone : +33 8 99 70 17 61</p>
  <h2>Politique de confidentialité</h2>
  <h3>Statistiques et mesures d'audience</h3>
  <p>Nous n'utilisons pas d'outils de mesure d'audience.<br />Les logs de connexion du serveur sont conservés pour une durée de 14 jours conformément aux dispositions européennes en matière de rétention de données.</p>
  <h3>Accès aux données</h3>
  <p>Conformément à la loi Informatique et Libertés 78-17 du 6 janvier 1978 modifiée ainsi qu'au Règlement européen sur la protection des données (RGPD), vous bénéficiez d'un droit d'accès, de rectification, d'opposition et d'effacement de vos données personnelles ainsi que d'un droit à la limitation du traitement vous concernant.<br/><br/>Pour exercer ces droits ou pour toute question sur le traitement de vos données dans ce dispositif, vous pouvez contacter par courrier électronique l'adresse suivante : actions.insoumises@gmail.com.<br/><br/>Si vous estimez, après nous avoir contactés, que les droits dont vous disposez ne sont pas respectés, vous pouvez adresser une réclamation à la CNIL.</p>
  <h3>Litiges</h3>
  <p>La loi applicable au présent contrat est la loi française. Dans toute hypothèse où un choix de loi serait possible, les parties conviennent que la loi applicable est la loi française.</p>
</main>

<!-- ne copie pas le CSS depuis ici, c'est du SCSS, ça permet d'aller plus vite, mais il doit être compiler pour fonctionner correctement, tu trouveras le CSS compilé dans /styles/compiled.css -->
<style lang="scss">
  .legal {
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
    @media screen and (width >= 1520px) {
      padding: 0;
    }

    & h1 {
      font-size: var(--fs-title--large);
    }

    & h2, h3 {
      text-transform: initial;
      font-weight: var(--fw--bold);
    }

    & h3 {
      font-size: var(--fs-text);
      font-family: 'Barlow', 'sans-serif';
      line-height: 1;
    }
  }
</style>