# FR-03 — TTS / AI-NARRATION RULES, FRENCH (Knowledge File)

The French script is read by an **AI voice**. One garbled number or one
rushed pause breaks the spell for attentive audiobook listeners. Every part
must obey these rules — they are the French fork of the master system's
file 14, and they **override French typographic tradition wherever the two
conflict** (e.g. semicolons).

---

## 1. PUNCTUATION = PACING
- **Virgule** = short breath. Shape sentence rhythm with commas.
- **Point** = full stop. Prefer **short sentences**; French TTS runs out of
  breath on long multi-clause périodes. Split them.
- **Tiret (—)** mid-sentence = sharp break or interruption (distinct from
  the dialogue tiret at line start).
- **Points de suspension (…)** = trailing, hesitant pause. Sparing.
- **Paragraph break** = longer beat. Break often — audio needs air.
- **Semicolons: BANNED.** French literary tradition loves them; TTS engines
  rush them. Use a full stop.
- Standard French spacing before **? ! :** — keep it (French-trained TTS
  expects normal French typography).

## 2. NUMBERS, DATES, HOURS, MONEY — always spelled out in French words
| Written form | ✓ In narration |
|---|---|
| 1889 | **mille huit cent quatre-vingt-neuf** |
| 9:30 | **neuf heures et demie** |
| 10:45 | **onze heures moins le quart** |
| March 23rd | **le vingt-trois mars** |
| the 1st | **le premier** (only date using the ordinal) |
| £3 10s | **trois livres et dix shillings** |
| a half-crown | **une demi-couronne** |
| 5 guineas | **cinq guinées** |
| 7% | **sept pour cent** |
| 221B Baker Street | **au deux cent vingt et un B, Baker Street** |

Imperial units keep the Victorian illusion: **milles** (miles), **pieds**,
**pouces**, **yards** — never convert to kilomètres/mètres.

## 3. ABBREVIATIONS — none in spoken text
Write in full: **monsieur, madame, mademoiselle, docteur, Saint** (never
M., Mme, Mlle, Dr., St.). "Cox & Co." → rephrase (**la banque Cox, à Charing
Cross**) — the symbol **&** never appears in narration; nor do %, №, etc.

## 4. ROMAN NUMERALS — never
Rephrase: not « Édouard VII » but **« le roi Édouard »** (or spell it if the
number is essential). Chapter headings are spelled out (rule 8).

## 5. FRENCH HOMOGRAPH TRAPS — rephrase where the wrong reading is likely
- **plus** — /ply/ (no more) vs /plys/ (more): in ambiguous "more" contexts
  prefer **davantage** (*il en savait davantage*).
- **fils** — son /fis/ vs threads /fil/: context usually saves it; if both
  senses are near each other, rephrase one (**des fils de soie** → *de la
  soie filée*).
- **est** — verb vs east: fine inside *à l'est de Londres*; avoid bare
  ambiguous uses.
- **couvent / portions / As** — rare; check when they occur.
- **Subjonctif imparfait forms:** only the ear-invisible ones (*eût, pût,
  vînt, mît* — homophones of passé simple) may appear, per FR-01 §1. Never
  *visse / vinssent / eussions / fusse* — they stumble aloud; restructure
  the sentence instead.
- Avoid accidental rhymes and tongue-twisting consonant runs. **Read-aloud
  test:** if a human would stumble, the AI will too.

## 6. FOREIGN NAMES — do not fight the French voice
A French narrator pronounces « Sherlock Holmes », « Watson », « Baker
Street » with a French accent. **That is correct** — it is exactly how a
native French audiobook narrator reads them. Never respell English names
phonetically to force English pronunciation; never add pronunciation
brackets inside spoken text.

## 7. ELISION & LIAISON
Write standard, correct French — the engine handles liaison. One lock from
FR-04: **no elision before Holmes or Hudson** (*de Holmes*, never
*d'Holmes*; *de Hudson*).

## 8. CHAPTER HEADINGS — voiced, minimal, spelled out
Headings ARE read aloud (normal for audiobooks). Format:
**« Chapitre premier », « Chapitre deux », « Chapitre trois »…** — optionally
followed by a colon and a short title (*Chapitre trois : La clochette de
laiton*). Own line, blank line after.

## 9. DIALOGUE FOR THE EAR
- Tiret opens each spoken line; new paragraph per speaker.
- Action beats on their own paragraph, no tiret (see FR-02).
- In long exchanges, **re-anchor the speaker by name every few lines**
  (*répliqua Holmes*) so the listener never loses track — the ear cannot
  glance back up the page.
- Keep incises simple; the voice carries emotion, not adverbs.
- For emphasis, **rephrase** rather than rely on italics (TTS ignores them).

## 10. CLARITY HABITS
- One idea per sentence in tense moments.
- No bracketed tags of any kind inside this project's output (no SFX, no
  notes) — the deliverable is a clean voice-ready text.

---

## QUICK CHECK (run silently before delivering every part)
- [ ] No raw numerals, years, symbols, or abbreviations in spoken lines
- [ ] No semicolons; no sentence too long for one breath
- [ ] Chapter headings spelled out (« Chapitre premier »…)
- [ ] Dialogue: tirets, inversion incises, action beats on their own lines
- [ ] Homograph traps checked (plus / fils / est …)
- [ ] No phonetic respelling of English names
- [ ] Reads aloud smoothly, with the dignity of a classic translation
