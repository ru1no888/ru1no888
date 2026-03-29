name: Generate Snake Animation

on:
  # รันอัตโนมัติทุกๆ 24 ชั่วโมง
  schedule:
    - cron: "0 0 * * *" 
  
  # อนุญาตให้กดรันเองได้แบบ Manual
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Generate GitHub Contribution Grid Snake
        uses: Platane/snk@v3
        with:
          # ใส่ชื่อ GitHub ของคุณ
          github_user_name: ru1no888
          
          # สร้างไฟล์ 2 เวอร์ชั่น (โหมดสว่าง และ โหมดมืด)
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark

      - name: Push to Output Branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          # โค้ดจะส่งรูปไปเก็บไว้ที่ branch ชื่อ 'output'
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
