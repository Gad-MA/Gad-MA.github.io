---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Hello
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin

  - block: experience
    id: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Research Assistant
          company: Faculty of Engineering - Cairo University
          company_url: ''
          company_logo: 'cufe3'
          date_start: '2025-12-01'
          date_end: ''
          description: |2-
            Working on developing an end-to-end pipeline for the automated longitudinal segmentation and tracking of multiple sclerosis brain lesions in FLAIR MRI images.
        - title: Software Engineering Research Intern
          company: University of Illinois Urbana-Champaign
          company_url: 'https://illinois.edu/'
          company_logo: 'uiuc'
          # location: Cairo, Egypt
          date_start: '2025-05-01'
          date_end: '2025-08-01'
          description: |2-
            Built Bash CLI tools and Python dataset analysis scripts to support research on using LLMs for software testing. Some examples are:
              - Conducted comparative analysis between Large Language Models (LLMs) and human evaluators to detect equivalent mutants in mutation testing.
              - Solved a large-scale data efficiency problem by developing a Bash CLI tool to optimize operations on a massive GitHub repository (9,000+ branches), reducing data retrieval latency from minutes to seconds.
              - Automated dataset analysis and information retrieval pipelines using Python.
        - title: Computer Vision Team Member
          company: Cairo University Racing Team - Formula Student
          company_url: 'https://www.linkedin.com/company/cairo-university-racing-team-formula-student/'
          company_logo: 'cairo_uni_racing_team_formula_student_logo'
          # location: Cairo, Egypt
          date_start: '2024-09-19'
          date_end: '2025-05-01'
          description: |2-
            Developed a visual-based perception model for the autonomous racing car by:
            - Implementing real-time 2D cone detection, color classification, and pose estimation using YOLO.
            - Developing 2D-to-3D cone pose estimation using the classical Perspective-n-Point (PnP) algorithm.
        - title: Brand Ambassador
          company: Emonovo
          company_url: 'https://www.emonovo.com/'
          company_logo: emonovo
          # location: Egypt
          date_start: '2021-04-01'
          date_end: '2022-02-01'
          description: |2-
              Promoted the brand through high school events, virtual meetings, and video content to grow the customer base.
    design:
      columns: '2'

  - block: collection
    id: recent-news
    content:
      title: Recent News
      # title: 📢 Recent News
      # subtitle: '[All news >>](/tag/news/)'
      count: 5
      filters:
        folders:
          - news
        tag: 'News'
    design:
      columns: '2'
      view: community/news_list

  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: 'Computer Vision'
          tag: 'Computer Vision'
        - name: 'Image Processing'
          tag: 'Image Processing'
        - name: 'OOP'
          tag: 'OOP'
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false

  # - block: collection
  #   id: research
  #   content:
  #     title: Research Work
  #     filters:
  #       folders:
  #         - publication
  #   design:
  #     columns: '2'
  #     # view: card
  #     # view: citation
  #     view: compact

  - block: collection
    id: posts
    content:
      title: ✏️ Blog Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 0
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'

  # - block: tag_cloud
  #   content:
  #     title: Topics I talk about
  #   design:
  #     columns: '2'


  - block: collection
    id: talks
    content:
      title: Talks
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact

  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: If you have any questions, or if you just want to say hi, please feel free to reach out.
      # Contact (add or remove contact options as necessary)
      email: mohamed.a.gad55@gmail.com
      # contact_links:
      #   - icon: twitter
      #     icon_pack: fab
      #     name: ''
      #     link: ''
      # Automatically link email and phone or display as text?
      autolink: true
    design:
      columns: '2'
---
