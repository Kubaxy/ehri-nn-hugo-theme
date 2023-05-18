Hugo theme for EHRI National Node websites
==========================================

This is a work-in-progress example EHRI National Node theme, multilingual for English and Welsh 
(apologies to Welsh speakers for the incorrect translations.)

To adapt this theme, fork the repository and change:

 - things relating to the languages in `config.yaml`
 - the equivalent translations in `i18n/cy.yaml`
 - files in the content directory ending with `.cy.md`

In the content front matter the `type` key affects the template used. If you don't specify a `type` value,
the default single page template will be used which simply renders the title and the content as markdown (or
HTML, if you want.)

Currently the following types are available:

contact:
  renders a contact form and data from the `data/people_*.yaml` files as contact cards
services:
  renders the data in `data/services_*.yaml` as a list of resource cards
partners:
  renders the data in `data/partners_*.yaml` as a list of partner cards

If you add markdown/html content to pages with these types it will render before the data driven content.

### Shortcodes

Currently supported shortcodes are:

intro
  puts any markdown between the tags inside a `<p>` tag with the `intro` class, which gives it a larger font, e.g.

```html
{{< intro >}}
The is some markdown content rendered inside a <p class="intro"></p> tag.
{{ < /intro >}}
```

---

TODO: lots more...