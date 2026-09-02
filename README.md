# Obsidian Snippets

A collection of focused CSS snippets for Obsidian. The Relic snippets provide a coordinated dark fantasy appearance, while the smaller utility snippets can be used independently.

## Installation

1. Download the CSS files you want to use.
2. Copy them into your vault's `.obsidian/snippets` folder.
3. Open **Settings > Appearance > CSS snippets** in Obsidian.
4. Select the refresh button, then enable the snippets.

Several snippets expose optional controls through the [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) community plugin. The CSS works without Style Settings, using its built-in defaults.

## Snippets

### `relic-style.css`

The main visual foundation for the Relic design. It combines the interface theme and heading system in one snippet.

The theme styles:

- Dark stone and worked-iron interface surfaces
- Warm gold ornamental accents
- Navigation, tabs, controls, scrollbars, links, tags, and tables
- Optional higher-contrast stone surfaces
- Optional compact table spacing
- Reading view and Live Preview presentation

The heading system provides independent controls for H1 through H6, including:

- Colour, font, and size
- Left or centred alignment
- Default, divider, underline, framed, accent, double-rule, insignia, and separator treatments
- Optional stepped indentation for the heading hierarchy

Style Settings places these controls under **Relic Style**, divided into **Theme** and **Headers** groups.

### `relic-callouts.css`

Provides the ornamental callouts and reference-image treatment used by the Relic design.

#### Edict

A formal framed callout for proclamations, oaths, laws, and important declarations.

```markdown
> [!edict] The Black Oath
> What is sealed in shadow must remain unnamed.
```

Standard foldable callout markers are supported:

```markdown
> [!edict]- Collapsed edict
> Hidden content
```

Example:

[![Edict callout example](https://i.ibb.co/mFPHC8sK/image.png)](https://ibb.co/M5JRD6TH)

#### Infobox

A floated information card with a title, feature image, section headings, captions, and compact information tables.

```markdown
> [!infobox] Settlement
> ![[settlement.jpg]]
> *View from the southern road*
>
> ## Information
> | | |
> |---|---|
> | Type | Town |
> | Population | 2,400 |
```

Example:

[![Infobox example](https://i.ibb.co/gZxx7FQG/image.png)](https://ibb.co/b5kk3RYx)

The Infobox adapts for narrow panes and integrates with nested Gallery callouts.

#### Advice

A smaller highlighted callout for guidance, hints, and reminders.

```markdown
> [!advice] Explorer's Hint
> Bring a lantern before entering the lower ruins.
```

Example:

[![Advice callout example](https://i.ibb.co/nNxhL7kW/image.png)](https://ibb.co/7ds71ny9)

#### Reference Images

Floats illustrated reference images beside text and gives them soft watercolour-style edges.

```markdown
![[image.png|reference-right|380]]
![[image.png|reference-left|320]]
```

Append `-2` or `-3` to use an alternate edge shape:

```markdown
![[image.png|reference-right-2|380]]
```

Captions can follow an image on the same rendered paragraph, or the image and caption can be placed inside a blockquote. Floating is disabled automatically on narrow screens.

Example:

[![Reference Images example](https://i.ibb.co/ZRmNFJP5/image.png)](https://ibb.co/bjJ7C3ZT)

Style Settings groups the Infobox and Reference Images controls under **Relic Callouts**.

### `inline-title-tweaks.css`

Controls the inline title displayed at the top of a note.

Features include:

- Default or Relic title treatment
- Optional italics
- Optional title shadow
- Configurable font family
- Title colour, size, and spacing variables used by compatible banner layouts

The Relic treatment uses the H1 font from `relic-style.css` when that snippet is enabled, with a suitable serif fallback when it is not.

Example:

[![Inline title example](https://i.ibb.co/wZGGqKpz/image.png)](https://ibb.co/cKff9N2r)

### `text-tweaks.css`

Provides focused controls for note text without changing the rest of the Obsidian interface.

Style Settings controls include:

- Text line height
- Space before and after headings
- Italic text colour
- Space before and after lists

The rules cover Reading view, Live Preview, and Source mode where equivalent editor markup is available.

### `hide-base-ui.css`

Hides the header and summary controls from selected embedded Obsidian Bases while leaving the Base itself visible.

Add the `no-ui` alias to a Base embed:

```markdown
![[Party.base|no-ui]]
```

Example:

[![Hidden Base UI example](https://i.ibb.co/8pfnYHv/image.png)](https://ibb.co/DyvPrZc)

Only embeds using this alias are affected.

## Recommended combinations

- Enable `relic-style.css` and `relic-callouts.css` for the complete Relic presentation.
- Add `inline-title-tweaks.css` when you want independent control over note titles.
- Add `text-tweaks.css` when you want adjustable reading density and document spacing.
- Use `hide-base-ui.css` independently whenever a Base embed should appear without its surrounding controls.

Each file remains optional, so you can enable only the parts that suit your vault.
