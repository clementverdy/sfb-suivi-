# SFB — Suivi d'équipe (version web indépendante)

Cette version fonctionne exactement comme l'artefact Claude que tu utilisais, mais elle est maintenant connectée à ta propre base de données Supabase — plus de bug de sauvegarde côté Claude, et un vrai lien permanent à partager avec ton staff.

## ✅ Déjà fait
- La base de données Supabase est créée et connectée dans le code (`src/App.jsx`).
- Toutes les fonctionnalités sont identiques : joueurs, séances, match en direct avec paliers de charge, statistiques, suivi joueur avec vue coach protégée, blessures, gestion multi-équipes (R1/U19), export/import.

## 🚀 Étape suivante : mettre le code sur GitHub

1. Va sur **[github.com](https://github.com)** et crée un compte gratuit si tu n'en as pas.
2. Clique sur **"New repository"** (bouton vert).
3. Nomme-le `sfb-suivi`, laisse-le en **Public** ou **Private** (au choix), ne coche aucune case supplémentaire.
4. Clique sur **"Create repository"**.
5. Sur la page suivante, clique sur **"uploading an existing file"**.
6. Glisse-dépose **tous les fichiers de ce dossier** (garde bien la structure : `src/`, `public/`, `package.json`, etc.) dans la zone d'upload.
7. Clique sur **"Commit changes"** en bas.

## 🌐 Étape suivante : déployer sur Vercel (gratuit)

1. Va sur **[vercel.com](https://vercel.com)** et crée un compte gratuit avec **"Continue with GitHub"** (le même compte que ci-dessus, ça simplifie tout).
2. Clique sur **"Add New..." → "Project"**.
3. Trouve le dépôt `sfb-suivi` que tu viens de créer et clique sur **"Import"**.
4. Vercel détecte automatiquement que c'est un projet Vite/React — ne change aucun réglage.
5. Clique sur **"Deploy"**.
6. Attends 1-2 minutes — tu obtiens une URL du type `sfb-suivi.vercel.app`.

**C'est cette URL que tu partages avec ton staff.** Chacun l'ouvre depuis son téléphone/tablette, l'ajoute à son écran d'accueil (comme avant), et tout le monde travaille sur la même base de données Supabase — en temps réel, sans bug de sauvegarde.

## 🔁 Pour les futures modifications

Comme le code n'est plus dans Claude directement, la prochaine fois que tu veux une modification :
1. Demande-moi le code mis à jour dans une conversation Claude (je peux repartir de ce projet).
2. Remplace le fichier `src/App.jsx` sur GitHub par la nouvelle version (bouton crayon ✏️ sur GitHub pour éditer/remplacer un fichier).
3. Vercel redéploie automatiquement en quelques secondes dès que tu modifies un fichier sur GitHub — aucune autre action nécessaire.

## 🔒 Sécurité à connaître

La clé Supabase utilisée ici est une clé "publique" (anon) — c'est normal et sûr qu'elle soit visible dans le code, c'est prévu pour. En revanche, avec la configuration actuelle, **toute personne qui trouve l'URL de ton site peut voir et modifier les données** (comme le mode partagé que tu utilisais avant) : garde le lien réservé à ton staff de confiance. La vue coach (ressentis d'équipe) reste protégée par ton code PIN comme avant.
