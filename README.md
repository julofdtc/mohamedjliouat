# مدونة محمد اجليوط | Blog de Mhamed Jliouat

مدونة شخصية لنشر المقالات باللغة العربية، مستضافة على GitHub Pages.

Blog personnel pour publier des articles en arabe, hébergé sur GitHub Pages.

---

## 🚀 Déploiement sur GitHub Pages

### ✅ Déploiement effectué le 23/02/2026

Le site est **en ligne** à : **https://julofdtc.github.io/mohamedjliouat/**

#### Processus de déploiement utilisé :

1. **Création du repo** via l'API GitHub :
   ```
   POST https://api.github.com/user/repos
   → julofdtc/mohamedjliouat (public)
   ```

2. **Push du code** depuis le dossier local :
   ```bash
   cd mohamedjliouat
   git add -A && git commit -m "Ready for GitHub Pages"
   git remote add origin https://github.com/julofdtc/mohamedjliouat.git
   git push -u origin main
   ```

3. **Activation de GitHub Pages** via l'API :
   ```
   POST https://api.github.com/repos/julofdtc/mohamedjliouat/pages
   → source: branch "main", path "/"
   ```

4. **Build automatique** par GitHub (~1 min) → Site en ligne !

### Configuration `_config.yml` (déjà faite)

```yaml
baseurl: "/mohamedjliouat"                   # nom du repo
url: "https://julofdtc.github.io"            # URL GitHub Pages
```

### Re-déployer / Mettre à jour

Chaque commit sur la branche `main` déclenche automatiquement un rebuild du site.
- Via GitHub.com : modifier un fichier → Commit → le site se met à jour en ~1 min
- Via terminal :
  ```bash
  git add -A && git commit -m "description" && git push
  ```

---

## ✍️ كيف تضيف مقالاً جديداً؟ | Comment ajouter un article ?

### الطريقة (عبر موقع GitHub) | Via le site GitHub

1. **Allez sur** : `https://github.com/julofdtc/mohamedjliouat`
2. **Ouvrez le dossier** `_posts`
3. **Cliquez** sur **"Add file"** → **"Create new file"**
4. **Nommez le fichier** avec ce format :
   ```
   YYYY-MM-DD-titre-en-latin.md
   ```
   Exemple : `2026-03-15-mon-article.md`

5. **Copiez ce modèle** au début du fichier :
   ```markdown
   ---
   title: "عنوان المقال هنا"
   subtitle: "عنوان فرعي (اختياري)"
   date: 2026-03-15
   category: "عام"
   ---

   اكتب نص المقال هنا...

   ## عنوان فرعي

   فقرة جديدة هنا...

   > اقتباس مميز
   ```

6. **Cliquez** sur **"Commit new file"** (bouton vert en bas)
7. **Attendez ~1 minute** → L'article apparaît automatiquement sur le site !

### نموذج مقال | Modèle d'article

```markdown
---
title: "عنوان المقال"
subtitle: "وصف مختصر"
date: 2026-03-15
category: "ثقافة"
---

بسم الله الرحمن الرحيم

هنا يبدأ نص المقال. اكتب كل ما تريد هنا بحرية.

## عنوان فرعي

فقرة جديدة تحت العنوان الفرعي.

- نقطة أولى
- نقطة ثانية
- نقطة ثالثة

> هذا اقتباس أو جملة مميزة تريد إبرازها

### عنوان أصغر

تكملة النص هنا...
```

### التنسيقات المتاحة | Formatage disponible

| ماذا تريد؟ | ماذا تكتب؟ | النتيجة |
|---|---|---|
| عنوان كبير | `## عنوان` | عنوان كبير |
| عنوان صغير | `### عنوان` | عنوان صغير |
| خط عريض | `**كلمة**` | **كلمة** |
| خط مائل | `*كلمة*` | *كلمة* |
| اقتباس | `> نص الاقتباس` | نص مميز |
| قائمة نقاط | `- عنصر` | • عنصر |
| خط فاصل | `---` | ─────── |

### الفئات المقترحة | Catégories suggérées

| الفئة | الوصف |
|---|---|
| `عام` | مواضيع عامة |
| `ثقافة` | مقالات ثقافية وأدبية |
| `مجتمع` | قضايا اجتماعية |
| `رأي` | مقالات رأي |
| `تاريخ` | مقالات تاريخية |

---

## 🗑️ حذف مقال | Supprimer un article

1. Allez dans le dossier `_posts` sur GitHub
2. Cliquez sur le fichier à supprimer
3. Cliquez sur l'icône **🗑️ (Delete)** en haut à droite
4. Confirmez avec **"Commit changes"**

## ✏️ تعديل مقال | Modifier un article

1. Allez dans le dossier `_posts` sur GitHub
2. Cliquez sur le fichier à modifier
3. Cliquez sur l'icône **✏️ (Edit)** en haut à droite
4. Modifiez le contenu
5. Cliquez sur **"Commit changes"**

---

## 🏗️ Structure du projet

```
mohamedjliouat/
├── _config.yml          ← Configuration du blog
├── _layouts/            ← Templates HTML
│   ├── default.html
│   ├── home.html
│   └── post.html
├── _includes/           ← Composants réutilisables
│   ├── head.html
│   ├── header.html
│   └── footer.html
├── _posts/              ← 📝 LES ARTICLES ICI
│   ├── 2026-02-15-education-values.md
│   ├── 2026-02-20-reading-in-digital-age.md
│   └── 2026-02-23-welcome.md
├── assets/
│   ├── css/style.css    ← Styles du blog
│   └── favicon.svg      ← Icône du site
├── index.md             ← Page d'accueil
├── about.md             ← Page "À propos"
└── README.md            ← Ce fichier
```

## 💡 Pour le développeur

- Le site utilise **Jekyll** (intégré à GitHub Pages)
- **Aucun build local nécessaire** — GitHub le fait automatiquement
- Design **RTL** (droite à gauche) pour l'arabe
- Polices : **Noto Naskh Arabic** + **Amiri** (Google Fonts)
- Responsive : fonctionne sur mobile et desktop
- **Mode sombre** avec basculement automatique
- **Temps de lecture** estimé pour chaque article
- **Bouton de partage** (copier le lien)
- **Scroll to top** pour les longs articles
- **Design Marocain** avec couleurs et ornements inspirés du zellige
- Pour tester localement :
  ```bash
  gem install bundler jekyll
  bundle install
  bundle exec jekyll serve
  ```
  Puis ouvrir `http://localhost:4000/mohamedjliouat/`

---

**صنع بكل حب ❤️ | Fait avec amour**
