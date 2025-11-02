## Olá! Eu sou a Ana Reis 👋

- 💼 Trabalho em uma *Clínica de Terapias Integradas*  
- 💻 Estudando *GTI*  
- 📧 Contate-me no email: *roll72316@gmail.com*  
- 👩‍ Pronouns: *ela/dela*

---

### 📊 Minhas Estatísticas no GitHub
<div align="center">
  <a href="https://github.com/Ana-Reis22">
    <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Ana-Reis22&show_icons=true&theme=merko&include_all_commits=true&count_private=true"/>
    <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ana-Reis22&layout=compact&langs_count=16&theme=merko"/>
  </a>
</div>


<div style="display: inline_block"><br>
  <img align="center" alt="Ana-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Ana-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
 <img align="center" alt="Ana-MySQL" height="40" width="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg">
  <img align="center" alt="Ana-VSCode" height="40" width="50" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vscode/vscode-original.svg">
</div>

  
  ##
 
<div> 
  <a href="https://instagram.com/reis.karol12" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:roll72316@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/ana-carolina-reis-s%" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>

name: Generate Snake Animation

on:
  schedule: # Gera automaticamente todo dia à meia-noite
    - cron: "0 0 * * *"
  workflow_dispatch: # Permite rodar manualmente
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout do repositório
        uses: actions/checkout@v3

      - name: Gerar animação da cobrinha 🐍
        uses: Platane/snk@v3
        with:
          github_user_name: Ana-Reis22  # <-- seu nome de usuário aqui
          outputs: dist/snake.svg

      - name: Publicar no branch de saída
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

          ### 🐍 Minhas Contribuições

<p align="center">
  <img src="https://raw.githubusercontent.com/Ana-Reis22/Ana-Reis22/output/snake.svg" alt="Cobrinha animada"/>
</p>
