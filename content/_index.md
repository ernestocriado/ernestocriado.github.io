---
# Leave the homepage title empty to use the site title
title: ''
date: 2026-07-26
lastmod: 2026-07-29
type: landing
summary: Ernesto Criado-Hidalgo builds non-invasive tools for imaging, stimulation, and measurement at the intersection of engineering, biology, and medicine.

seo:
  title: 'Ernesto Criado-Hidalgo | Engineering in Medicine'

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: semantic-markdown
    content:
      text: |-
        Website content is currently being updated.
    design:
      columns: '1'
      css_class: site-status-notice
      spacing:
        padding: ['0.65rem', '0', '0.65rem', '0']
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/cv.pdf
      resume_button:
        text: Download Resume
        url: uploads/resume.pdf
      headings:
        about: <span class="block">Translating engineering into non-invasive tools</span><span class="block">for biology and medicine</span>
        education: ''
        interests: ''
      secondary_button:
        text: View Research
        url: /research/
      tertiary_button:
        text: Publications
        url: /publications/
    design:
      # Apply a gradient background
      css_class: hbx-bg-gradient
      spacing:
        padding: ['0.5rem', '0', '6rem', '0']
      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: semantic-markdown
    content:
      title: Research
      subtitle: ''
      text: |-
        My research sits at the intersection of engineering, biology, and medicine, with a focus on non-invasive tools for imaging, stimulation, and measurement.

        Current themes include biomolecular ultrasound, acoustic reporter genes, ultrasound neuromodulation, mechanobiology, and cerebrospinal fluid mechanics.
      button:
        text: Explore my research
        url: /research/
    design:
      columns: '1'
      css_class: homepage-section-copy
  - block: semantic-collection
    id: papers
    content:
      title: Featured Publications
      button:
        text: View all publications
        url: /publications/
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
      css_class: homepage-featured-publications
  - block: semantic-markdown
    id: news
    content:
      title: Writing & Updates
      subtitle: ''
      text: |-
        I write about research, engineering in medicine, scientific computing, and the tools that support multidisciplinary work.

        Recent posts explore ultrasound-enabled technologies, mechanobiology, data science, and AI-assisted research workflows.
      button:
        text: Read the blog
        url: /blog/
    design:
      columns: '1'
      css_class: homepage-section-copy
  - block: semantic-markdown
    id: contact
    content:
      title: Contact
      subtitle: ''
      text: |-
        Open to research conversations, collaborations, and opportunities at the intersection of engineering, biology, and medicine.

        **Ernesto Criado-Hidalgo**  
        James Boswell Postdoctoral Scholar  
        California Institute of Technology  
        391 S Holliston Ave  
        MC 210-41 (Shapiro Lab)  
        Pasadena, CA  
        91106

        [ecriadoh@caltech.edu](mailto:ecriadoh@caltech.edu)  
        [ernestocriado@gmail.com](mailto:ernestocriado@gmail.com)

        {{< profile-icons username="admin" >}}
    design:
      columns: '1'
      css_class: contact-section
---
