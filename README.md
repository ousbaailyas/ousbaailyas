### Hi there 👋


Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          #  - public_repo
          #  - repo
          #  - read:user
          #  - read:org
          # The following additional scopes may be required:
          #  - read:org  (for organization related metrics)
          #  - read:user (for user related data)
          #  - repo      (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: ousbaailyas
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Africa/Casablanca
          plugin_achievements: yes
          plugin_achievements_display: detailed
          plugin_achievements_secrets: yes
          plugin_achievements_threshold: C
          plugin_activity: yes
          plugin_activity_days: 14
          plugin_activity_filter: all
          plugin_activity_limit: 5
          plugin_activity_load: 300
          plugin_activity_visibility: all
          plugin_anilist: yes
          plugin_anilist_limit: 2
          plugin_anilist_limit_characters: 22
          plugin_anilist_medias: anime, manga
          plugin_anilist_sections: favorites
          plugin_anilist_shuffle: yes
          plugin_anilist_user: .user.login
          plugin_code: yes
          plugin_code_lines: 12
          plugin_code_load: 100
          plugin_code_visibility: public
          plugin_discussions: yes
          plugin_discussions_categories: yes
          plugin_followup: yes
          plugin_followup_sections: repositories
          plugin_fortune: yes
          plugin_gists: yes
          plugin_habits: yes
          plugin_habits_days: 14
          plugin_habits_facts: yes
          plugin_habits_from: 200
          plugin_introduction: yes
          plugin_introduction_title: yes
          plugin_isocalendar: yes
          plugin_isocalendar_duration: half-year
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_limit: 8
          plugin_languages_recent_categories: markup, programming
          plugin_languages_recent_days: 14
          plugin_languages_recent_load: 300
          plugin_languages_sections: most-used
          plugin_languages_threshold: 0%
          plugin_lines: yes
          plugin_music: yes
          plugin_music_limit: 4
          plugin_music_time_range: short
          plugin_music_top_type: tracks
          plugin_music_user: .user.login
          plugin_nightscout: yes
          plugin_nightscout_datapoints: 12
          plugin_nightscout_highalert: 180
          plugin_nightscout_lowalert: 80
          plugin_nightscout_urgenthighalert: 250
          plugin_nightscout_urgentlowalert: 50
          plugin_nightscout_url: https://example.herokuapp.com
          plugin_notable: yes
          plugin_notable_from: organization
          plugin_notable_types: commit
          plugin_pagespeed: yes
          plugin_pagespeed_url: .user.website
          plugin_people: yes
          plugin_people_limit: 24
          plugin_people_size: 28
          plugin_people_types: followers, following
          plugin_poopmap: yes
          plugin_poopmap_days: 7
          plugin_posts: yes
          plugin_posts_limit: 4
          plugin_posts_user: .user.login
          plugin_projects: yes
          plugin_projects_limit: 4
          plugin_reactions: yes
          plugin_reactions_display: absolute
          plugin_reactions_limit: 200
          plugin_reactions_limit_discussions: 100
          plugin_reactions_limit_discussions_comments: 100
          plugin_reactions_limit_issues: 100
          plugin_repositories: 100
          plugin_repositories: yes
          plugin_repositories_affiliations: owner
          plugin_repositories_batch: 100
          plugin_rss: yes
          plugin_rss_limit: 4
          plugin_screenshot: yes
          plugin_screenshot_background: yes
          plugin_screenshot_selector: body
          plugin_screenshot_title: Screenshot
          plugin_skyline: yes
          plugin_skyline_frames: 60
          plugin_skyline_quality: 0.5
          plugin_skyline_year: current-year
          plugin_sponsors: yes
          plugin_sponsors_sections: goal, about
          plugin_stackoverflow: yes
          plugin_stackoverflow_limit: 2
          plugin_stackoverflow_lines: 4
          plugin_stackoverflow_lines_snippet: 2
          plugin_stackoverflow_sections: answers-top, questions-recent
          plugin_stargazers: yes
          plugin_stargazers_charts_type: classic
          plugin_starlists: yes
          plugin_starlists_limit: 2
          plugin_starlists_limit_languages: 8
          plugin_starlists_limit_repositories: 2
          plugin_starlists_shuffle_repositories: yes
          plugin_stock: yes
          plugin_stock_duration: 1d
          plugin_stock_interval: 5m
          plugin_support: yes
          plugin_topics: yes
          plugin_topics_limit: 15
          plugin_topics_mode: starred
          plugin_topics_sort: stars
          plugin_traffic: yes
          plugin_tweets: yes
          plugin_tweets_limit: 2
          plugin_tweets_user: .user.twitter
          plugin_wakatime: yes
          plugin_wakatime_days: 7
          plugin_wakatime_limit: 5
          plugin_wakatime_sections: time, projects, projects-graphs, languages, languages-graphs, editors, os
          plugin_wakatime_url: https://wakatime.com
          plugin_wakatime_user: current
