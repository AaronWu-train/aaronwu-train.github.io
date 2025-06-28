---
title: Posts
summary: My courses
type: landing

cascade:
  - _target:
      kind: page
    params:
      show_breadcrumb: true

sections:
  - block: collection
    id: posts
    content:
      title: Posts
      filters:
        folders:
          - posts
    design:
      view: article-grid
      columns: 2
---
