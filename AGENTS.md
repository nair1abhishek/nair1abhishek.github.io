# Agent guidance

The style guide is for agents and must not be published as a site page. Keep HTML diagrams accessible and responsive when adding them to articles or notes.

Use diagrams when relationships or sequences are easier to understand visually. Keep the message simple and explain the essential idea in the surrounding text.

## Principles

- Give each diagram a short caption and a meaningful text description. Do not rely on color alone.
- Use actual text in HTML rather than text baked into an image. Label arrows when their meaning is not obvious.
- Keep contrast high and use the existing palette and classes so diagrams feel at home on the site.
- Let sequences wrap or stack on small screens. For wide tables, use a horizontally scrollable container.
- Keep content in a logical reading order for keyboard and screen-reader users. Decorative arrows should use `aria-hidden="true"`.

These principles follow the [W3C guidance for complex images](https://www.w3.org/WAI/tutorials/images/complex/) and [WCAG guidance on use of color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html).

## Flow diagram

A visitor submits a request, the application processes it, and the result is stored.

Paste this HTML into a Markdown article or note, leaving blank lines around it:

```html
<figure class="diagram">
  <div class="diagram-flow">
    <div class="diagram-node">1. Request</div>
    <span class="diagram-arrow" aria-hidden="true">→</span>
    <div class="diagram-node">2. Process</div>
    <span class="diagram-arrow" aria-hidden="true">→</span>
    <div class="diagram-node">3. Store</div>
  </div>
  <figcaption>Request → process → store.</figcaption>
</figure>
```

## Comparison diagram

For comparisons, use a semantic table with headings. The wrapper allows scrolling when needed.


For more complex diagrams, include a longer explanation immediately before or after the figure. The sample styles are regular HTML and CSS, so no JavaScript or external rendering service is needed.
