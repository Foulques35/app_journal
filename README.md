🏗️ Journal de Chantier - PWA iOS Offline
Une application web mobile (PWA) ultra-légère pour le suivi de chantier. Conçue pour fonctionner sans connexion internet, sans serveur, et sans abonnement. Elle permet de créer des fiches de suivi, d'ajouter des photos et de générer des rapports PDF instantanément depuis un iPhone.

✨ Fonctionnalités
100% Hors Ligne : Fonctionne parfaitement en mode avion grâce aux Service Workers.

Stockage Grande Capacité : Utilise IndexedDB (pas de limite de 5Mo), permettant de stocker des centaines de fiches et photos.

Rapports PDF : Génération de rapports PDF professionnels directement sur le téléphone (via jsPDF).

Photos illimitées : Ajout de photos avec redimensionnement automatique pour optimiser l'espace.

Suivi Chronologique : Historique des interventions (timeline) pour chaque chantier.

Données Locales : Vos données restent sur votre téléphone. Rien n'est envoyé dans le cloud.

Sauvegarde : Système d'export/import JSON complet pour sécuriser vos données.

📂 Structure du projet
Pour que l'application fonctionne, le dossier doit contenir impérativement ces 3 fichiers :

index.html : Le code principal de l'application (HTML/JS/CSS).

sw.js : Le Service Worker qui gère le mode hors ligne (mise en cache).

jspdf.umd.min.js : La librairie pour générer les PDF (hébergée localement pour le offline).

🚀 Installation & Hébergement
Pas besoin de serveur complexe. Un simple hébergement de fichiers statiques suffit (GitHub Pages ou Netlify Drop).

Option A : Via Netlify Drop (Recommandé)
Mettez les 3 fichiers (index.html, sw.js, jspdf.umd.min.js) dans un dossier sur votre ordinateur.

Glissez-déposez ce dossier sur Netlify Drop.

C'est en ligne ! Notez l'URL sécurisée (https://...).

Option B : Via GitHub Pages
Activez "GitHub Pages" dans les réglages de votre dépôt (Settings > Pages).

Choisissez la branche main comme source.

📱 Installation sur iPhone (App Native)
Pour transformer le site web en application "native" qui fonctionne hors ligne :

Ouvrez Safari sur votre iPhone.

Allez sur l'URL de votre site (ex: https://mon-journal.netlify.app).

Appuyez sur le bouton Partage (carré avec une flèche vers le haut).

Cherchez et appuyez sur "Sur l'écran d'accueil".

Validez.

Une icône apparaît sur votre écran. L'application se lancera désormais en plein écran, sans barre d'adresse, et fonctionnera même sans réseau.

⚠️ Sécurité des Données (Important)
Cette application fonctionne en Local First. Cela signifie que toutes les données sont stockées dans la mémoire de votre navigateur (Safari).

Pas de Cloud : Si vous perdez votre téléphone ou si vous le cassez, les données sont perdues (sauf si vous avez fait une sauvegarde).

Nettoyage Safari : Évitez de faire "Effacer historique et données de site" dans les réglages de Safari sans avoir sauvegardé avant.

🛡️ Procédure de sauvegarde recommandée
Allez régulièrement dans l'application.

Cliquez sur le bouton Partage/Export (en haut à droite).

Choisissez "Sauvegarde JSON".

Enregistrez le fichier généré dans vos Fichiers (iCloud Drive) ou envoyez-le vous par email.

Pour restaurer vos données sur un nouveau téléphone, utilisez le bouton "Restaurer Sauvegarde" dans le même menu.

🛠️ Stack Technique
Langages : HTML5, CSS3, Vanilla JavaScript (ES6+).

Stockage : IndexedDB (via wrapper asynchrone natif).

Offline : Service Worker (Cache Storage API).

PDF : jsPDF (version UMD locale).

📄 Licence
Projet sous licence MIT. Libre d'utilisation et de modification. Créé par Maxime Bousquet.
