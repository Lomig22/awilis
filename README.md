# 🚀 Awilis - Site Web Premium SEO & IA

Site web ultra design pour une agence de référencement SEO & Intelligence Artificielle, conçu avec les meilleures pratiques de développement web moderne.

## ✨ Caractéristiques

### Design & UX
- **Design premium & moderne** avec animations subtiles et fluides
- **Palette de couleurs sophistiquée** : bleu électrique, violet, vert accent
- **Typographies élégantes** : Inter + Poppins
- **Gradients soft** et formes abstraites
- **Micro-animations** au hover et au scroll
- **100% Responsive** - Mobile-first design
- **Dark mode compatible** sur sections spécifiques

### Performance
- **HTML5 sémantique** pour un SEO optimal
- **CSS moderne** avec variables CSS (Custom Properties)
- **JavaScript vanilla** optimisé (pas de framework lourd)
- **Animations GPU-accelerated** avec transforms
- **Lazy loading** compatible
- **Optimisé Core Web Vitals**

### Fonctionnalités
- ✅ Navigation sticky avec effet de transparence
- ✅ Menu mobile hamburger animé
- ✅ Smooth scroll entre sections
- ✅ Compteurs animés au scroll
- ✅ Carrousel de témoignages avec swipe mobile
- ✅ Formulaire de contact validé
- ✅ Indicateur de scroll
- ✅ Animations au scroll (AOS)
- ✅ Tracking analytics (Google Analytics + Meta Pixel ready)

## 📁 Structure du Projet

```
awilis-main/
├── index.html          # Structure HTML principale
├── styles.css          # Styles CSS avec design system
├── script.js           # JavaScript pour interactions
└── README.md           # Documentation (ce fichier)
```

## 🎨 Design System

### Couleurs Principales
```css
--color-primary: #6366F1        /* Bleu électrique */
--color-secondary: #8B5CF6      /* Violet */
--color-accent: #10B981         /* Vert */
--color-gray-900: #1A1F2E       /* Anthracite */
--color-white: #FFFFFF          /* Blanc pur */
```

### Typographies
- **Titres** : Poppins (Bold, 700-800)
- **Corps de texte** : Inter (Normal, 400-600)
- **Échelle** : 12px → 72px (responsive)

### Espacements
- Mobile : 16px base
- Desktop : 24px base
- Sections : 96px padding vertical

### Border Radius
- Petit : 6px
- Moyen : 12px
- Large : 24px
- Full : 9999px (boutons pill)

## 🚀 Installation & Démarrage

### Option 1 : Ouvrir directement
Simplement ouvrir `index.html` dans un navigateur moderne.

### Option 2 : Serveur local (recommandé)
```bash
# Avec Python 3
python3 -m http.server 8000

# Avec Node.js (http-server)
npx http-server -p 8000

# Avec PHP
php -S localhost:8000
```

Puis visiter : `http://localhost:8000`

## 📦 Dépendances

### CDN Utilisés
- **AOS (Animate On Scroll)** : 2.3.1
  - Animations au scroll
  - https://unpkg.com/aos@2.3.1/dist/aos.js
  
- **Google Fonts** :
  - Inter (300, 400, 500, 600, 700, 800, 900)
  - Poppins (400, 500, 600, 700, 800)

### Aucune Installation Requise
Le site fonctionne sans `npm install` ou gestionnaire de paquets. Toutes les dépendances sont chargées via CDN.

## 🎯 Sections du Site

1. **Hero Section**
   - Titre accrocheur avec gradient
   - 2 CTA principaux
   - Statistiques clés
   - Animation de fond avec orbes

2. **Pourquoi Awilis**
   - 3 cartes : Problème / Solution / Bénéfices
   - Card centrale mise en avant
   - Icons SVG personnalisés

3. **Services SEO & IA**
   - 4 services détaillés
   - Cards avec hover effects
   - Liste de features par service
   - CTA sur chaque card

4. **Processus / Méthodologie**
   - Timeline verticale à 4 étapes
   - Animation des numéros
   - Livrables par étape
   - Alternance gauche/droite

5. **Résultats**
   - Compteurs animés
   - 4 KPIs principaux
   - Mini cas clients
   - Fond dark pour contraste

6. **Témoignages**
   - Carrousel avec 4 témoignages
   - Navigation prev/next
   - Dots indicator
   - Swipe mobile
   - Auto-play (5s)

7. **CTA / Contact**
   - Formulaire 5 champs
   - Validation front-end
   - Message de succès
   - Orbes animés en fond

8. **Footer**
   - 4 colonnes responsive
   - Réseaux sociaux
   - Liens utiles
   - Coordonnées complètes

## ⚙️ Configuration

### Intégration Google Analytics
Ajouter avant `</head>` dans `index.html` :
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Intégration Meta Pixel
Ajouter avant `</head>` dans `index.html` :
```html
<!-- Meta Pixel Code -->
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'YOUR_PIXEL_ID');
  fbq('track', 'PageView');
</script>
```

### Intégration Formulaire Backend

#### Option A : EmailJS (gratuit)
1. Créer un compte sur [emailjs.com](https://www.emailjs.com/)
2. Ajouter le SDK avant `</body>` :
```html
<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
<script>
  emailjs.init('YOUR_PUBLIC_KEY');
</script>
```
3. Modifier la fonction `initFormHandling()` dans `script.js`

#### Option B : Netlify Forms
1. Ajouter `data-netlify="true"` au formulaire
2. Ajouter un input hidden :
```html
<input type="hidden" name="form-name" value="contact" />
```

#### Option C : Votre propre API
Modifier la partie `setTimeout()` dans `initFormHandling()` avec :
```javascript
fetch('https://votre-api.com/contact', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(formData)
})
.then(response => response.json())
.then(data => {
  showNotification('Merci !', 'success');
  contactForm.reset();
})
.catch(error => {
  showNotification('Erreur', 'error');
});
```

## 🎨 Personnalisation

### Changer les Couleurs
Modifier les variables CSS dans `styles.css` :
```css
:root {
    --color-primary: #6366F1;     /* Votre couleur */
    --color-secondary: #8B5CF6;   /* Votre couleur */
    --color-accent: #10B981;      /* Votre couleur */
}
```

### Changer les Typographies
Modifier dans `styles.css` :
```css
:root {
    --font-primary: 'VotreFontCorps', sans-serif;
    --font-display: 'VotreFontTitre', sans-serif;
}
```
Et ajouter le lien Google Fonts dans `index.html`.

### Modifier le Contenu
Tout le contenu est dans `index.html`. Recherchez les sections par leur ID :
- `#home` - Hero
- `#why` - Pourquoi Awilis
- `#services` - Services
- `#process` - Processus
- `#results` - Résultats
- `#testimonials` - Témoignages
- `#contact` - Contact

## 🌐 SEO On-Page

Le site est optimisé pour le SEO :
- ✅ Balises meta complètes
- ✅ Open Graph (Facebook)
- ✅ Twitter Cards
- ✅ Structure HTML5 sémantique
- ✅ Headings hiérarchisés (H1 → H6)
- ✅ Alt text sur images (à ajouter)
- ✅ Aria labels pour accessibilité
- ✅ Schema.org ready (à implémenter)

### Ajouter Schema.org
Ajouter dans `<head>` :
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "name": "Awilis",
  "description": "Agence SEO & IA Premium",
  "url": "https://www.awilis.ai",
  "telephone": "+33-1-23-45-67-89",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Paris",
    "addressCountry": "FR"
  }
}
</script>
```

## 📱 Responsive Breakpoints

```css
/* Mobile : < 640px (défaut) */
/* Tablet : 641px - 968px */
@media (max-width: 968px) { ... }

/* Desktop : > 969px */
@media (min-width: 969px) { ... }
```

## ♿ Accessibilité

- ✅ Navigation au clavier
- ✅ Aria labels
- ✅ Contraste élevé (WCAG AA)
- ✅ Focus visible
- ✅ Skip links
- ✅ Alt text (à compléter avec images)

## 🚀 Déploiement

### Netlify (recommandé)
1. Créer un compte sur [netlify.com](https://www.netlify.com)
2. Drag & drop le dossier `awilis-main`
3. Le site est en ligne ! 🎉

### Vercel
```bash
npm i -g vercel
vercel
```

### GitHub Pages
1. Push le code sur GitHub
2. Settings → Pages → Source: main branch
3. Le site est en ligne !

### Hébergement classique
Upload via FTP sur votre hébergeur :
- OVH
- O2Switch
- Hostinger
- etc.

## 📊 Performance

### Scores attendus :
- **Lighthouse Performance** : 95-100
- **Lighthouse Accessibility** : 95-100
- **Lighthouse Best Practices** : 95-100
- **Lighthouse SEO** : 95-100

### Optimisations possibles :
- Minifier CSS/JS pour production
- Optimiser/compresser les images
- Ajouter Service Worker (PWA)
- Lazy load images
- Preload fonts critiques

## 🛠️ Technologies Utilisées

- **HTML5** - Structure sémantique
- **CSS3** - Design moderne avec Custom Properties
- **JavaScript ES6+** - Interactions
- **AOS** - Animations au scroll
- **Google Fonts** - Typographies
- **SVG** - Icons & illustrations

## 📝 Licence

Ce projet est créé pour Awilis. Tous droits réservés.

## 💬 Support

Pour toute question ou assistance :
- 📧 Email : contact@awilis.ai
- 📱 Téléphone : +33 1 23 45 67 89
- 🌐 Site : [www.awilis.ai](https://www.awilis.ai)

## 🎯 Prochaines Étapes

### Améliorations Suggérées
1. **Ajouter un blog**
   - Section articles SEO
   - CMS headless (Contentful, Strapi)
   
2. **Dashboard Client**
   - Espace client sécurisé
   - Suivi des KPIs en temps réel
   
3. **Calculateur ROI**
   - Outil interactif
   - Estimation gains SEO
   
4. **Chat en direct**
   - Crisp, Intercom ou Drift
   - Support temps réel
   
5. **Multi-langue**
   - Version EN
   - i18n implementation

6. **Visuels personnalisés**
   - Photos d'équipe
   - Illustrations custom
   - Logos clients

7. **Certificats & Awards**
   - Google Partner
   - Certifications
   - Récompenses

---

**Développé avec ❤️ et expertise pour Awilis**

🚀 **Prêt à dominer Google !**
