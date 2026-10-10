---
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
summary: ""                 # one or two sentences, shown on the home page card and as the page lede
date: {{ .Date }}           # the card shows its year
group: research             # an id from data/groups.toml
weight: 10                  # order inside the group, lowest first
kind: ""                    # e.g. "Research project", "Internship, Software team", "Competition"
# period: "2024 – present"  # optional, replaces the year in the meta line
# supervisor: "Dr. …"       # optional, shown in the meta line as "Supervised by …"
# result: "1st Prize"       # optional outcome line, in the accent color
# image: thumbnail.png      # optional card image, a file next to this page (use a folder: projects/<slug>/index.md)
# links:                    # optional buttons; url can be https://…, a file next to the page, or /path under static/
#   - name: Code
#     url: ""
# build:                    # uncomment for an entry with no page of its own:
#   render: never           # the card then links to the first link, or nowhere
draft: true                 # remove when the entry is ready to publish
---
