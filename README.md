### Salve, men! Tô guardando meus códigos aqui. Se quiser dar uma olhada, fica à vontade! (Só não copiar que tá dboa!) 🧑‍💻


- 🔭 Hoje trabalho com Front-end, Back-end e Marketing Digital (PLR)
- 🌱 Estudando Hacking

<!--
<div>
    <a href="https://araujocode.netlify.app/"></a>
    <img height="180em" src="https://github-readme-stats.vercel.app/api?username=JJL0s3r&show_icons=true&theme=dracula&include_all_commits=true&count_private=true" />
    <img height="180em" src="https://github-readme-stats.vercel.app/api/wakatime?username=JJL0s3r" />
    

</div>
-->

<div>
  
  <img  height="180em" src="https://github-readme-stats.vercel.app/api?username=JJL0s3r&show_icons=true&theme=great-gatsby&include_all_commits=true&count_private=true"/>
  <img align="right" height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=JJL0s3r&layout=compact&langs_count=16&theme=great-gatsby"/>
</div>
<br>

<div  align="center"> 
  <div style="display: inline_block"><br>
    <img align="left" height="250" alt="coding-time" src="code.gif">
    <h1 align="center">Minhas Tecnologias Preferidas <3</h1>


        
<div style="display: inline_block"><br>
      <img align="center" alt="JJL0s3r-HTML" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="JJL0s3r-CSS" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="JJL0s3r-Js" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="JJL0s3r-React" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
  <img align="center" alt="JJL0s3r-BootStrap" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" />
  <img align="center" alt="JJL0s3r-Python" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="JJL0s3r-PHP" height="50" width="60"  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" />
  <img align="center" alt="JJL0s3r-MySQL" height="60" width="70" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" />
  <img align="center" alt="JJL0s3r-NodeJS" height="60" width="70"  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original-wordmark.svg" />
  <img align="center" alt="JJL0s3r-Ruby" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ruby/ruby-original.svg" />
  <img align="center" alt="JJL0s3r-Onrails" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rails/rails-original-wordmark.svg" >
</div>
   </div>
    
  
  <h1 align="center">Redes Sociais</h1>
    <div> 
  <a href="https://www.youtube.com/channel/UCrOcWtDQez3eterfyK8-u2A" target="_blank"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" target="_blank"></a>
  <a href="https://instagram.com/ealvesjj" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
 	<a href="https://www.twitch.tv/JJL0s3r" target="_blank"><img src="https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white" target="_blank"></a>
  <a href = "mailto:d.aaraujo.ti@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/daniel-araujo-0043a0273/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  
</div>
</div>
    
    
    # Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: Formandodev #Seu usuario
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}


