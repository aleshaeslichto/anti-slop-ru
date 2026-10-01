# Russian Trigger Phrases and Intent Routing

Use these as examples of how people may ask for Russian editing. They are not magic keywords: infer the requested scope from the whole prompt, and honor explicit constraints over generic wording like «сделай живее».

## 1. Full stylistic edit

These usually ask for a complete but conservative cleanup. Preserve the source's facts, claims, tone, register, and authorial voice; do not invent anecdotes, details, humor, or conversational color.

- «Сделай текст живее и понятнее»
- «Перепиши по-человечески, а то звучит как ChatGPT»
- «Можешь причесать этот текст?»
- «Тут прям пахнет нейросетью. Поправь, но смысл не меняй»
- «Убери нейроязык / нейросетевой тон»
- «Сделай естественнее, сейчас слишком сухо и шаблонно»
- «Перепиши без воды и штампов»
- «Почисти текст от типичных фраз ChatGPT»
- «Сделай так, чтобы это не звучало как ответ бота»
- «Приведи текст в порядок, факты и цифры оставь как есть»
- «Текст какой-то деревянный. Сделай его легче для чтения»

«Сделай живее» describes the desired reading experience, not permission to add a personal voice. Keep neutral text neutral unless the user asks for a specific tone.

## What common cleanup requests usually contain

A natural request often combines three parts:

1. **An everyday action verb:** «отредактируй», «перефразируй», «перепиши», «поправь», «причеши», «вычитай».
2. **A desired reading experience or complaint:** «живее», «понятнее», «проще», «естественнее», «слишком сухо», «деревянно», «пахнет нейросетью», «много воды/пафоса/штампов».
3. **A scope constraint:** «смысл оставь», «факты не меняй», «официальный тон сохрани», «не делай разговорным», «только найди, не переписывай», «только готовый текст».

Use the scope constraint to choose how far to go. A general request for a clearer, livelier text does not cancel a request to preserve formality or the author's voice. Do not make users name a technical category such as «канцелярит» when they have already described the problem in ordinary words.

Commonly named symptoms include pompous time-setting openers, formulaic «не X, а Y» contrasts, strings of dramatic fragments, overused long dashes or quotation marks, repetitive lists, empty expert-sounding generalities, and heavy official phrasing. Use these as clues for what to inspect, not as automatic replacements. For example, «это», quotation marks, dashes, and three-item lists can all be entirely appropriate in context.

For a clear editing request, do the work without an unnecessary interview. Ask only when the intended scope or requested register would materially change the result.

## 2. Light proofreading

These usually ask for correction, not a full stylistic rewrite:

- «Вычитай текст»
- «Проверь и поправь ошибки»
- «Посмотри, нормально ли написано»
- «Проверь формулировки, но сильно не переписывай»
- «Поправь шероховатости, мой стиль оставь»

Fix spelling, grammar, punctuation, and obvious awkwardness. Keep the author's structure and voice unless the user asks for more.

If the user says only «проверь текст» and there is no surrounding context, ask whether they want comments only, proofreading, or a full stylistic edit.

## 3. Audit only (do not rewrite)

These clearly ask for a diagnosis:

- «Найди места, которые звучат искусственно, но не переписывай»
- «Что здесь выдаёт нейросеть?»
- «Проверь, не пахнет ли этот текст ChatGPT. Только отметь проблемные места»
- «Покажи штампы и объясни, почему они режут слух»
- «Оцени текст, сам текст не меняй»
- «Где здесь вода / пафос / шаблонные обороты?»

Quote the exact passages and briefly state the issue. Do not provide a silently edited version. If the user asks for both audit and rewrite, do both as separate sections.

## 4. Targeted edit (change only the named issue)

These name one problem and should not trigger a complete rewrite:

- «Сократи вступление» / «убери воду»
- «Убери повторы»
- «Смягчи пафос»
- «Поправь только тире»
- «Упрости тяжёлые официальные обороты»
- «Убери канцелярские формулировки, но оставь деловой тон»
- «Замени кальки с английского»
- «Проверь только ритм и повторы»

The phrase «убери канцелярит» is understandable as a specific editing request, but it is editor jargon and should not be the primary user-facing example or a synonym for all Russian cleanup. Prefer familiar formulations such as «упрости тяжёлые официальные обороты» or «сделай понятнее, сохранив деловой тон».

## 5. Register-constrained edit

Phrases like these ask for readability without switching to casual speech:

- «Сделай текст живее, но официальный тон оставь»
- «Перепиши попроще, но сохрани деловой стиль»
- «Сделай понятнее для клиента, без панибратства»
- «Упрости фразы, но термины и официальный стиль не трогай»
- «Текст сухой. Сделай легче для чтения, но не разговорным»
- «Сохрани формулировки, которые нужны для договора/отчёта»

Keep required terms, formal address, and necessary institutional wording. Simplify sentence structure and remove empty padding, but do not replace the register with slang or personal intimacy. “Keep the official tone” does not mean “preserve every awkward bureaucratic phrase”; preserve the register and necessary terminology, not avoidable verbal padding.

## 6. Explicit constraints override trigger wording

- «Только исправь орфографию» means do not perform stylistic cleanup.
- «Не переписывай» means audit or explain only.
- «Канцелярит и термины оставь, поправь только повторы» means preserve them.
- «Официальный тон сохрани» means do not make the text conversational.
- Preserve quoted material, legal clauses, technical terms, and facts unless the user explicitly asks to change them.
