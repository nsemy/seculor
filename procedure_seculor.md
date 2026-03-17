=====================================================
PROCÉDURE COMPLÈTE — SITE WEB SECULOR.CA
Hébergement GitHub Pages + Domaine GoDaddy + HTTPS
=====================================================


------------------------------------------------------
PARTIE 1 — HÉBERGER LA PAGE SUR GITHUB
------------------------------------------------------

1. Connectez-vous sur https://github.com

2. Cliquez sur "+" en haut à droite → "New repository"

3. Nommez-le : seculor
   - Cochez : Public
   - Cochez : Add a README file
   - Cliquez : Create repository

4. Dans votre dépôt, cliquez "Add file" → "Upload files"
   - Glissez-déposez votre fichier seculor.html
   - Cliquez "Commit changes"

5. Renommer le fichier :
   - Cliquez sur le fichier seculor.html dans le dépôt
   - Cliquez sur l'icône crayon (✏️) en haut à droite
   - Changez le nom "seculor.html" pour "index.html"
   - Cliquez "Commit changes"

6. Activer GitHub Pages :
   - Cliquez sur "Settings" (onglet en haut du dépôt)
   - Dans le menu de gauche → "Pages"
   - Sous "Branch", sélectionnez "main" → cliquez "Save"
   - Attendez 2 minutes
   - Votre site est temporairement en ligne à :
     https://nsemy.github.io/seculor

7. Configurer le domaine personnalisé dans GitHub :
   - Toujours dans Settings → Pages
   - Dans le champ "Custom domain", entrez : www.seculor.ca
   - Cliquez "Save"
   - GitHub crée automatiquement un fichier CNAME (c'est normal)


------------------------------------------------------
PARTIE 2 — LIER LE DOMAINE SECULOR.CA (GODADDY)
------------------------------------------------------

1. Connectez-vous sur https://godaddy.com

2. Allez dans : Mes produits → Domaines → Gérer
   (à côté de seculor.ca)

3. Cliquez sur "DNS"

4. MODIFIER l'enregistrement CNAME existant (www) :
   - Cliquez sur le crayon (✏️) à côté de :
     CNAME | www | seculor.ca.
   - Changez la valeur pour : nsemy.github.io
   - TTL : 1/2 Hour
   - Cliquez Enregistrer

   ⚠️ NE PAS TOUCHER aux enregistrements :
   - MX  → gère votre courriel olorisson@seculor.ca
   - TXT → vérification Google Workspace
   - NS / SOA → structure du domaine
   - _domainconnect CNAME → GoDaddy interne

5. AJOUTER 4 enregistrements A (un par un) :

   Type | Nom | Valeur
   -----|-----|-------
   A    | @   | 185.199.108.153
   A    | @   | 185.199.109.153
   A    | @   | 185.199.110.153
   A    | @   | 185.199.111.153

   Pour chaque enregistrement :
   - Cliquez "Ajouter" → choisissez type A
   - Nom : @
   - Valeur : l'adresse IP
   - TTL : 1/2 Hour
   - Cliquez Enregistrer

6. Attendez 30 à 60 minutes pour la propagation DNS


------------------------------------------------------
PARTIE 3 — SÉCURISER LE SITE (HTTPS / cadenas 🔒)
------------------------------------------------------

1. Retournez dans GitHub → Settings → Pages

2. Cliquez "Check again" sous Custom domain

3. Une fois la vérification réussie :
   - Cochez "Enforce HTTPS"
   - GitHub active automatiquement un certificat SSL
     gratuit via Let's Encrypt

4. Votre site est maintenant sécurisé à :
   https://www.seculor.ca


------------------------------------------------------
RÉSUMÉ DES ÉTAPES
------------------------------------------------------

Étape              | Action                        | Délai
-------------------|-------------------------------|----------
1. GitHub          | Créer dépôt + importer HTML   | 5 minutes
2. GitHub Pages    | Activer + configurer domaine  | 5 minutes
3. GoDaddy DNS     | Modifier CNAME + ajouter A    | 5 minutes
4. Propagation     | Attendre                      | 30-60 min
5. HTTPS           | Cocher Enforce HTTPS          | Automatique

Résultat final : https://www.seculor.ca ✅


------------------------------------------------------
INFORMATIONS DU SITE
------------------------------------------------------

Nom d'utilisateur GitHub : nsemy
Dépôt GitHub             : https://github.com/nsemy/seculor
URL temporaire           : https://nsemy.github.io/seculor
URL finale               : https://www.seculor.ca
Courriel                 : olorisson@seculor.ca
Téléphone                : 514-951-7642

Coût total : GRATUIT 🎉
(GitHub Pages est gratuit, domaine déjà possédé)


------------------------------------------------------
NOTE IMPORTANTE — IPs GitHub Pages
------------------------------------------------------

Les adresses IP 185.199.108-111.153 appartiennent à
Fastly Inc., le CDN officiel de GitHub Pages.
Elles sont sûres malgré certaines détections sur
VirusTotal (faux positifs dus aux IPs partagées).

Source officielle GitHub :
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

=====================================================
FIN DE LA PROCÉDURE
=====================================================
