

# Hola, Soy Pablo!

[![MY PORTFOLIO](https://img.shields.io/badge/MY%20PORTFOLIO-000000?style=for-the-badge&logoColor=white&labelColor=000000&color=000000)](https://pablosolis.com)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pablo-solis-front-end)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pablo.solishrt@gmail.com)

Soy  Desarrollador **Front-End** apasionado por crear experiencias web modernas, fluidas y funcionales.  

Cuento con más de 2 años de experiencia desarrollando sitios web enfocados en el Front-End y la experiencia de usuario.


## Proyectos destacados
🔗 [WeatherApp](https://weatherappsol.netlify.app) – Mi portafolio personal con animaciones, diseño responsivo y enfoque en experiencia de usuario.  

🔗 [pablosolis.com](https://pablosolis.com) – Weather App que muestra el clima en tiempo real usando una REST API, desarrollada con JavaScript, Axios, SCSS y HTML.



## Tecnologías y herramientas
<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original-wordmark.svg" height="40" alt="tailwindcss logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="40" alt="typescript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="40" alt="react logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jquery/jquery-original.svg" height="40" alt="jquery logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" height="40" alt="nodejs logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="40" alt="git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="40" alt="vscode logo"  />
</div>

###


## Git Hub Stats

[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com?user=Pablo8Solis&theme=tokyonight&locale=es)](https://git.io/streak-stats)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Pablo8Solis)](https://github.com/anuraghazra/github-readme-stats)


name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

  steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark

    - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist 
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

<img src="https://raw.githubusercontent.com/Pablo8Solis/Pablo8Solis/output/snake.svg" alt="Snake animation" />

###
