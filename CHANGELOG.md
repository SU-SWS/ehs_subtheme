# Environmental Health & Safety Theme

1.x-X.X
--------------------------------------------------------------------------------
_Release Date: 202X-XX-XX_

- Forked from `vpsa_ose_subtheme` and rebranded for Environmental Health &
  Safety: theme files, machine name, package/composer metadata, and display
  name are now `ehs_subtheme` / "Environmental Health & Safety".
- Homepage search bar reduced to the search field alone. Removed the
  OSE-specific related-resource links (CardinalEngage, student-org work orders,
  VSO re-registration), the contact-us block, and their styles.
- Removed the decorative `search_bg.svg` background image and the asset itself,
  along with the image-only `background-position` / `background-repeat` /
  `background-size` rules.
- Restyled to the Stanford brand palette: near-black `$su-color-black`
  (`#2e2d29`) band replacing the lagunita teal gradient, and a
  `$su-color-digital-red` hover on the submit button. No teal remains.
- Reduced the search band's `padding-top` to a flat `2.7rem` (was responsive
  6/12.6/13.3rem); `padding-bottom` stays responsive.
- Dropped the search input's border (`border: none`) now that the field reads as
  a white pill against the dark band; keyboard focus is carried by
  `outline: revert`.
- Search heading copy is now "What would you like to do today?", moved out of
  the `<label>` into the `<h2>`, with a visually-hidden label on the input so
  the field keeps an accessible name.
- Removed the inherited GitPod configuration (`.gitpod.yml`) and its README
  section.
