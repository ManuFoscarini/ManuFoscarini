
# Hi there, I'm Manu! 👋

Software engineer with experience in C, C ++, Python and Java. 

- 🔭 Computer Science undergrad at UFSC
- 👯 I’m currently working as a Full Stack Developer at Bridge Labs

### Connect with me:

:mailbox: manuufoscarini@gmail.com |
[Linkedin](https://www.linkedin.com/in/emanuelle-foscarini-a4a9b120a/)


name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: manufoscarini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
