---
name: process-orderflow-images
description: Convert screenshot images from Carmine Rosato's order flow YouTube course into structured Obsidian notes. Use when the user wants to process new images from the course into the vault.
---

# Process Order Flow Images

Convert new screenshot images from Carmine Rosato's order flow course into the existing Obsidian note structure.

## Vault Paths

- **Image inbox:** `/Users/phuynh/Library/Mobile Documents/iCloud~md~obsidian/Documents/pierre-icloud-vault/Trading/Carmine-orderflow-playlist/images-to-process-into-notes/`
- **Image log:** `/Users/phuynh/Library/Mobile Documents/iCloud~md~obsidian/Documents/pierre-icloud-vault/Trading/Carmine-orderflow-playlist/_image-log.md`
- **Notes folder:** `/Users/phuynh/Library/Mobile Documents/iCloud~md~obsidian/Documents/pierre-icloud-vault/Trading/Carmine-orderflow-playlist/`

## Note Files (topic-based)

| File | Content |
|------|---------|
| `Carmine OF - 01 Auction Theory.md` | Market mechanics, passive vs aggressive, order types |
| `Carmine OF - 02 Footprint Chart.md` | Footprint anatomy, delta, Carmine's 3-column setup |
| `Carmine OF - 03 Order Flow Reading.md` | Signals: absorption, traps, large buyer/seller, volume tails |
| `Carmine OF - 04 Trade Setups.md` | Concrete setup examples with entry logic |

Add new topic files if a batch of images introduces a genuinely new topic area (e.g., a new episode covering a distinct concept). Name them `Carmine OF - 05 <Topic>.md`.

## Workflow

1. **List all images** in the inbox folder using `ls`.

2. **Check the log** — read `_image-log.md` and extract filenames already in the Processed table.

3. **Identify unprocessed images** — any file in the inbox not in the Processed table.

4. If there are **no unprocessed images**, tell the user and stop.

5. **Read each unprocessed image** using the Read tool (it handles jpegs visually).

6. **Determine the topic** for each image based on content:
   - Auction theory, bid/ask, passive/aggressive → `01 Auction Theory`
   - Footprint chart anatomy, delta, columns → `02 Footprint Chart`
   - Absorption signals, traps, volume tails, large buyer/seller → `03 Order Flow Reading`
   - Concrete chart examples with entries/exits → `04 Trade Setups`
   - New distinct topic → create a new numbered note file

7. **Add content to the appropriate note** using Edit (append to the relevant section or add a new section). Preserve the existing structure and wikilinks. Keep notes concise — capture the key insight, not a transcript.

8. **Update `_image-log.md`** — move each processed image from Pending (or add it directly) to the Processed table with today's date and the note file name.

## Content Guidelines

- Capture the **core concept or rule**, not a word-for-word transcript
- Use bullet points and tables — these notes are for review, not reading
- Bold key terms on first use
- Preserve wikilinks between note files (`[[Carmine OF - 02 Footprint Chart]]` etc.)
- If an image is a chart example with annotations, describe what's being demonstrated and what the takeaway is
- If an image is a slide/text, convert it faithfully with the key points highlighted

## Handling Ambiguity

- Image covers multiple topics → add content to each relevant note
- Image is a duplicate/near-duplicate of content already in a note → skip and mark as processed with note "(duplicate)"
- Image content is unclear → add it to `04 Trade Setups` as a chart example with a description of what's visible, and note "(needs review)"
