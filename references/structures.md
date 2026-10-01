# Structures to Avoid (Russian)

The categories below cover patterns typical of Russian AI-generated text.

## Канцелярит and Nominalization (номинализация)

Turning verbs into abstract nouns is the #1 Russian AI tell. The noun:verb ratio in LLM text is ~3:1, in human writing ~2:1.

| Pattern | Problem |
|---------|---------|
| «Осуществление проверки документов» | The verb «проверить» became a noun chain |
| «Принятие решения о запуске» | «решили запустить» says it in two words |
| «Реализация процесса оптимизации» | Two nominalizations stacked |
| «Обеспечение возможности доступа» | «позволяет получить доступ» |
| «Производит оценку ситуации» | «оценивает ситуацию» |

**Instead:** turn the noun back into a verb. «Команда проверила документы» beats «Было осуществлено проведение проверки документов».

## Genitive Chains (цепочки родительного падежа)

Three or more nouns in genitive in a row is a marker of both AI and канцелярит.

- «процесс оптимизации системы мониторинга производительности»
- «улучшение качества обслуживания клиентов компании»
- «анализ эффективности стратегии развития продукта»
- «процесс осуществления контроля качества данных»

Read it aloud — you lose the start by the end. Real writers structure differently.

**Instead:** two short sentences, or a verb. «Клиенты стали довольнее» / «Обслуживание в компании стало лучше» beat «улучшение качества обслуживания клиентов компании».

## «Является» (copula crutch)

The most irritating Russian word-parasite. In 9 of 10 cases it can be deleted or replaced with a dash or a real verb.

| Pattern | Fix |
|---------|-----|
| «Данный подход является эффективным» | «Подход эффективен» |
| «Это является важным фактором» | «Это важно» |
| «Продукт является решением проблемы» | «Продукт решает проблему» |
| «Данные являются ключевым фактором успеха» | «Без данных проект не взлетит» |
| «Скорость является определяющим фактором» | «Скорость определяет всё» / «Решает скорость» |

**Instead:** find the actual verb. If the sentence is a definition, the dash works where the register allows it («Антитела — это белки»), though a verb («называются», «служат», «относятся») reads more alive. If it is just padding, cut the «является» and the noun that follows it.

## Binary Contrasts (бинарные противопоставления)

The «not X, it's Y» family translated into Russian is the most viral AI construction of all:

| Pattern | Problem |
|---------|---------|
| «Не просто X, а Y» | Telegraphed reversal |
| «Не только X, но и Y» | Additive hedge (fine once, a tell repeated) |
| «Это не X — это Y» | Setup/reveal cliche |
| «Это не просто инструмент, это философия» | Marketing parody outside ads |
| «Не автокомплит, а раскрытие потенциала» | Mechanical contrast |

**Instead:** state Y directly. «Инструмент» or «философия» — say which one you mean and why. Drop the negation entirely.

## Negative Listing (перечисление через отрицание)

Listing what something is *not* before revealing what it *is*.

| Pattern | Problem |
|---------|---------|
| «Это не инструмент. Это не процесс. Это философия.» | Dramatic buildup through negation |
| «Речь идёт не о скорости. Не о качестве. О доверии.» | Same structure, different words |

**Instead:** state Z in the first sentence. The reader doesn't need the runway.

## Dramatic Fragmentation (рубленые фразы)

Sentence fragments for emphasis read as manufactured profundity.

| Pattern | Problem |
|---------|---------|
| «Скорость. Качество. Надёжность. Это всё.» | Staccato drama |
| «Быстро. Надёжно. Удобно.» | Empty abstract triad |
| «Вот и всё. Просто. Честно.» | Affected simplicity |

**Instead:** complete sentences stating the real point. Abstract triads («быстро, надёжно, удобно») are a rhythm crutch — test each item: can the reader say what it concretely means? If not, cut to two items or say one specific thing.

## Rule of Three (правило трёх)

AI loves triads because they sound rhythmic and complete. The tell is when all three elements are abstract.

- «Инновации, вдохновение и возможности»
- «Быстро, надёжно, удобно»
- «Вдохновляет, мотивирует и трансформирует»
- «Просто, понятно и эффективно»

**Test:** if the list has exactly three items and all are abstract — it's almost certainly AI. Humans write two items or five, with varied length. Three round abstractions in a row is a marker.

## Dash Overload (перегруз тире)

In Russian the em-dash is typographically legitimate — unlike English, the fix is not "zero dashes" but "no overload".

| Pattern | Problem |
|---------|---------|
| «Скорость — выше. Качество — стабильнее. Риски — ниже.» | Mirror sentences, one schema |
| «Код — чистый, тесты — зелёные, деплой — успешный» | Dash as comma substitute |
| Two or more dashes in one sentence | Dash overload |
| Long em-dash (—) in casual online text (Telegram, blog, email) | Formal typography in an informal venue |

**Instead:** replace with commas, periods, or restructure. In casual online writing, live authors mostly use the en-dash or a hyphen anyway; the long em-dash reads as textbook-generated.

## Passive Voice and Impersonal Constructions (страдательный залог)

Every sentence needs a subject doing something.

| Pattern | Fix |
|---------|-----|
| «Осуществляется контроль качества на всех этапах» | «Команда проверяет данные на каждом этапе» |
| «Было отмечено, что…» | «Мы заметили…» / name who noted |
| «Производится оценка ситуации» | «Оцениваем ситуацию» |
| «Проводится работа по…» | Name the work or cut |
| «Решение было принято» | «Мы решили» |

Reflexive verbs (на -ся) frequently hide the actor: «вопрос решается», «задача выполняется». Russian uses them naturally in many registers, but as a *nominalization-plus-refl* stack («осуществляется обеспечение…») it is pure канцелярит.

**Instead:** find the actor, put them at the front.

## False Agency (неодушевлённый субъект)

Giving inanimate things human verbs to avoid naming a person.

| Pattern | Problem |
|---------|---------|
| «Событие подчёркивает важность…» | The event did nothing. Someone drew a conclusion. |
| «Тренд отражает…» | Trends don't reflect. Someone read data. |
| «Данные говорят нам…» | Data sits there. Someone reads it. |
| «Опыт показывает, что…» | Experience is not a subject |
| «Технологии трансформируют подходы» | Technologies don't do this by themselves. People adopt them. |

**Instead:** name the human. «Команда увидела в данных…» beats «Данные показывают…». If no specific person fits, use «вы»/«ты».

## Narrator-from-a-Distance (рассказчик со стороны)

Floating above the scene instead of putting the reader in it.

| Pattern | Problem |
|---------|---------|
| «Многие сталкиваются с этой проблемой» | Armchair generalization |
| «Эксперты считают…» | Vague authority |
| «Исследования показывают…» | Without a citation, it's a crutch |
| «В последние годы наблюдается…» | Lecturer voice |
| «Никто не ожидал…» | Disembodied observation |

**Instead:** put the reader in the room. «Когда мы впервые запустили это в проде, никто не ожидал…» beats «В последние годы наблюдается рост интереса…».

## Rhetorical Setups (риторические подводки)

These announce insight rather than deliver it.

| Pattern | Problem |
|---------|---------|
| «А что, если…?» | Socratic posturing |
| «Представьте себе…» | Padded invite |
| «Подумайте об этом» | Condescending prompt |
| «Самое интересное впереди» | Redundant preview |
| «И вот здесь начинается самое интересное» | Clickbait transition |

**Instead:** make the point. Let readers draw conclusions.

## Template Structures (шаблонные структуры)

| Pattern | Problem |
|---------|---------|
| «Во-первых… Во-вторых… В-третьих…» | Mechanical numbering with same-shaped blocks |
| Every bullet starts the same way («Снижает… Повышает… Ускоряет…») | Listicle signature |
| «**Скорость:** … **Качество:** … **Внедрение:** …» | Chatbot listicle signature |
| All paragraphs 3–4 lines, one thought each, same rhythm | Equal paragraphs |
| Every paragraph ends punchily | Monotone emphasis |
| «Таким образом, …» / «Подводя итог…» / «В заключение…» at the end of every section | Formulaic conclusion |
| «Теперь перейдём к…» / «Следующий аспект…» | Smooth prefab transitions |
| A «Заключение» section that just re-states the text | Duplicate, no added value |

**Instead:** vary the grammar of list items; merge short paragraphs and split long ones; end a section with the actual conclusion or the next step without a formulaic bridge; let one paragraph be a single line for accent.

## Word Patterns (словесные паттерны)

| Pattern | Problem |
|---------|---------|
| Lazy absolutes (всегда, никогда, все, каждый, любой) | False authority |
| «от X до Y» for unrelated concepts | False range; enumerate or name one real range |
| «с одной стороны… с другой стороны…» | False balance; take a position |
| Synonym carousel («главный герой» → «ключевой игрок» → «ведущий персонаж») | AI avoiding repetition; repeat the name if clearer |
| «Существует мнение, что…» | Unattributed opinion |
| Comma-splice strings of participles: «решение, обеспечивающее повышение эффективности, реализующее контроль…» | Participle pile-up; use verbs |

**Instead:** use the specific word, repeat the name when repetition is clearer, give real ranges with units, and attribute opinions to actual people.

## Genre Exceptions (жанровые исключения)

Not everything on this list is wrong everywhere. Before cutting, check the register:

- **Academic/scientific**: «является», «данный», «таким образом», «в рамках» are normal. Clean only obvious канцелярит c chains and empty superlatives.
- **Legal**: keep «данный», «настоящий», «в соответствии с». Do not "humanize" contracts.
- **News**: strict factual style; dash may be normal in some outlets — calibrate.
- **Casual online (Telegram, blog, email)**: the most permissive; this is where long dashes and канцелярит read as the most foreign.

When in doubt, keep the author's voice. The goal is removing AI marks, not imposing one bland style.