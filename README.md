# Radar cover + icon assets

Public image host for the Systems & Tools Radar Notion database covers and icons, and a
general-purpose logo library for decks.

- `covers/` — wide cover images, one per tool
- `icons/` — square icons, one per tool

## Using these

Link to the raw URL:

```
https://raw.githubusercontent.com/sarahcallmesmadds/radar-assets/main/icons/Salesforce.webp
```

Point Claude at a folder path and it can pick the right logo for a deck without you
hunting for one.

## Naming convention

Filenames are the contract. URLs are referenced from Notion and from decks, so **renaming
an existing file breaks live links.** Add new files, do not rename old ones.

1. **TitleCase, underscores between words.** `Google_Drive.png`, `LinkedIn_Sales_Navigator.png`.
   Lowercase brand names that are genuinely lowercase stay as they are: `n8n.png`.
2. **No dots except the extension.** A dot in the name reads as a file extension to some
   tools. Version numbers and dotted brand names use a hyphen: `Opus_4-8.webp`,
   `Otter-ai.jpg`, `Trigger-dev.png`.
3. **No spaces**, ever. They become `%20` in URLs.
4. **Real extension matching real format.** Two files arrived as `.img` and were actually
   AVIF; browsers and Notion will not render a mislabelled file.
5. **One image per tool per folder.** If you have two versions, pick the one that looks
   right at small size and keep the other locally.

## Scope

This repo is public and holds third-party product logos only. Screenshots, personal
images, and anything showing session or account content do not belong here.
