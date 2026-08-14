+++
# --- Front matter options recognized on this page ---

title = 'Experience'      # Shown as the <h1> and in the browser tab.

date = 2026-08-14         # Not displayed here, but Hugo uses it for sorting/ordering elsewhere.

draft = false             # true = page is excluded from the build entirely (won't appear even in menu).

layout = 'experience'     # REQUIRED to get the fancy layout (stat boxes + timeline).
                           # Points Hugo at themes/hugo-noir/layouts/_default/experience.html.
                           # Without it, Hugo silently falls back to the plain single.html template
                           # (title + text only — no stat boxes, no timeline). That's what was
                           # happening before this line was added.

# Fields the theme does NOT read for this page (harmless to add, but ignored unless you
# edit themes/hugo-noir/layouts/_default/experience.html yourself to use them):
#   description, summary, tags, weight, aliases, etc. — none of these are referenced
#   by the experience.html template.
+++

<!--
  Everything below this line is your page's Markdown BODY. It renders as the intro
  paragraph ABOVE the four stat boxes (Technologies Used / Projects Completed / etc).
  Standard Markdown works here: ## headings, **bold**, *italic*, [links](url), lists, images.
-->

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

<!--
  The actual job/timeline entries below the intro do NOT come from this file — they're
  pulled from a separate data file: data/en/experience.yaml (doesn't exist yet).
  Structure the theme expects there, per entry:

    experience:
      - company: "Company Name"        # optional
        company_link: "https://..."     # optional — makes company name a clickable link
        role: "Job Title"               # shown as the big heading
        period: "Jan 2023 - Present"    # shown under the role
        country: "Remote"               # optional
        responsibilities:               # optional bullet list
          - "Did thing one"
          - "Did thing two"
        technologies:                   # optional pill tags
          - "Go"
          - "Docker"

  Note: if `company` is exactly "GitHub", the template auto-adds a GitHub profile link/icon —
  a hardcoded special case in the template, not something you configure.

  Without this data file, the page still builds fine — it just shows
  "No experience data found" where the timeline would go.
-->
