# Veyrath

A personal, non-commercial Chrome extension for reviewing manga and manhwa reading progress across Asura Scans and MyAnimeList. MyAnimeList remains the main reading tracker.

## Current status

Veyrath is in early development. A local read-only Asura bookmark scanner prototype is available; this repository currently serves as the project homepage. No extension release is published here yet.

The prototype reads the main bookmark grid across every page, checks the unique series count, and previews calculated reading progress. It does not open chapter readers, touch progress sliders, edit bookmarks, or update MyAnimeList. MAL sign-in, API list retrieval, and automatic syncing are not implemented yet.

## Progress rules

- Continue chapter N means N minus 1 chapters read.
- Up to Date chapter N means N chapters read.
- Latest chapter labels are ignored.
- Fractional chapters, special chapters, and ambiguous labels require review.

## Planned workflow

1. Connect to MyAnimeList through its official API and review the manga list.
2. Compare titles, alternate titles, authors, and editions before confirming matches.
3. Preview proposed transfers in both directions for approval.
4. Raise MAL chapter counts only when appropriate, preserving higher counts and existing statuses.
5. Add selected missing Asura bookmarks without changing existing reading progress.
6. Enable daily Asura-to-MAL checks only after the initial transfer is reviewed and verified.

## Privacy and credentials

The current local prototype has no analytics or external reporting. It stores its last complete preview in the local Chrome profile and can export a local JSON file. API credentials, tokens, and personal reading-list exports must not be committed to this repository or posted in issues. Future MAL authorization will use the official OAuth flow.

## Project information

Veyrath is an independent personal project and is not affiliated with or endorsed by MyAnimeList or Asura Scans.
