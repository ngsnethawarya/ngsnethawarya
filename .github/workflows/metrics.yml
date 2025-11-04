name: Metrics

on:
  schedule:
    - cron: "0 */24 * * *"
  workflow_dispatch:

permissions:
  contents: write  # allow committing the generated SVG

jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - name: Generate GitHub metrics
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}   # your PAT with repo + read:user
          user: ngsnethawarya
          template: classic
          base: header, activity, community, repositories
          config_timezone: America/Chicago
          filename: github-metrics.svg          # write this file to the repo root
          plugin_languages: yes
          plugin_languages_details: percentage
          plugin_languages_sections: most-used
          plugin_achievements: yes
          plugin_achievements_display: compact
          plugin_followup: yes
