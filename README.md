# Fieldnotes

An editorial [Masthead](https://github.com/JoeriDijkstra/masthead) theme for
indie blogs and small journals: a photo-led grid of stories, tall condensed
headlines in capitals, and an unhurried reading page. No JavaScript.

## The journal

**New page → Theme page → Journal**, then set it as the site homepage. Every
post becomes a card: featured photo, tags, title and excerpt, centred. The
plain homepage (`index`) renders the same grid.

| Field | What it does |
|---|---|
| Show page title | Prints the page title above the grid. Off = photos first |
| Intro | A short line under the title. Empty = skipped |
| Show tag filter | A row of tag links above the grid (`?tag=`) |
| Show site navigation | Hide the nav bar on this page only |

## Posts

| Field | What it does |
|---|---|
| Featured image | The card photo in the grid and the photo at the top of the post |
| Featured image alt text | Describes the photo for screen readers |
| Caption | Small line under the photo — a credit or `Shot on 35mm, Portra 400` |
| Featured image on the post | `wide` (default), `full` (edge to edge), `column` (text width), `hidden` (card only) |
| Search description | Overrides the excerpt in meta / social previews |

A post reads: tags → title → excerpt as a dek → date → photo → body. Blockquotes
become large pull quotes, `##` headings are set in the headline face, and a
paragraph that is only **bold text** is treated as an interview question
(tight to its answer). Under the post, up to three more stories from its first
tag (or the latest posts) — toggle with **Show "more stories"**. Posts without
a featured image render as text-only cards.

## Tokens

| Group | Tokens |
|---|---|
| Appearance | `paper`, `ink`, `accent`, `favicon` — muted and rule tones are mixed from paper + ink |
| Typography | `heading_font` (Oranienbaum, Bodoni Moda, Playfair Display, Cormorant Garamond), `body_font` (Newsreader, Hanken Grotesk) |
| Journal | `columns` (2 / 3), `card_shape` (natural / portrait / square), `show_search`, `show_tags` |
| Posts | `drop_cap`, `show_more` |
| Social | `instagram_url`, `pinterest_url`, `behance_url`, `email` — icons appear in the nav when set |

## Development

```bash
masthead preview     # sample journal in preview/ + preview.json
masthead validate
masthead package
```

Pins `"render_version": "v1"`: page settings are read as
`page.page_options.<key>`, post settings as `post.post_options.<key>`.
