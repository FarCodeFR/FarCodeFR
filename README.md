 ⚡️ Bienvenue sur mon GitHub ! ⚡️

## 🤝 Contact

- [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/timothé-renard-a686072b4/)
- **Portfolio** : 🚧 🚧 🚧 🚧

<h1 align="center">Bonjour 👋, Je suis Timothé</h1>
<h3 align="center">je suis un développeur web passionné par la création de sites et d'applications performants et intuitifs. 🚀</h3>


## 



## 📂 Mes projets phares

### 1. **[Nom du projet 1]**
   - **Description** : [Brève description du projet, par ex. "Une application de gestion des tâches intuitive et responsive."]
   - **Technologies** : React.js, Node.js, MongoDB
   - **Lien** : [Démo](https://exemple.com) | [Code source](https://github.com/utilisateur/projet1)

### 2. **[Nom du projet 2]**
   - **Description** : [Brève description, par ex. "Une plateforme e-commerce avec un système de paiement intégré."]
   - **Technologies** : Vue.js, Firebase, TailwindCSS
   - **Lien** : [Démo](https://exemple.com) | [Code source](https://github.com/utilisateur/projet2)

### 3. **[Nom du projet 3]**
   - **Description** : [Brève description, par ex. "Un blog personnel avec un CMS customisé."]
   - **Technologies** : Laravel, MySQL
   - **Lien** : [Démo](https://exemple.com) | [Code source](https://github.com/utilisateur/projet3)

---

## 🌱 Ce que j'apprends actuellement

- Next.js pour des applications SSR/SSG performantes
- GraphQL pour des API modernes et optimisées
- Docker pour la gestion de conteneurs

---

## 🏆 Stats GitHub

name: GitHub Snake Game

on:
  # Schedule the workflow to run daily at midnight UTC
  schedule:
    - cron: "0 0 * * *"
  # Allow manual triggering of the workflow
  workflow_dispatch:
  # Trigger the workflow on pushes to the main branch
  push:
    branches:
      - main
jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      # Step 1: Checkout the repository
      - name: Checkout Repository
        uses: actions/checkout@v3
      # Step 2: Generate the snake animations
      - name: Generate GitHub Contributions Snake Animations
        uses: Platane/snk@v3
        with:
          # GitHub username to generate the animation for
          github_user_name: ${{ github.repository_owner }}
          # Define the output files and their configurations
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
      # Step 3: Deploy the generated files to the 'output' branch
      - name: Deploy to Output Branch
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
          publish_branch: output
          # Optionally, you can set a custom commit message
          commit_message: "Update snake animation [skip ci]"

![Stats GitHub](https://github-readme-stats.vercel.app/api?username=FarCodeFR&show_icons=true&theme=radical)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=FarCodeFR&layout=compact)](https://github.com/anuraghazra/github-readme-stats)

---

Merci d'avoir visité mon profil ! 🌟 N'hésitez pas à explorer mes dépôts et à laisser des étoiles ⭐ si vous trouvez mes projets intéressants.
