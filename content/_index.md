---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

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
        url: uploads/CV_ECH_20251117.pdf
      #button:
       # text: Download resume
        #url: uploads/Resume_ECH_20251117.pdf
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
  - block: markdown
    content:
      title: Research
      subtitle: ''
      text: |-
        My research sits at the intersection of engineering, biology, and medicine, with a focus on non-invasive tools for imaging, stimulation, and measurement.

        Current themes include biomolecular ultrasound, acoustic reporter genes, ultrasound neuromodulation, mechanobiology, and cerebrospinal fluid mechanics. The [Research](/research/) page provides a fuller overview of these directions.
    design:
      columns: '1'
  - block: collection
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
  - block: markdown
    content:
      title: Recent Publications
      subtitle: ''
      text: |-
        For a fuller list of publications and recent manuscripts, see my Google Scholar profile linked above.

        [24] Han H, Ma X, Tang S, Zhao K, **Criado-Hidalgo E**, Truong HD, Yoo J, Fezzi C, Zhang J, Chen G, Hays C, Reyes Segura RJ, Jin Z, Liu A, Shapiro MG, Greer JR, Zhou Q, Gao W. Programmable multigas cancer therapy using ultrasound-propelled microrobots. *Nature Communications*. (In revision) [article](#)

        [23] Luo K, Ma Y, Li HR, Li H, Swift MB, Dalleska NF, Farooq AS, **Criado-Hidalgo E**, Liu A, Shapiro MG, Elowitz MB. In vivo spatial coordination with synthetic paracrine signaling. Submitted to *Nature Chemical Biology*. [article](#)

        [22] Lee J, Liu A, **Criado-Hidalgo E**, Ling B, You MY, Jin Z, Shapiro MG. Engineering monocytes as ultrasound reporter cells for cancer detection. In preparation. [article](#)

        [21] Shivaei S, Cheung K, Yadav A, Hurvitz I, Lee S, Revilla J, Rabut C, **Criado-Hidalgo E**, Zhang R, Shapiro MG. Ultrasound imaging of in situ transcriptional activity in opaque tissue. *Nature Methods*. (In revision) [article](#)

        [20] Vasallo R, Ling B, **Criado-Hidalgo E**, Robinson N, Schrunk E, Liu A, Daghlian G, Li HR, Swift MB, Mannar D, Malounda D, Lack N, Goldenberg L, Black PC, Cox ME, Salcudean SE, Shapiro MG. A modular method for rapidly prototyping targeted gas vesicle protein nanoparticles. *Bioconjugate Chemistry* 37 (2), 225-232 (2026). [article](https://pubs.acs.org/doi/full/10.1021/acs.bioconjchem.5c00387)
    design:
      columns: '1'
      css_class: homepage-publications
  - block: markdown
    id: news
    content:
      title: Writing & Updates
      subtitle: ''
      text: |-
        I plan to use the blog for occasional writing on research, engineering in medicine, and related scientific ideas.

        For now, the most complete view of my work is through the [Research](/research/), [Publications](/publications/), and [Experience](/experience/) pages.
    design:
      columns: '1'
  - block: markdown
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
