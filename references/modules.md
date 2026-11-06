# Modules et sources à consulter

## SEO technique — SEO-T
- Vérifier codes HTTP, erreurs réelles et soft 404, chaînes/boucles de redirection, HTTPS, variantes d’hôte, robots.txt, sitemap, canonical, noindex, en-têtes X-Robots-Tag, pagination, facettes et hreflang si pertinent.
- Séparer explorabilité, indexabilité et indexation constatée. Un robots.txt restrictif ne garantit pas une désindexation ; ne pas proposer de bloquer l’exploration nécessaire à la lecture de noindex.
- Comparer HTML initial et rendu JavaScript ; vérifier liens explorables, contenu essentiel et ressources bloquées. Rechercher doublons et pages orphelines seulement si le corpus permet cette conclusion.
- Pour un projet, examiner routes, configuration par environnement, templates et génération des URL. Ne pas prendre le noindex d’un environnement de développement pour une erreur de production.
- Examiner données structurées : syntaxe, adéquation au contenu visible, propriétés du type et conditions Google. Séparer validité Schema.org et éligibilité aux résultats enrichis, sans garantie d’affichage.
- Examiner les versions des technologies et les risques de faille de sécurités, Version du CMS, Version LTS, CVE connue.
- Sources : https://developers.google.com/search/docs/essentials ; https://developers.google.com/search/docs/crawling-indexing ; https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data ; https://schema.org/docs/schemas.html

## SEO éditorial, GEO et visibilité — SEO-C
- Évaluer intention de recherche, utilité, précision, originalité, sources, fraîcheur pertinente, titres descriptifs, descriptions, hiérarchie de titres, maillage, ancres et alternatives d’images selon leur fonction.
- Évaluer l'autorité du domaine et des pages DA. Évaluer le nombre de Backlink.
- Utiliser longueurs de titres/descriptions comme repères de présentation, jamais comme normes absolues. Ne pas imposer densité de mots-clés, balise meta keywords ou nombre unique de H1 comme facteurs garantis de classement.
- Identifier cannibalisation potentielle et contenu faible à partir de preuves ; ne pas conclure automatiquement à une pénalité.
- Évaluer transparence de l’auteur et confiance selon le contexte ; ne pas inventer un score E-E-A-T officiel.
- Si les accès existent, analyser Search Console et statistiques : période, pays, appareil, requêtes, impressions, clics, CTR et positions. Sans accès, marquer ces données indisponibles. Pour les backlinks, nommer la source et les limites de couverture ; ne pas supposer l’absence de liens.
- Pour moteurs IA, privilégier contenu accessible, vérifiable et structuré ; distinguer observation et hypothèse. Ne pas garantir de citations et ne pas présenter llms.txt comme exigence de Google ou norme établie.
- Sources : https://developers.google.com/search/docs/fundamentals/creating-helpful-content ; https://developers.google.com/search/docs/appearance/title-link ; https://developers.google.com/search/docs/appearance/snippet ; https://developers.google.com/search/docs/appearance/ai-features ; https://ahrefs.com/keyword-generator ; https://www.bing.com/webmasters/help/webmaster-guidelines-30fba23a ; https://blogs.bing.com/webmaster/2014/6/How-Does-Bing-Choose-The-Title-For-My-Web-Page/ ; https://blogs.bing.com/webmaster/2020/4/Announcing-new-options-for-webmasters-to-control-their-snippets-at-Bing/ ; https://www.bing.com/webmasters/help/new-ai-preferences-2t1cc16d ; https://moz.com/domain-analysis ; https://ahrefs.com/website-authority-checker ; https://ahrefs.com/backlink-checker

## Performance et mobile — PERF
- Mesurer avec Lighthouse local ou PageSpeed Insights si accessible ; noter URL, date, profil mobile/desktop, environnement et version. Si mesures instables, répéter et expliquer la dispersion.
- Distinguer CrUX terrain (période, URL/origine, appareil, disponibilité) et laboratoire. Ne pas présenter TBT comme INP mesuré, ni un score Lighthouse comme conformité ou positionnement.
- Vérifier les seuils courants dans les sources ; repères initiaux « bons » au 75e percentile : LCP ≤ 2,5 s, INP ≤ 200 ms, CLS ≤ 0,1. Signaler les données terrain insuffisantes.
- Examiner images responsives et dimensions, formats, polices, CSS/JS, cache, compression, ressources bloquantes, scripts tiers et réactivité mobile. Ne pas appliquer lazy-loading à l’image LCP sans justification.
- Sources : https://web.dev/articles/vitals ; https://developers.google.com/speed/docs/insights/v5/about ; https://developer.chrome.com/docs/lighthouse/overview ; https://gtmetrix.com/ ;

## Conformité HTML et CSS — HTML
- Exécuter Nu Html Checker sur HTML final public ou local ; distinguer erreurs et avertissements. Inclure URL/état, ligne ou extrait, diagnostic et correction. Revalider les documents corrigés.
- Inspecter sémantique, imbrication, attributs, identifiants et ARIA ; ne pas attribuer à un validateur des tests qu’il n’a pas réalisés. Éviter les diagnostics obsolètes sur les technologies modernes.
- Vérifier CSS avec le service W3C ou outil équivalent si disponible ; préciser profil et limites concernant les fonctionnalités récentes. Séparer avertissement de compatibilité et erreur normative.
- Ne pas confondre HTML valide et respect de toutes les normes frontend, sécurité ou accessibilité.
- Sources : https://validator.w3.org/nu/ ; https://validator.w3.org/docs/users.html ; https://validator.nu/ ; https://html.spec.whatwg.org/ ; https://jigsaw.w3.org/css-validator/

## Accessibilité — A11Y
- Lire la recommandation WCAG cible et sa liste complète des critères A/AA. Construire la matrice des critères applicables ; couvrir chaque critère ou le marquer non testé/non applicable avec justification. Identifier explicitement la couverture automatisée et manuelle.
- Lire la recommandation RGAA cible et sa liste complète des critères ; couvrir chaque critère ou le marquer non testé/non applicable avec justification. Identifier explicitement la couverture automatisée et manuelle.
- Exécuter axe-core sur plusieurs pages et états : menus, modales, erreurs de formulaire et contenu dynamique. Distinguer violations, points nécessitant revue et contrôles passés. Ne pas compter « incomplete » comme conforme.
- Vérifier manuellement clavier, ordre/focus visible/non masqué, absence de pièges, lien d’évitement, menus et modales, restitution des noms/rôles/états, annonces dynamiques, labels/instructions/erreurs, langue, titres, liens, structure, tableaux, alternatives pertinentes et médias.
- Contrôler contraste texte et éléments UI, zoom 200 %, redistribution à 320 pixels CSS, espacement du texte, orientation, mouvements, flashs, alternatives aux gestes et au glisser-déposer, taille des cibles, authentification accessible et saisies redondantes. Appliquer les exceptions exactes du critère, sans réduire la vérification à cette liste.
- Examiner tous les états concernés et les parcours complets ; tester au lecteur d’écran si disponible en nommant navigateur/technologie d’assistance. Sinon signaler ce contrôle non effectué.
- Ne pas réintroduire le critère 4.1.1 supprimé de WCAG 2.2 comme obligation de ce référentiel. Conserver la validité HTML dans son propre module.
- Ne pas publier de déclaration de conformité sur la seule base d’un audit partiel. Pour une demande RGAA ou juridique, vérifier séparément le référentiel et son champ applicable.
- Sources : https://www.w3.org/TR/WCAG22/ ; https://www.w3.org/WAI/WCAG22/quickref/ ; https://www.w3.org/WAI/test-evaluate/ ; https://www.w3.org/TR/wai-aria-practices/ ; https://github.com/dequelabs/axe-core;  https://webaim.org/resources/contrastchecker/ ; https://accessibilite.numerique.gouv.fr/ ; https://rgaa-checker.com/

## Contrat d’extension
Pour chaque ajout demandé, définir un préfixe stable, les déclencheurs et exclusions, le référentiel daté, les données/outils nécessaires, les contrôles et preuves, les limites, les recommandations et les tests de correction. Charger le module seulement lorsqu’il est pertinent. Conserver les résultats non comparables séparés.
