---
title: Publications
date: 2026-04-26
type: landing

design:
  spacing: '5rem'

sections:
  - block: collection
    content:
      title: Featured Publications
      text: A curated selection of representative publications across current research directions.
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: All Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---
