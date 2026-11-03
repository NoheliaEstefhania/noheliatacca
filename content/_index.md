---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: true

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: markdown
    content:
      title: '📚 My Research & Mission'
      subtitle: ''
      text: |-
        I am a Systems Engineer, researcher, and educator currently serving as a **Quechua Language Instructor at the Language Center of Universidad Nacional de San Agustín de Arequipa (UNSA)**.

        My interdisciplinary research focuses on **Indigenous Language Revitalization (Southern Quechua)**, **Low-Resource Natural Language Processing (NLP)**, and **Computer-Assisted Language Learning (CALL)**. I design computational tools, deterministic morphological analyzers, and embodied learning frameworks (combining Quechua Second Language Acquisition with Andean dance) to bridge urban academic spaces and indigenous communities while championing Andean digital humanities and data sovereignty.

        Feel free to reach out to collaborate! 😃
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Research Presentations & Conference Papers
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    id: projects
    content:
      title: Research Projects & Technologies
      filters:
        folders:
          - projects
    design:
      view: card
      columns: 2
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - events
    design:
      view: card
---
