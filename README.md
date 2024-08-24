<h1 align="left">Hey 👋 What's up?</h1>

###

<h1 align="left">My name is Abdi Malika and I'm a Backend Developer</h1>

###

<h5 align="left">I have learned various programming languages, including PHP, Laravel, MySQL, and JavaScript. I also have experience in building web applications using the Laravel framework. I am a diligent learner and have good problem solving skills. I also have good communication skills and can work well with a team.</h5>

###

<p align="left">✨ Creating bugs since 2023<br>📚 I'm currently learning Laravel<br>🎯 Goals:  Fullstack Developer<br>🎲 Fun fact: Happines</p>

###

<h2 align="left">I code with</h2>

###

<div align="left">
  <img src="https://cdn.simpleicons.org/laravel/FF2D20" height="40" alt="laravel logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.simpleicons.org/php/777BB4" height="40" alt="php logo"  />
  <img width="12" />
  <img src="https://cdn.simpleicons.org/mysql/4479A1" height="40" alt="mysql logo"  />
</div>

###
<h1 align="center">This Is My Github🔥🔥</h1>

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=AsaMalika25&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="stats graph"  />
  <img src="https://streak-stats.demolab.com?user=AsaMalika25&locale=en&mode=daily&theme=dracula&hide_border=false&border_radius=5" height="150" alt="streak graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=AsaMalika25&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="languages graph"  />
</div>

###

<img align="right" height="150" src="https://c.tenor.com/nO51qBe-HjsAAAAC/tenor.gif"  />

###

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.simpleicons.org/laravel/FF2D20" height="30" alt="laravel logo"  />
  <img width="12" />
  <img src="https://cdn.simpleicons.org/php/777BB4" height="30" alt="php logo"  />
  <img width="12" />
  <img src="https://cdn.simpleicons.org/mysql/4479A1" height="30" alt="mysql logo"  />
</div>

###

<div align="center">
  <img src="https://img.shields.io/static/v1?message=Instagram&logo=instagram&label=&color=E4405F&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="instagram logo"  />
  <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="linkedin logo"  />
</div>

###
<br clear="both">
<img src="https://raw.githubusercontent.com/AsaMalika25/AsaMalika25/output/snake.svg" alt="Snake animation" />
###
###
###

name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

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
          github_user_name: ${{ github.AsaMalika25 }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
