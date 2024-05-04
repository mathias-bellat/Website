---
# Leave the homepage title empty to use the site title
title: ''
date: 2024-04-30
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: skills
    content:
      title: Skills
      text: ''
      # Choose a user to display skills from (a folder name within `content/authors/`)
      username: admin
    design:
      columns: '1'
  - block: experience
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
        - title: Doctoral Contract
          company: University of Tübingen
          company_url: ''
          company_logo: Tub
          location: Tübingen
          date_start: '2021-10-01'
          date_end: ''
          description: |2-
              Responsibilities include:

              * Soils survey
              * FTIR analyses
              * Soil laboratory analysis (texture, pH, CaCO3...)
              * Machine Learning experience in Archaeology
              * Geoarchaeology analysis (Datations, stratigraphy)
    
    
        - title: Director of excavation
          company: Monachus
          company_url: ''
          company_logo: Monachus
          location: Paris/Rambouillet
          date_start: '2021-06-01'
          date_end: '2021-07-31'
          description: Direction of an archaeological medieval excavation with 7 - 10 archaeologists.

      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
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
        - name: Archéo-informatique
          tag: Archéo-informatique
        - name: Micromorphologie
          tag: Micromorphologie
        - name: Proche-Orient
          tag: Proche-Orient
        - name: Géoarchéologie
          tag: Géoarchéologie
    
    design:
      columns: '2'
      view: compact
  - block: collection
    id: publications
    content:
      title: Publications récentes
      text: |-
        {{% callout note %}}
        Rechercher le contenu approprié avec [filter les publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation 
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        N'hésitez pas à me contacter je vous repondrai dans les plus bref délais.
      # Contact (add or remove contact options as necessary)
      email: mathias.bellat@uni-tuebingen.de
      phone: +49(0)7071-29-74-081
      #appointment_url: 'https://calendly.com'
      address:
        street: 19-23 Rümelinstraße
        city: Tübingen
      #  region: 
        postcode: '72070'
        country: Germany
      #  country_code: DEU
      directions: Premier étage bâtiment ouest bureau W302
      #office_hours:
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '48.5238539'
        longitude: '9.0549744'  
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
---
