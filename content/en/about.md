+++
# --- Front matter options recognized on this page ---

title = 'About Me'        # Shown as the <h1> and in the browser tab.

date = 2026-08-14         # Not displayed here, but Hugo uses it for sorting/ordering elsewhere.

draft = false             # true = page is excluded from the build entirely (won't appear even in menu).

layout = 'about'           # REQUIRED to get the fancy layout (Honors & Awards / Certifications /
                           # Voluntary Work sections below your bio).
                           # Points Hugo at themes/hugo-noir/layouts/_default/about.html.
                           # Without it, Hugo silently falls back to the plain single.html template
                           # (title + bio text only). That's what was happening before this line.

# Fields the theme does NOT read for this page (harmless to add, but ignored unless you
# edit themes/hugo-noir/layouts/_default/about.html yourself to use them):
#   description, summary, tags, weight, aliases, etc. — none of these are referenced
#   by the about.html template.
+++

<!--
  Everything below this line is your page's Markdown BODY. It renders as your bio, in the
  card at the top of the page, ABOVE the Honors & Awards / Certifications / Voluntary sections.
  Standard Markdown works here: ## headings, **bold**, *italic*, [links](url), lists, images.
-->

## Hello

I'm a **developer** who loves [Hugo](https://gohugo.io).

- Point one
- Point two

<!--
  The Honors & Awards, Certifications, and Voluntary Work sections below your bio do NOT come
  from this file — they're pulled from a separate data file: data/en/author.yaml (doesn't exist
  yet). Structure the theme expects there:

    honors:
      - institution: "Some University"
        title: "Some Award"
        date: "May 2020"

    certifications:
      - title: "Some Certification"
        company: "Some Company"
        date: "Valid until Jan 2025"
        url: "https://..."

    voluntary:
      - organization: "Some Charity"
        role: "Community Helper"
        period: "2021 - Present"
        description: "What you did there."
        url: "https://..."

  Without this data file, the page still builds fine — those sections just render as empty
  headers with nothing underneath.
-->
