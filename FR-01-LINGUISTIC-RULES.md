# FR-01 — LINGUISTIC RULES (Knowledge File)

The grammar and register laws that make the French output read as **natively
written**, in the tradition of classic French Conan Doyle translations.
These are checked in the internal QC pass before every part.

---

## 1. LA RÈGLE D'OR — PASSÉ SIMPLE (the #1 AI-detector)
All **narration** uses the classic literary tense system:
- **Passé simple** for narrative actions: *je trouvai, il alla, elle
  s'assit, il eut, nous prîmes, ils entrèrent, elle murmura, il répondit.*
- **Imparfait** for description, habit, background: *la pluie tombait, il
  portait un manteau gris, elle tenait ses gants.*
- **Plus-que-parfait** for backstory: *il n'avait pas touché au petit
  déjeuner.*
- **Passé composé** is allowed ONLY inside spoken dialogue (characters speak
  naturally): *« J'ai vu cet homme hier soir. »*

If narration slips into passé composé (*« Holmes est allé à la fenêtre »*),
the text instantly reads as machine translation. **Zero tolerance.**

Nuance: **subjonctif présent** is welcome in elevated speech; **subjonctif
imparfait** (*qu'il fût, qu'il vînt*) — avoid: it sounds stiff to modern
listeners and fights the "period-flavored but accessible" brief.

## 2. VOUVOIEMENT — ABSOLUTE
All adults of the era address each other as **vous** — including Holmes and
Watson, however close their friendship. Clients, police, suspects, servants:
vous, always. **Tutoiement is forbidden** except an adult addressing a young
child (and even then, prefer vous unless intimacy demands it — flag it if
used). AI loves to slide Holmes/Watson into "tu" to show friendship; that is
a register disaster in a Victorian setting.

## 3. DIALOGUE MECHANICS
- Each spoken line opens with a **tiret cadratin (—)** on a new paragraph.
  No guillemets around dialogue lines.
- **Incises use inversion, always:** *dit-il, répondit-elle, murmura Holmes,
  répliqua-t-il, fit Watson.* Never *« … », il a dit.*
- **Verb variety** in incises — rotate naturally, don't stack the same verb:
  *dit, fit, répondit, répliqua, murmura, souffla, s'écria, gronda, observa,
  reprit, poursuivit, lança, demanda, s'enquit, admit, concéda, trancha,
  articula, glissa.* Keep tags lean — no adverb stuffing (*dit-il
  froidement* occasionally; the voice actor carries emotion).
- **Action beats between lines** go on their **own paragraph without a
  tiret** (see FR-02 for the pattern). This keeps TTS from mistaking an
  action for a new speaker.
- Ping-pong rhythm: trade lines; no monologue over ~4 sentences except the
  final reveal.

## 4. ACTIVE VOICE / « ON »
English passive constructions must not survive as calques. *"The book was
stolen from him"* → **« On lui a volé le livre »** (dialogue) / **« On lui
avait volé le livre »** (narration) — never *« Le livre a été volé par… »*
patterns repeated through the text. French literature runs on active voice
and *on*.

## 5. FAUX AMIS — the silent killers (sweep every part)
| English | ❌ Wrong French | ✓ Correct |
|---|---|---|
| evidence | l'évidence | **les preuves** |
| actually | actuellement | **en fait / à vrai dire** |
| eventually | éventuellement | **finalement / à la longue** |
| to deceive | décevoir | **tromper / duper** |
| injury / to injure | injure / injurier | **blessure / blesser** |
| library | librairie | **bibliothèque** |
| a lecture | une lecture | **une conférence** |
| sensible | sensible | **sensé / raisonnable** |
| to pretend | prétendre | **feindre / faire semblant** |
| to attend | attendre | **assister à** |
| to demand | demander | **exiger** |
| physician | physicien | **médecin** |
| to achieve | achever | **accomplir / réussir** |
| comprehensive | compréhensif | **complet** |
| to introduce (someone) | introduire | **présenter** |
| to realize | réaliser | **se rendre compte / comprendre** |
| definitely | définitivement | **assurément / sans aucun doute** |
| opportunity | opportunité | **occasion** |
| to support | supporter | **soutenir / appuyer** |
| versatile | versatile | **polyvalent** |

Genre vocabulary (get these right): clue → **un indice** · red herring →
**une fausse piste** · culprit → **le coupable** · witness → **un témoin** ·
landlady → **la logeuse** · crime scene → **les lieux du crime** (period;
not the modern *scène de crime*) · case → **une affaire / une enquête**.

## 6. ANGLICISM CALQUES — BANNED
*faire sens* (→ **avoir du sens**) · *être en charge de* (→ **être chargé
de**) · *impacter* (→ **toucher, frapper, peser sur**) · *en termes de* (→
**en matière de / quant à**) · *supporter* for "endure people" misuse ·
*juste* as filler ("c'est juste étrange" → **c'est proprement étrange /
tout simplement étrange**) · *définitivement* for "definitely" ·
*opportunité* for "occasion" · *réaliser* for "se rendre compte".

## 7. MODERN WORDS — BANNED (period ~1880–1905)
*OK · week-end · stresser / le stress · job · sympa · au final · du coup ·
ça craint · pas de souci*. Convey period through vocabulary, not archaism
overload — the Channel Bible's rule ("period-flavored but accessible")
applies in French too.

## 8. FRENCH AI-CLICHÉ BANS (the French cousins of the English banned list)
*se plonger dans* (as "delve") · *une tapisserie de* · *un labyrinthe de
mensonges* · *telle une symphonie* · *chatoyant* · *éthéré* · *palpable*
(*la tension était palpable*) · *un frisson lui parcourut l'échine / le dos*
· *il était loin de se douter que / il ne se doutait pas encore que* ·
*les ombres dansaient / jouaient* · *un témoignage de* (as "a testament to")
· *cela étant dit* · *un silence assourdissant* · *la vérité éclata au grand
jour*. Write plain, concrete, period-natural French.

## 9. REGISTER BY CLASS (le niveau de langue)
- **Holmes:** français soutenu — precise vocabulary, inversion in questions
  (*« Qu'en dites-vous ? », « Avez-vous remarqué la boue sur ses
  bottines ? »*), occasional ne explétif (*avant que la maison ne soit
  éveillée*). At most one or two quiet aphorisms per episode.
- **Watson (narrator):** cultivated but warm — see FR-02.
- **Working-class characters (Cobb, cabmen, servants):** short, plain,
  concrete sentences; *est-ce que* questions acceptable; **NO heavy argot
  parisien, NO eye-dialect** — class shows through word choice and rhythm,
  never broken spelling (TTS rule).
- **Officials (Lestrade, Thorne):** correct, slightly stiff, professional.

## 10. FOISONNEMENT (French runs longer — let it)
French is naturally **15–20% longer** than English. Do NOT compress to match
English sentence lengths — compression produces choppy, robotic French. Let
sentences breathe and flow. BUT: the expansion must come from **French
syntax**, never from added content, invented atmosphere, or padding.

## 11. IDIOM RE-ENGINEERING
Never translate an idiom literally. Replace with the natural French
equivalent or plain period phrasing: *"raining cats and dogs"* → **il
pleuvait des cordes** · *"dead of night"* → **au cœur de la nuit** ·
*"caught red-handed"* → **pris la main dans le sac**. English directness may
become French elegance (*"He looked angry"* → **« Son visage s'assombrit »**)
— but keep FR-02's restraint: elegant, never purple.

## 12. TYPOGRAPHY
Standard French spacing before **? ! :** (*« Qui est là ? »*). Semicolons
are BANNED regardless of French typographic tradition — FR-03 (TTS) wins.
Ellipsis (…) sparing, for trailing hesitation. Em-dash mid-sentence for a
sharp break is fine; don't confuse it with the dialogue tiret at line start.
