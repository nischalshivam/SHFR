# FR-01 — LINGUISTIC RULES (Knowledge File) — v1.1
(v1.1: added §6 Structural Calques + calibrated subjonctif imparfait rule +
félon/capter entries, after the Episode 1 audit.)

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
- **Passé composé** is allowed ONLY inside spoken dialogue — plus one
  refined exception: Watson's **present-frame commentary** (when he writes
  from "now", e.g. *« Je l'ai conservé, plié contre la carte »*) correctly
  uses passé composé. Frame = PC; story = PS.

If story narration slips into passé composé (*« Holmes est allé à la
fenêtre »*), the text instantly reads as machine translation. **Zero
tolerance.**

### Subjonctif imparfait / plus-que-parfait — the CALIBRATED rule
These classical forms are an authenticity asset **only when the ear cannot
stumble on them**. The rule:
- **Allowed in narration, sparingly (max ~1 per chapter),** and ONLY forms
  that sound identical to passé simple / simple past aloud: *eût, fût, pût,
  vînt, mît,* and regular *-ât* forms (*parlât, comptât*). To a listener
  these read as smooth classical French.
- **Forbidden everywhere:** forms that sound odd or ambiguous aloud —
  *visse, vinssent, eussions, eusse(s), fusse(nt), pussions…* Restructure
  the sentence instead (infinitive: *avant même de voir l'homme* ·
  subjonctif présent · or reshape the clause).
- **In dialogue:** only elevated-register speakers (Holmes, Vesper Lyle,
  aristocrats) may use the allowed forms. Middle- and working-class
  speakers take subjonctif présent (*« qu'un dentiste en approche »*).
- The native calibration reviewer's Episode 1 verdict overrides this
  default if they judge otherwise.

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
  articula, glissa.* Keep tags lean — no adverb stuffing.
- **Action beats between lines** go on their **own paragraph without a
  tiret** (see FR-02). This keeps TTS from mistaking an action for a new
  speaker.
- Ping-pong rhythm: trade lines; no monologue over ~4 sentences except the
  final reveal.

## 4. ACTIVE VOICE / « ON »
English passive constructions must not survive as calques. *"The book was
stolen from him"* → **« On lui a volé le livre »** (dialogue) / **« On lui
avait volé le livre »** (narration) — never repeated *« a été volé par… »*
patterns. French literature runs on active voice and *on*.

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
| a felon | un félon (= a traitor) | **un criminel / un condamné** |

Genre vocabulary (get these right): clue → **un indice** · red herring →
**une fausse piste** · culprit → **le coupable** · witness → **un témoin** ·
landlady → **la logeuse** · crime scene → **les lieux du crime** (period;
not the modern *scène de crime*) · case → **une affaire / une enquête** ·
life-insurance money → **une assurance sur la vie / une police
(d'assurance)** — never *« de l'argent sur sa vie »*.

## 6. CALQUES STRUCTURELS — English skeletons under French words ⭐
The deepest failure layer, and the subtlest AI-tell. Every word is French,
the grammar is correct — but the sentence's SKELETON (its collocations, its
idiom architecture) is still English. Word-level rules (§5) cannot catch
these; only a structure check can. All examples below occurred in real
output:

| English skeleton | ❌ Calque | ✓ Native rebuild |
|---|---|---|
| "no deceit **in him**" (traits) | Il n'y a pas de tromperie **en lui** | Il n'y a **chez lui** nulle tromperie |
| "money **on his life**" | de l'argent **sur sa vie** | une **assurance sur la vie** / une police |
| "There is nothing in that." | Il n'y a rien là. | **Rien de plus ordinaire.** / Il n'y a là rien que de très ordinaire. |
| "an **ugly** arithmetic" | une **laide** arithmétique | une **vilaine** arithmétique |
| "had not the **spine** to stand" | il n'avait pas **l'échine** de | il n'avait pas **le cran** de |
| "emptied it of our quarry" | en aurait **vidé** notre gibier | en aurait **chassé** notre gibier |

The rules behind the table:
- **Traits & qualities live « chez » someone, not « en » someone.** *Il y a
  chez lui une grande bonté* — never *en lui* for character.
- **Adjective–abstract-noun collocations:** *laid* rarely pairs with
  abstractions in French. For "ugly + abstract" use **vilain / triste /
  sinistre** (*une vilaine affaire, un triste calcul*).
- **Body-part idioms never transfer.** English spine/backbone/stomach
  idioms → French *le cran, les reins solides, le cœur de*. Translate the
  MEANING of the idiom, never its anatomy.
- **Flat existentials:** bare *« Il n'y a rien là »* is oral, not literary.
  Literary French fronts *là* or reshapes: *« Il n'y a là rien que de… »*,
  *« Rien de plus ordinaire »*.
- **Modern-signal verbs** (correct French, wrong century/register for a
  Watson narration): *capter* (a smell/a look → **saisir, percevoir,
  « cela me parvint »**), *scanner, gérer, stresser, impacter, réaliser*
  (for "realize").
- **THE STRUCTURE TEST (run on every paragraph in QC):** ask of each
  sentence — *"Would a French novelist have BUILT this thought this way, or
  only worded it this way?"* If the skeleton is English, **rebuild the
  sentence; don't re-dress it.**

## 7. ANGLICISM CALQUES — BANNED
*faire sens* (→ **avoir du sens**) · *être en charge de* (→ **être chargé
de**) · *impacter* (→ **toucher, frapper, peser sur**) · *en termes de* (→
**en matière de / quant à**) · *juste* as filler ("c'est juste étrange" →
**c'est proprement étrange / tout simplement étrange**) · *définitivement*
for "definitely" · *opportunité* for "occasion" · *réaliser* for "se rendre
compte".

## 8. MODERN WORDS — BANNED (period ~1880–1905)
*OK · week-end · stresser / le stress · job · sympa · au final · du coup ·
ça craint · pas de souci*. Convey period through vocabulary, not archaism
overload — the Channel Bible's rule ("period-flavored but accessible")
applies in French too.

## 9. FRENCH AI-CLICHÉ BANS (the French cousins of the English banned list)
*se plonger dans* (as "delve") · *une tapisserie de* · *un labyrinthe de
mensonges* · *telle une symphonie* · *chatoyant* · *éthéré* · *palpable*
(*la tension était palpable*) · *un frisson lui parcourut l'échine / le dos*
· *il était loin de se douter que / il ne se doutait pas encore que* ·
*les ombres dansaient / jouaient* · *un témoignage de* (as "a testament to")
· *cela étant dit* · *un silence assourdissant* · *la vérité éclata au grand
jour*. Write plain, concrete, period-natural French.

## 10. REGISTER BY CLASS (le niveau de langue)
- **Holmes:** français soutenu — precise vocabulary, inversion in questions
  (*« Qu'en dites-vous ? », « Avez-vous remarqué la boue sur ses
  bottines ? »*), occasional ne explétif (*avant que la maison ne soit
  éveillée*). At most one or two quiet aphorisms per episode.
- **Watson (narrator):** cultivated but warm — see FR-02.
- **Working-class characters (Cobb, cabmen, servants):** short, plain,
  concrete sentences; *est-ce que* questions acceptable; **NO heavy argot
  parisien, NO eye-dialect** — class shows through word choice and rhythm,
  never broken spelling (TTS rule). Cobb's dropped *ne* is his one
  permitted marker — a few times per scene at most.
- **Officials (Lestrade, Thorne):** correct, slightly stiff, professional.

## 11. FOISONNEMENT (French runs longer — let it)
French is naturally **15–20% longer** than English. Do NOT compress to match
English sentence lengths — compression produces choppy, robotic French. Let
sentences breathe and flow. BUT: the expansion must come from **French
syntax**, never from added content, invented atmosphere, or padding.

## 12. IDIOM RE-ENGINEERING
Never translate an idiom literally. Replace with the natural French
equivalent or plain period phrasing: *"raining cats and dogs"* → **il
pleuvait des cordes** · *"dead of night"* → **au cœur de la nuit** ·
*"caught red-handed"* → **pris la main dans le sac** · *"a fortnight"* →
**quinze jours**. English directness may become French elegance (*"He
looked angry"* → **« Son visage s'assombrit »**) — but keep FR-02's
restraint: elegant, never purple. London-specific images may be adapted to
equivalents a French listener knows (*"between the Pool and the Park"* →
**« de la Tour à Hyde Park »**) — keep the local colour where it stays
legible.

## 13. TYPOGRAPHY
Standard French spacing before **? ! :** (*« Qui est là ? »*). Semicolons
are BANNED regardless of French typographic tradition — FR-03 (TTS) wins.
Ellipsis (…) sparing, for trailing hesitation. Em-dash mid-sentence for a
sharp break is fine; don't confuse it with the dialogue tiret at line start.
