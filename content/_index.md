---
# Leave the homepage title empty to use the site title
title: ''
date: 2026-07-26
lastmod: 2026-07-26
type: landing
summary: Ernesto Criado-Hidalgo builds non-invasive tools for imaging, stimulation, and measurement at the intersection of engineering, biology, and medicine.

seo:
  title: 'Ernesto Criado-Hidalgo | Engineering in Medicine'

design:
  # Default section spacing
  spacing: '6rem'

sections:
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

        Current themes include biomolecular ultrasound, acoustic reporter genes, ultrasound neuromodulation, mechanobiology, and cerebrospinal fluid mechanics. The [Research](/research/) page provides a fuller overview of these directions.
    design:
      columns: '1'
  - block: semantic-collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: semantic-markdown
    content:
      title: Recent Publications
      subtitle: ''
      text: |-
        For a fuller list of publications and recent manuscripts, see my Google Scholar profile linked above.

        Han H, Ma X, Tang S, Zhao K, **Criado-Hidalgo E**, Truong HD, Yoo J, Fezzi C, Zhang J, Chen G, Hays C, Reyes Segura RJ, Jin Z, Liu A, Shapiro MG, Greer JR, Zhou Q, Gao W (2026). Programmable multigas cancer therapy using ultrasound-propelled microrobots. *Nature Communications*. In revision.

        Luo K, Ma Y, Li HR, Li H, Swift MB, Dalleska NF, Farooq AS, **Criado-Hidalgo E**, Liu A, Shapiro MG, Elowitz MB (2026). [In vivo spatial coordination with synthetic paracrine signaling](https://doi.org/10.64898/2026.06.26.734902). Submitted to *Nature Chemical Biology*.

        Lee J, Liu A, **Criado-Hidalgo E**, Ling B, You MY, Jin Z, Shapiro MG (2026). Engineering monocytes as ultrasound reporter cells for cancer detection. In preparation.

        Shivaei S, Cheung K, Yadav A, Hurvitz I, Lee S, Revilla J, Rabut C, **Criado-Hidalgo E**, Zhang R, Shapiro MG (2026). [Ultrasound imaging of in situ transcriptional activity in opaque tissue](https://doi.org/10.1101/2025.07.06.663365). *Nature Methods*. In revision.

        Vasallo R, Ling B, **Criado-Hidalgo E**, Robinson N, Schrunk E, Liu A, Daghlian G, Li HR, Swift MB, Mannar D, Malounda D, Lack N, Goldenberg L, Black PC, Cox ME, Salcudean SE, Shapiro MG (2026). [A modular method for rapidly prototyping targeted gas vesicle protein nanoparticles](https://pubs.acs.org/doi/full/10.1021/acs.bioconjchem.5c00387). *Bioconjugate Chemistry* 37 (2), 225-232.
    design:
      columns: '1'
      css_class: homepage-publications
  - block: semantic-markdown
    id: news
    content:
      title: Writing & Updates
      subtitle: ''
      text: |-
        I write about research, engineering in medicine, scientific computing, and the tools that support multidisciplinary work.

        Visit the [Blog](/blog/) for recent posts on ultrasound-enabled technologies, mechanobiology, data science, and AI-assisted research workflows.
    design:
      columns: '1'
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
