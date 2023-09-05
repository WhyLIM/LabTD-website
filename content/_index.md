---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        <div style="float: left;">{{< figure src="icon1.png" width="70px" >}}</div>
        <div style="float: left;">&nbsp;&nbsp;Lab TD</div><br>
    #   image:
    #     filename: icon.png
      text: |
        <br>

        <p>Our research endeavors revolve around delving into the underlying biological mechanisms behind comorbidity, while simultaneously harnessing the power of bioinformatics to prognosticate potential biomarkers for intricate diseases.</p>
    design:
      background:
        image:
          # Name of image in `assets/media/`.
          filename: banner.jpg
          # Apply image filters?
          filters:
            # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
            brightness: 0.6
          #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
          size: cover
          # Image focal point. Options include `left`, `center` (default), or `right`.
          position: center
          # Use a fun parallax-like fixed background effect on desktop? true/false
          parallax: true
        # Text color (true=light, false=dark, or remove for the dynamic theme color).
        text_color_light: true

  - block: portfolio
    id: projects
    content:
      title: Projects
      subtitle: 
      text: |
        <br>
      filters:
        # Folders to display content from
        folders:
          - project
        # Only show content with these tags
        tags: []
        # Exclude content with these tags
        exclude_tags: []
        # Which Hugo page kinds to show (https://gohugo.io/templates/section-templates/#page-kinds)
        kinds:
          - page
      # Field to sort by, such as Date or Title
      sort_by: 'Date'
      sort_ascending: false
      # Default portfolio filter button
      # 0 corresponds to the first button below and so on
      # For example, 0 will default to showing all content as the first button below shows content with *any* tag
    #   default_button_index: 0
      # Filter button toolbar (optional).
      # Add or remove as many buttons as you like.
      # To show all content, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the button toolbar, delete the entire `buttons` block.
    #   buttons:
    #     - name: All
    #       tag: '*'
    #     - name: Deep Learning
    #       tag: Deep Learning
    #     - name: Other
    #       tag: Demo
    design:
      # See Page Builder docs for all section customization options.
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      # Choose a listing view
      view: 5
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false

#   - block: features
#     content:
#       title: Interests
#       subtitle: Section subtitle
#       text: 
#       items:
#         - name: R
#           description: 90%
#           icon: r-project
#           icon_pack: fab
#         - name: Statistics
#           description: 100%
#           icon: chart-line
#           icon_pack: fas
#         - name: Photography
#           description: 10%
#           icon: camera-retro
#           icon_pack: fas
#         - name: Unicorns
#           description: I have a pet unicorn.
#           icon: 🦄
#           icon_pack: emoji

  - block: slider
    content:
      slides:
      - title: 🆕 Welcome to the **CBD2**
        content: V2 of the Colorectal Cancer Biomarker Database
        align: center
        background:
          image:
            filename: img/homepage-slide/cbd.png
            filters:
              brightness: 0.5
          position: right
          color: '#666'
        link:
          icon: database
          icon_pack: fas
          text: Try CBD2 ➡️
          url: http://www.eyeseeworld.com/cbd/
      - title: Take a look at **EBD** 👁️
        content: EBD is an Eye Biomarker Database
        align: center
        background:
          image:
            filename: img/homepage-slide/ebd.png
            filters:
              brightness: 0.5
          position: center
          color: '#555'
        link:
          icon: database
          icon_pack: fas
          text: Go to EBD ➡️
          url: http://www.eyeseeworld.com/ebd/
      - title: 👋 Do you know **SBD**?
        content: It's our Sepsis Biomarker Database
        align: center
        background:
          image:
            filename: img/homepage-slide/sbd.png
            filters:
              brightness: 0.5
          position: center
          color: '#333'
        link:
          icon: database
          icon_pack: fas
          text: Learn about SBD ➡️
          url: http://www.sysbio.org.cn/sbd/
    design:
      # Slide height is automatic unless you force a specific height (e.g. '400px')
      slide_height: ''
      is_fullscreen: true
      # Automatically transition through slides?
      loop: true
      # Duration of transition between slides (in ms)
      interval: 3000
  
  - block: collection
    id: news
    content:
      title: Latest News
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: compact
      columns: '1'
  
  - block: collection
    id: publications
    content:
      title: Publications
      text: |-
        {{% callout note %}}
        SEE ALL PUBLICATIONS by [***FILTER***](./publication/).
        {{% /callout %}}
      count: 10
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '1'
      view: citation

  - block: people
    id: people
    content:
      title: Meet the Team
      # Choose which groups/teams of users to display.
      #   Edit `user_groups` in each user's profile to add them to one or more of these groups.
      user_groups:
        - Principal Investigators
        - Researchers
        - Students
      sort_by: Params.last_name
      sort_ascending: true
    design:
      # Show user's social networking links? (true/false)
      show_social: true
      # Show user's interests? (true/false)
      show_interests: true
      # Show user's role?
      show_role: true
      # Show user's organizations/affiliations?
      show_organizations: true

  - block: markdown
    content:
      title: Life Snapshots
      subtitle: 'Behind the Science: Events and Coffee Breaks ☕'
      text: |-
        {{< gallery album="break" >}}
    design:
      columns: '1'

#   - block: markdown
#     content:
#       title:
#       subtitle: ''
#       text:
#     design:
#       columns: '1'
#       background:
#         image: 
#           filename: coders.jpg
#           filters:
#             brightness: 1
#           parallax: false
#           position: center
#           size: cover
#           text_color_light: true
#       spacing:
#         padding: ['20px', '0', '20px', '0']
#       css_class: fullscreen
  
#   - block: markdown
#     content:
#       title:
#       subtitle:
#       text: |
#         {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
#     design:
#       columns: '1'

#   - block: logos
#     content:
#       title: Collaborator
#       subtitle: Affiliations of authors who collaborate with this laboratory
#       # Path to the logo images within the `assets/media/` folder
#       logo_folder: 
#     design:
#       columns: '1'

  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: 
      email: zhangxueli@gdph.org.cn
      address:
        street: No. 106, Zhongshan 2nd Road
        city: Guangzhou
        region: Guangdong
        postcode: '510000'
        country: China
        country_code: CN
      coordinates:
        latitude: '23.127761'
        longitude: '113.281932'
    #   directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
      office_hours:
        - 'Monday to Friday, 8:30 to 17:30'
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