# 🚀 Site Web Hirondia Pro - Guide de Déploiement GitHub Pages

## 📋 Contenu du Site

Votre site web professionnel pour **Hirondia Pro** comprend :

- ✅ **index.html** - Page d'accueil (Hero, fonctionnalités, statistiques)
- ✅ **fonctionnalites.html** - Détail des fonctionnalités
- ✅ **telechargement.html** - Page de téléchargement avec FAQ
- ✅ **contact.html** - Contact, documentation et support

---

## 🎯 Étape 1 : Créer un Compte GitHub

### Si vous n'avez pas de compte GitHub :

1. Aller sur **https://github.com**
2. Cliquer sur **"Sign up"**
3. Remplir :
   - **Username** : `hirondia` (ou votre choix)
   - **Email** : votre email
   - **Password** : mot de passe sécurisé
4. Vérifier votre email
5. **C'est gratuit !**

---

## 🏗️ Étape 2 : Créer le Dépôt GitHub Pages

### Instructions détaillées :

1. **Connectez-vous** à GitHub

2. Cliquez sur le **"+"** en haut à droite → **"New repository"**

3. **Configuration du dépôt :**
   ```
   Repository name: hirondia.github.io
   (⚠️ Ce nom EXACT est obligatoire pour GitHub Pages)
   ```

4. **Paramètres :**
   - ✅ Cocher **"Public"** (obligatoire pour GitHub Pages gratuit)
   - ✅ Cocher **"Add a README file"**
   - ❌ NE PAS cocher "Add .gitignore" ou "Choose a license" pour l'instant

5. Cliquer sur **"Create repository"**

---

## 📤 Étape 3 : Upload des Fichiers

### Méthode 1 : Upload Direct (Recommandé pour débuter)

1. **Dans votre dépôt GitHub**, cliquez sur **"Add file"** → **"Upload files"**

2. **Glissez-déposez les 4 fichiers HTML :**
   - `index.html`
   - `fonctionnalites.html`
   - `telechargement.html`
   - `contact.html`

3. **En bas de la page :**
   - Message du commit : `Ajout du site web Hirondia Pro`
   - Cliquer sur **"Commit changes"**

4. **Attendre 2-3 minutes** que GitHub traite les fichiers

---

## 🌐 Étape 4 : Activer GitHub Pages

1. Dans votre dépôt, cliquer sur **"Settings"** (onglet en haut)

2. Dans le menu de gauche, cliquer sur **"Pages"**

3. Sous **"Source"** :
   - Branch : **"main"**
   - Folder : **"/ (root)"**

4. Cliquer sur **"Save"**

5. **Attendre 2-5 minutes**

6. **Rafraîchir la page** → Un message vert apparaîtra :
   ```
   Your site is live at https://hirondia.github.io
   ```

---

## ✅ Étape 5 : Tester Votre Site

1. Ouvrir **https://hirondia.github.io** (remplacez `hirondia` par votre username)

2. **Vérifier :**
   - ✅ Page d'accueil s'affiche correctement
   - ✅ Navigation entre les pages fonctionne
   - ✅ Design responsive sur mobile
   - ✅ Formulaire de contact réagit

3. **Félicitations ! 🎉 Votre site est en ligne !**

---

## 🔄 Étape 6 : Mettre à Jour le Site

### Pour modifier le contenu :

1. **Cliquer sur le fichier** à modifier (ex: `index.html`)

2. Cliquer sur l'**icône crayon** (Edit this file)

3. **Modifier le code**

4. **Commit changes** en bas

5. **Attendre 1-2 minutes** → Les changements sont en ligne !

---

## 🌍 Étape 7 : Ajouter un Nom de Domaine Personnalisé (Optionnel)

### Passer de `hirondia.github.io` à `hirondia.com`

#### A. Acheter le domaine

1. Aller sur **Namecheap**, **OVH**, ou **Google Domains**
2. Chercher et acheter **hirondia.com** (~12€/an)

#### B. Configurer le DNS

**Chez votre hébergeur de domaine :**

1. Aller dans **DNS Management**

2. Ajouter ces **4 enregistrements A** :
   ```
   Type: A    Host: @    Value: 185.199.108.153
   Type: A    Host: @    Value: 185.199.109.153
   Type: A    Host: @    Value: 185.199.110.153
   Type: A    Host: @    Value: 185.199.111.153
   ```

3. Ajouter un **enregistrement CNAME** :
   ```
   Type: CNAME    Host: www    Value: hirondia.github.io
   ```

#### C. Configurer GitHub

1. Dans votre dépôt GitHub → **Settings** → **Pages**

2. Sous **"Custom domain"**, entrer : `hirondia.com`

3. Cliquer **"Save"**

4. ✅ Cocher **"Enforce HTTPS"** (attendre 24h si pas disponible)

5. **Attendre 24-48h** pour la propagation DNS

6. **Résultat :** Votre site sera accessible sur `hirondia.com` ! 🎉

---

## 🛠️ Personnalisation du Site

### Modifier les informations de contact :

**Dans `contact.html`, ligne ~120 :**
```html
<p><a href="mailto:contact@hirondia.com">contact@hirondia.com</a></p>
<p><a href="tel:+21612345678">+216 12 345 678</a></p>
```
→ Remplacez par vos vraies coordonnées

### Ajouter le lien de téléchargement réel :

**Dans `telechargement.html`, ligne ~480 (fonction handleDownload) :**
```javascript
// Remplacer par votre lien GitHub Release
window.location.href = 'https://github.com/hirondia/hirondia/releases/download/v2.0/HirondiaPro_Setup.exe';
```

### Changer les couleurs :

**Dans chaque fichier HTML, modifier les variables CSS (ligne ~15) :**
```css
:root {
    --primary: #667eea;        /* Couleur principale */
    --secondary: #764ba2;      /* Couleur secondaire */
}
```

---

## 📊 Héberger le Logiciel sur GitHub

### Pour permettre le téléchargement du fichier .exe :

1. **Créer une Release :**
   - Onglet **"Releases"** → **"Create a new release"**
   - Tag : `v2.0`
   - Title : `Hirondia Pro v2.0`
   - Description : Notes de version
   - **Attacher le fichier .exe** (drag & drop)
   - Cliquer **"Publish release"**

2. **Copier le lien de téléchargement** qui ressemble à :
   ```
   https://github.com/hirondia/hirondia/releases/download/v2.0/HirondiaPro_Setup.exe
   ```

3. **Mettre à jour** `telechargement.html` avec ce lien

---

## 📈 Suivi des Statistiques (Optionnel)

### Ajouter Google Analytics :

1. Créer un compte sur **https://analytics.google.com**

2. Obtenir votre **Measurement ID** (ex: G-XXXXXXXXXX)

3. **Ajouter ce code** avant `</head>` dans TOUS les fichiers HTML :
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🔒 Sécurité et Bonnes Pratiques

✅ **GitHub Pages est sécurisé** (HTTPS automatique)  
✅ **Pas de serveur à maintenir**  
✅ **Gratuit à vie** pour sites publics  
✅ **Sauvegarde automatique** (historique Git)  
✅ **100% uptime** garanti par GitHub  

---

## 📞 Support

### Besoin d'aide ?

- **Documentation GitHub Pages :** https://pages.github.com
- **Tutoriels vidéo :** YouTube "GitHub Pages tutorial"
- **Support GitHub :** https://support.github.com

---

## 🎉 Récapitulatif

Vous avez maintenant :

✅ Un site web professionnel  
✅ Hébergement gratuit à vie  
✅ URL : `https://hirondia.github.io`  
✅ Possibilité d'ajouter `hirondia.com` plus tard  
✅ Design moderne et responsive  
✅ 4 pages complètes  
✅ Formulaire de contact  
✅ Section téléchargement  

**Prochaines étapes suggérées :**

1. ✅ Tester le site sur mobile/tablette
2. ✅ Personnaliser les coordonnées de contact
3. ✅ Ajouter le fichier .exe en Release
4. ✅ Partager le lien sur les réseaux sociaux
5. ✅ (Plus tard) Acheter le domaine `hirondia.com`

---

## 🌟 Félicitations !

Votre site **Hirondia Pro** est maintenant en ligne et accessible partout dans le monde ! 🚀

**URL de votre site :** `https://hirondia.github.io`

---

*Créé avec ❤️ pour Hirondia Pro - Logiciel d'Audit Financier Premium*