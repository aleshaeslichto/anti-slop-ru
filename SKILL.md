---
name: anti-slop-ru
description: >-
  Edit, proofread, or audit Russian prose while preserving meaning, facts, register, and author voice. Use for requests like «сделай текст живее/естественнее/понятнее», «перепиши по-человечески», «причеши текст», «пахнет ChatGPT/нейросетью», «убери нейроязык», «перепиши без воды и штампов», «вычитай и поправь», or «что здесь звучит искусственно?». Route by intent: full edit, light proofreading, audit only, or targeted fix. If asked to make formal prose livelier, preserve its official/business register and necessary terms; do not make it colloquial. Treat «убери канцелярит» as a narrow request, not the default trigger. Also use when drafting Russian prose. See references/triggers.md.
metadata:
  license: MIT
  trigger: Writing or editing Russian prose; de-AI-ing Russian drafts
---

# Anti-Slop RU

Eliminate predictable AI writing patterns from Russian prose.

Russian AI text has its own fingerprints. English slop runs on em-dashes and "at its core"; Russian slop runs on **канцелярит** (officialese), nominalization, copula crutches («является», «данный»), genitive chains, empty superlatives, calques from English, and overloaded dashes. The rules below target those.

## Choose the User's Intended Mode

Read the user's wording as an intent, not as a keyword checklist. Russian users often describe the result they want («сделай живее», «текст какой-то деревянный») rather than name an editing category. Use [references/triggers.md](references/triggers.md) for examples and route as follows:

- **Full stylistic edit (default when the user asks to make the text more natural):** requests like «сделай текст живее», «перепиши по-человечески», «пахнет нейросетью», «убери нейроязык». Clean relevant patterns throughout while preserving meaning and author voice.
- **Light proofreading:** «вычитай», «поправь текст», «проверь и исправь ошибки». Fix language and obvious awkwardness; do not perform a full rewrite unless requested.
- **Audit only:** «что здесь звучит неестественно?», «найди штампы, но не переписывай», «проверь, не пахнет ли нейросетью». Quote the relevant passages and briefly explain; do not alter the text.
- **Targeted edit:** «убери повторы», «сократи воду», «упрости официальные обороты». Change only the named issue. «Убери канцелярит» belongs here, not as a generic trigger for all editing.
- **Register-constrained edit:** «сделай живее, но оставь официальный/деловой тон», «упрости, но сохрани термины». Keep the requested register, terminology, and necessary formal conventions. Make the syntax clearer; do not turn the text into casual speech. “Livelier” does not mean “colloquial.”

If the request is just «проверь текст» and the intended depth is unclear, ask whether the user wants comments only, proofreading, or a full stylistic edit. If the user says not to rewrite, honor that even if other wording suggests a full edit.

## Interpret Natural Requests, Not Editing Jargon

Users often describe the result they want rather than name a copy-editing category: «сделай текст живее и понятнее», «сейчас сухо/деревянно», «перепиши нормальным языком», «убери нейроязык», «причеши». Read any accompanying constraints as part of the task: «смысл и цифры оставь», «не добавляй ничего от себя», «сохрани официальный тон», «сделай разговорнее», «только отметь, не переписывай», or «выведи только готовый текст».

“Lively, simple, and readable” means remove empty setup, inflated phrasing, repetition, and avoidable complexity. It does **not** automatically mean informal, chatty, or humorous. Only make it conversational when the user asks for that tone. A prompt may also call out specific symptoms—pompous openers, formulaic contrasts, choppy fragments, too many dashes or quotation marks, generic claims, or bureaucratic wording. Treat them as contextual clues, not blanket bans: do not delete every «это», dash, quotation mark, list, or three-part phrase when it carries meaning or serves the genre.

For an edit, return the revised text directly by default; omit a preamble, self-evaluation, or change log unless requested. In audit mode, return the quoted findings and explanations only, never a rewritten passage.

## Core Rules

1. **Cut throat-clearing and meta-commentary.** Russian AI leads with announcements instead of content: «Стоит отметить, что…», «Важно отметить, что…», «Важно понимать, что…», «Нельзя не отметить…», «Следует подчеркнуть…», «Можно с уверенностью сказать…». Cut the lead-in, keep the claim. Same for chatbot closers: «Надеюсь, это было полезно», «Если у вас остались вопросы, обращайтесь». See [references/phrases.md](references/phrases.md).

2. **De-nominalize. Kill канцелярит.** The #1 Russian AI marker. LLMs convert verbs into abstract nouns and pad the sentence: «осуществление проверки документов» instead of «проверили документы», «принятие решения о запуске» instead of «решили запустить». Unpack the nominalization back into a verb. Watch especially for **genitive chains** — three or more nouns stacked in genitive: «процесс оптимизации системы мониторинга производительности». Break them. See [references/structures.md](references/structures.md).

3. **Kill the copula crutches «является» and «данный».** «Данный подход является эффективным» → «Этот подход эффективен». «Продукт является решением проблемы» → «Продукт решает проблему». «Данный/данная/данное/указанный/вышеупомянутый» → «этот/эта/это». Exception: in scientific and legal writing «является» and «данный» are the norm of the register — leave them there (see Rule 9).

4. **Break formulaic structures.** Russian AI loves: «Не просто X, а Y», «Не только X, но и Y», «Это не X — это Y», negative listings («Это не инструмент. Это не процесс. Это философия»), abstract triads («Быстро. Надёжно. Удобно.»). State Y directly. Two items beat three. See [references/structures.md](references/structures.md).

5. **Use active voice with a human subject.** Russian passives and impersonals hide the actor: «Осуществляется контроль качества», «Было отмечено, что…», «Производится оценка ситуации». Name the person who does the thing. Inanimate subjects doing human verbs («Событие подчёркивает», «Тренд отражает», «Данные говорят нам») mean the author avoided naming an actor — name them.

6. **Be specific. Drop empty superlatives.** «Революционный», «уникальный», «беспрецедентный», «инновационный», «непревзойдённый», «ключевой», «новая реальность» without a fact to back them up are noise. Add the specific fact («снизили ошибки на 40%») or cut the adjective. No «в значительной степени» — give the number.

7. **Cut English calques.** Russian AI translates English idioms literally and they land as translationese: «в конце дня» ("at the end of the day"), «давайте нырнём» ("let's dive in"), «на одной странице» ("on the same page"), «разблокировать потенциал» ("unlock potential"), «это меняет игру» ("it's a game changer"), «двигатель роста», «на следующем уровне». Replace with plain Russian: «в итоге», «разберёмся», «понимаем одинаково», «использовать сильнее», «многое меняет». See [references/phrases.md](references/phrases.md).

8. **Vary rhythm. Tame the dash.** Unlike English, Russian legitimately uses the em-dash — the rule is not "no dashes" but **no dash overload**: two or more dashes per sentence, or mirror chains («Скорость — выше. Качество — стабильнее. Риски — ниже.»). Replace with commas, periods, or restructure. Also break equal-length paragraphs, uniform bullet lists, and identical section endings.

9. **Respect register and the author's voice.** Calibrate to the text before editing (see Voice Calibration below). In academic, scientific, and legal writing, «является», «данный», «таким образом», and restrictive formality are the *norm* — do not strip them there. Do not flatten an author who writes with long dashes into comma-comma-comma. The goal is removing AI marks, not imposing one bland style.

10. **Trust readers. Cut quotables.** State facts directly. Skip softening and justifications. If a sentence reads like a pull-quote it probably came from a template — rewrite it. Cut lazy absolutes («все всегда», «никогда», «каждый»).

11. **Lock the facts and proofread the seams.** Preserve numbers, names, dates, claims, attributions, uncertainty, and cause-and-effect relations. Never add examples, promises, evidence, or a more specific scenario just to make prose feel vivid. After cutting or joining sentences, check punctuation and syntax: do not create a comma splice by joining independent clauses with a comma. In Russian, choose a period, semicolon, colon, or a conjunction that preserves the source relation.

## Voice Calibration

Before editing, determine the author's register and habits (ask, infer from the text, or use samples the user provides):

- Address: «ты» or «Вы» (keep it consistent).
- Dash style: em-dash with spaces, en-dash, or hyphen (some authors genuinely write with long dashes — respect it, do not "fix" a personal style).
- Quotation marks: «ёлочки», „лапки", or straight quotes (keep the author's).
- «Ё»: rendered or not, consistently.
- Sentence length and formality level: an academic text stays formal; a Telegram post stays loose.

If the user gives samples of their writing, match those patterns — but **do not invent** liveliness the source doesn't have. Never add facts, numbers, or images that aren't in the source text.

## Quick Checks

Before delivering any edited Russian prose:

- Any «является»? In 9 of 10 cases a verb or a dash does it better — or it's removable entirely.
- Any «данный/указанный/вышеупомянутый»? → «этот/эта/это».
- Any «Стоит отметить, что / Важно отметить / Следует подчеркнуть»? Cut the lead-in, keep the claim.
- Any genitive chain of 3+ nouns? Break into a verb or two short sentences.
- Any «Не просто X, а Y» / «Не только X, но и Y» / «Это не X — это Y»? State Y directly.
- Any abstract triad («быстро, надёжно, удобно»)? Make it two items, or be specific.
- Any empty superlative («революционный», «уникальный», «ключевой»)? Add the fact or cut the word.
- Any English calque («в конце дня», «давайте нырнём», «на следующем уровне»)? Say it in Russian.
- Any passive without an actor («осуществляется», «было отмечено»)? Find the actor, put them at the front.
- Two or more dashes in one sentence? Replace with commas or periods.
- All paragraphs about the same length / every bullet starts the same way? Break the pattern.
- Ends with «Надеюсь, это было полезно» or «В заключение…»? Cut it and end on the actual conclusion.
- Any «В современном мире» or «Технологии не стоят на месте» openers? Start with a fact, a number, or a scene.
- Did a cut or merge create a comma splice, dangling modifier, broken agreement, or unclear reference? Fix the seam without adding content.
- Did you invent a scenario, fact, promise, causal link, or concrete example that the source did not contain? Remove it.

## Scoring

Rate 1–10 on each dimension:

| Dimension | Question |
|-----------|----------|
| Directness (прямота) | Statements or announcements? |
| Rhythm (ритм) | Varied or metronomic? |
| Trust (доверие) | Respects the reader's intelligence? |
| Authenticity (аутентичность) | Sounds like a person wrote it? |
| Density (плотность) | Anything cuttable? |

Below 35/50: revise.

## Examples

See [references/examples.md](references/examples.md) for before/after transformations in Russian.

## License

MIT.
