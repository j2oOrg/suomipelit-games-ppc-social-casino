# Directive: Content Rewording Plan for Social Casino Site

## Scope and constraint
- Reword only existing copy to reduce textual overlap while preserving:
  - current HTML/CSS/JS structure,
  - routes,
  - existing functional behavior.
- Do **not** introduce new functional components (no new age gate, no extra forms, no extra navigation, no new legal pages).
- Keep all existing legal disclaimers that classify the product as social casino.
- Target market and copy baseline: **Finland (FI)**.
- Keep current footer legal notice structure and text locations unchanged.

## Content surface reviewed
- Files identified for rewording:
  - `index.html`
  - `about.html`
  - `contact.html`
  - `privacy-policy.html`
  - `terms-of-service.html`
  - `games/book-of-cleo.html`
  - `games/bloodaxe.html`
  - `games/rooster-mobs-slot.html`
- Shared repeated text also appears in:
  - cookie banner modal messages,
  - footer notice,
  - newsletter blocks,
  - legal section intros.

## Google Ads / social casino language safety rules
Before editing any copy, enforce these rules everywhere:
- Explicitly state that this is social/entertainment only in at least one visible legal context.
- Remove/avoid phrases that imply guaranteed payouts, guaranteed wins, unlimited riches, or cash/poker/gambling as outcome.
- Use neutral "play" wording, not "bet", not "real money", not "real prizes", not "profit."
- Keep age statement factual and unchanged in intent (18+ audience).
- Keep disclaimers for gambling support where already linked (`BeGambleAware`, `GamCare`, `GamblingTherapy`) unless link set is intentionally revised.

Mandatory phrase list to avoid (no exceptions):
- gambling platform, gambling site, bet, betting, bet here, real money, real-money, real money gambling, casino gambling, bet-based, wagering, wager, wagering mechanics, wager-based features, pay-to-play, paid rewards
- winning, win, winner, guaranteed win, guaranteed victory, guaranteed rewards
- jackpot, prize money, cash prize, payout, payout ratio, return to player, RTP, financial rewards, money-based outcomes, financial outcomes
- money prize, bankroll, profit, guaranteed profits
- deposit, withdrawal, reward money
- unlimited riches, sure win, instant win, biggest chance
- finnish equivalents (if used): `voitto`, `rahakasino`, `panos`, `rahapalkinto`, `rahalla`

## Rewording plan (by section, preserve structure)
1. Create a replacement matrix (current line → proposed line) per file before editing.
2. Start with shared/legal text used across multiple pages to get maximum de-risk consistency:
   - cookie banner.
   - footer “IMPORTANT NOTICE”.
   - quick links/section headings.
   - newsletter intro + CTA.
3. Normalize copy quality in page-specific blocks:
   - homepage advantage cards,
   - about “About Us” description,
   - contact status/success copy,
   - privacy and terms section lead-ins,
   - game description paragraphs.
4. Keep exact structure and markup unchanged except inner text (and harmless punctuation tweaks).

## Suggested wording strategy (safe baseline)
- Rewriting approach is **full rewrite** for all repeated/shared copy blocks, not only minor substitutions.
- Replace hard “marketing claim” wording with:
  - “Fun-first social slots” instead of “Completely Free Social Casino” if needed.
  - “Entertainment-focused gaming” instead of “unlimited riches”/“great victories.”
  - “No real-value outcomes, no betting-style mechanics, no cash-oriented reward systems” for all legal-sensitive areas.
- Update cookie/CTA labels to one consistent English style across pages (example: `Accept` / `Decline`, `Subscribe` / `Subscribe Now`).
- Replace duplicated intro descriptions with equivalent but not identical phrasing to reduce duplicate-index overlap.

## Implementation order (no behavior changes)
1. Build draft replacements in this file section-by-section (one block per page).
2. Apply text updates page-by-page in this order:
   - Shared/legal blocks first (`privacy-policy.html`, `terms-of-service.html`, footer notice),
   - then `index.html`,
   - `about.html`,
   - `contact.html`,
   - each game landing (`book-of-cleo`, `bloodaxe`, `rooster-mobs-slot`).
3. Keep game iframe/scripts, file paths, classes, IDs, buttons, and script hooks unchanged.

## Verification checklist
- Confirm no references remain to prohibited claims like guaranteed winnings or real-money framing.
- Confirm every page still includes social-casino-only language.
- Confirm no new files or page routes were introduced.
- Confirm footer/legal areas still match links and disclaimers.
- Confirm existing 18+ messaging remains present and unchanged in intent.

## Resolved user input
1. Target region: **Finland (FI)**.
2. Mandatory phrase list: **added** in this directive as a hard block-list (do not use).
3. Rewriting depth: **full rewrite** for repeated/shared copy.
4. Footer legal notice: keep current structure and location exactly as-is.
5. Site-brand baseline: continue with `Suomipelit` unless changed later.
6. CTA normalization: apply consistent English labels in existing language blocks during rewrite (`Accept`, `Decline`, `Subscribe`, `Subscribe Now`) and remove mixed-language labels.
7. Keep page structure and copy placement: no new pages/sections/age-gate components.
