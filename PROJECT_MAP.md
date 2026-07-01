# PROJECT MAP - Portfolio Aymane Ayyadi

## TECH_STACK
- **HTML5** - Structure sémantique
- **CSS3** - Styles personnalisés (Style.css)
- **Tailwind CSS** (CDN) - Framework utilitaire CSS
- **Font Awesome 6** - Icônes
- **JavaScript (Vanilla)** - Animations, interactions, WebGL
- **WebGL 2** - Animation Lightfall (hero)

## STRUCTURE
```
index.html              → Page principale (single-page)
mentions-legales.html   → Page des mentions légales
Style.css               → Tous les styles (dark/light mode)
PROJECT_MAP.md          → Documentation du projet
Conception/             → Assets (images, PDF, favicon)
```

## FONCTIONNALITÉS INTERACTIVES

### Corrections appliquées
- **React & OGL supprimés** - Libs chargées mais jamais utilisées (gain de poids)
- **CSS `.header` dupliqué** - Fusionné en une seule définition propre
- **CSS `.logo-fallback`** - `display: none` par défaut, `display: flex` seulement quand l'image est absente
- **Navigation mobile ajoutée** - Menu hamburger avec overlay animé
- **Lien Mentions légales** - Masqué sur tablette (`hidden lg:inline`) pour éviter le débordement

### Nouvelles animations (fluides & dynamiques)
1. **Barre de progression** - Fine ligne dégradée en haut de page qui se remplit au scroll
2. **Menu mobile** - Hamburger avec animation en croix + overlay avec entrée staggered des liens
3. **Effet 3D Tilt** - Les cartes (projets, certificats, centres d'intérêt) suivent la souris en 3D
4. **Boutons magnétiques** - Les icônes sociales LinkedIn/Github suivent la souris
5. **Curseur de machine à écrire** - Barre clignotante `|` après le titre du hero
6. **Accessibilité** - `prefers-reduced-motion` supporté (désactive les animations)

### Fonctionnalités existantes conservées
- **Scroll animations** - IntersectionObserver + classes CSS (`scroll-animate`)
- **Theme toggle** - Dark/Light mode avec localStorage
- **Custom cursor** - Cercle avec point qui suit la souris
- **Lightfall WebGL** - Animation de particules hero
- **Typewriter** - Texte d'accueil animé (amélioré avec curseur)
- **Navigation active** - Surlignage selon section visible
- **Modal PDF** - Visualisation des attestations
- **Scrollbar personnalisée** - Thème bleu/violet

### Problèmes connus (inchangés)
- Certains chemins de fichiers PDF contiennent des espaces (ex: `Attestation%20de%20stage...`)
- Les images Unsplash sont chargées depuis l'URL directe (pas de fallback local)

## SECTIONS (index.html)
1. **Accueil** - Hero avec WebGL + typewriter
2. **Profil** - Photo + description + cartes BTS SIO/SISR/SLAM
3. **Centres d'intérêt** - Grille 3 cartes (Karaté, Gaming, Veille)
4. **Parcours** - Timeline responsive 4 étapes
5. **Projets** - 3 cartes projet (AP2, AP3, AP4) avec overlays
6. **Epreuve E5** - Tableau de synthèse + attestations (modal PDF)
7. **Epreuve E6** - Dossier réalisations PDF
8. **Certificats** - 3 certificats Microsoft Learn
9. **Veille** - Article pédagogique + sources (CNIL)
10. **Contact** - Téléphone + Email
11. **Footer** - Liens sociaux + mentions légales
