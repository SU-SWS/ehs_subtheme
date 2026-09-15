# [EHS Subtheme](https://github.com/SU-SWS/ehs_subtheme)
##### Version: 1.x-dev

Changelog: [CHANGELOG.md](CHANGELOG.md)

Description
---

`ehs_subtheme` is the Stanford sub-theme for **Environmental Health & Safety
(EHS)**. It works with the Stanford Basic base theme on Stanford Sites
(Drupal 10).

Machine name: `ehs_subtheme` · CSS class prefix: `ehs-`

Summary of customizations:
1. Homepage search bar on the front page (`templates/form--search.html.twig`,
   included from `templates/page--front.html.twig`; styles in
   `src/scss/components/search/_search.scss`). Originally developed by RH and
   designed by JT in 2025 for VPSA OSE, from which this theme was forked.
   Restyled for EHS in the Stanford brand near-black (`$su-color-black`,
   `#2e2d29`) with a digital red (`$su-color-digital-red`) submit hover.

History / provenance:
This repository was forked from
[`vpsa_ose_subtheme`](https://github.com/SU-SWS/vpsa_ose_subtheme) and
rebranded for EHS. The search bar was reduced to the search field alone: the
OSE-specific related-resource links (CardinalEngage, student-org work orders,
VSO re-registration), the contact-us block, the decorative background image,
and the lagunita teal palette that went with them were all removed. If EHS
wants a related-links row under the search field later, the markup and styles
need to be written fresh — see commit history for the OSE originals.

Documentation
---
See subtheming guides and best practices here: 
https://devguide.sites.stanford.edu/front-end/drupal/sub-themes 

Installation
---
1. Review the documentation link above for best practices, particularly the Do's and Don't's sections.
2. Place this repository in the site's themes directory, then enable it and set it as the default active theme.
3. Add any EHS brand colors you need (in addition to the decanter colors that are already available) to src/scss/utilities/variables/_colors.scss. 
See all the colors already available through decanter: https://decanter.stanford.edu/page/brand-design-elements-color/ 
4. If desired, add font settings if you need to override and use fonts other than decanter fonts ( https://decanter.stanford.edu/page/brand-design-elements-typography/ ),
by defining a font library in the ehs_subtheme.libraries.yml file.
5. If desired, add button mixins in src/scss/utilities/mixins/_buttons.scss with your button styles and then reference them and use them in src/scss/theme/_button.scss.
6. If desired, add cta and link mixins in src/scss/utilities/mixins/_cta.scss with your button styles and then reference them and use them in src/scss/theme/_cta.scss.
7. If you want to skin or theme a component, like a paragraph, create a _mycomponent.scss file in src/scss/components folder. Consider using a subfolder like 'cards' or 'banners' if applicable. Prefix any new classes with `ehs-`.

Configuration
---

Nothing special needed. Install, enable, and set as the default active theme.

Developer
---

If you wish to develop on this theme you will most likely need to compile some new css. Please use the sass structure provided and compile with the sass compiler packaged in this theme. To install:

```
yarn install
```
After you've made a change you want to see processed, you can run:
```
yarn build
```
This will process scss, js, and asset files, preparing them from the src directory to the dist directory.

```
yarn watch
```
This will watch the scss files and compile them upon saving.

Contribution / Collaboration
---

You are welcome to contribute functionality, bug fixes, or documentation to this theme. If you would like to suggest a fix or new functionality you may add a new issue to the GitHub issue queue or you may fork this repository and submit a pull request. For more help please see [GitHub's article on fork, branch, and pull requests](https://help.github.com/articles/using-pull-requests)
