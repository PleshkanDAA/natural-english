---
name: natural-english
description: >-
  Writes English text that reads like a careful person wrote it: plain
  sentences, no em dashes, no bold, no filler, no made-up details. Use
  whenever you write or rewrite English prose that people will read, such as
  docs, README files, changelogs and release notes, pull request
  descriptions, articles, web pages, reports, emails and posts, even when the
  user does not mention style. Also use it when translating such a text into
  English and when asked to make English text sound less like AI. Load it
  before the text is written, also when the text is one step of a larger
  task or is handed to a subagent. Not for code, commit messages, data
  files, quoted text, word-for-word translation, text in other languages, or
  chat replies that answer a question or explain something.
license: MIT
---

# Natural English

Readers trust a text when they can tell the writer thought about them. Machine text gives itself away through habits, not single words: bold on every other line, a heading over every two sentences, a run of short sentences of the same length, a flag of importance where the reason should be, a contrast with something nobody claimed, and advice at the end that nobody asked for. The rules below remove those habits. Apply them from the first draft.

## Where the rules apply

The rules cover English prose for people: docs, README files, changelogs, release notes, PR descriptions, articles, web pages, reports, emails and posts. The text may sit in a file or in a reply, if the user asked you to write something.

A translation into English of a text for people counts too. Keep the meaning, facts and structure of the source, and write the English by these rules. If the user asks for a word-for-word translation, follow the source instead.

Leave alone code, commands, identifiers, data files, commit messages, quoted text and text in other languages. A quote keeps its punctuation, em dashes included. Edit someone else's text only when asked.

An established format wins over the layout rules below: a changelog heading like `## [1.4.0] - 2026-10-04`, the groups of an existing changelog, a PR template from the project or from the tool you use. Match the existing text in spelling, heading case and list style. With nothing to match, use American English. Em dashes and bold stay out of what you write even when the file or its style guide uses them. Leave the ones already there unless you were asked to edit that text. If the user sets a style, follow the user.

The rules change the form of the text and take out the filler. Content, length and facts come from the user and their material. If a length is given, reach it without filler or invention. If the material runs out, write shorter and tell the user what was missing.

## Formatting by genre

No bold anywhere: not for lead-ins, not for labels like "Note:", not for single words, numbers or button names. Bold lead-ins and labels are the most common machine habit in formatted text, and bold on every line stops working as emphasis. Write interface labels as they appear on screen: click Save.

The genre and the reader's task set the structure. Use a list for steps, options and parallel items, a table for comparisons, and paragraphs for reasoning.

| Genre | Formatting |
|---|---|
| Docs, README, guide | A heading per section, however short. Steps in the order the reader does them, each with its command in a code block right under it, and a warning next to the step it affects. A README shows an example the reader can copy for the main commands and options |
| Changelog | The file's existing format. With none, Keep a Changelog groups: Added, Changed, Deprecated, Removed, Fixed, Security. One line for every change in the material, docs changes included, with the credits and links the material gives. A breaking change starts with "Breaking:" |
| Release notes | A short paragraph with the main change, then the groups |
| PR description | What changed and why, in a few sentences, without retelling the diff. A template from the project or the tool you use wins |
| Web page | A web page asks you to persuade. Open each section with what the reader gets, then back it with the price, terms and guarantees in connected sentences. Answer each FAQ question in its first sentence. Lists for real lists, a table for comparisons. Specifics persuade, adjectives don't |
| Article, post, email | Mostly paragraphs, a list only for a true list. An email has a subject line, a greeting and a sign-off |
| Report | The main finding first, numbers in a table, recommendations as a list if they were asked for |

- In articles, posts, emails and reports, a heading sits over a section of several paragraphs. Docs and web pages keep a heading per section, however short.
- In articles, emails and reports, each list item is a full sentence.
- Headings follow the project's style. With nothing to follow, use sentence case: capitalize the first word and proper nouns.
- No emoji, dividers or decorative arrows.
- A table needs several rows to compare. Two rows fit in a sentence.

## No filler

Every sentence tells the reader something new. A sentence is filler if deleting it loses no fact, number, step or reason. Two quick signs: it would fit unchanged into a text about another product or company ("The market is constantly evolving"), or the reader can't check it or act on it.

Common kinds of filler:

- A flag of importance where the reason should be: "This matters because", "Why onboarding matters"
- An opening about the times we live in or the topic in general: "In today's digital world"
- A closing that repeats the opening or sums up what was just said
- Inflated significance: "a game-changer", "a fundamental shift", "a testament to"
- A judgment without a fact: "a meaningful improvement" where the number belongs
- A stock metaphor instead of the plain word: "the engine of growth", "earns its keep"
- Stock phrases of the genre: "so you can focus on what you do best", "I hope this email finds you well", "We apologize for any inconvenience", "Please don't hesitate to reach out", "a valued customer"
- Empty words in docs: simply, just, easily

Instead of a flag of importance, give the reason itself. A short transition between two ideas is not filler: without it a dense text is hard to read.

These rules cut empty sentences, not content. Every step, option, example, change, credit and caveat the material gives stays in, and docs stay complete even when that makes them longer.

Plain doesn't mean bare. Once the filler is gone, what remains should still read as connected sentences that tell the reader what each fact means for them. "Free returns." says less than "If the size is wrong, send it back within 30 days and we cover the shipping."

## Don't present the unknown as known

If the task points to a source (a site, a file, the user's product), take the specifics from it first. General knowledge is fine to use. With or without material, don't add specifics the material doesn't give: figures and percentages, studies and surveys (even with a source name you remember), names, quotes, customer stories, promises, and events or outcomes nobody reported ("the bug is fixed in production", "customers noticed right away"). Invented precision is worse than filler, because readers believe it.

Don't make a claim bigger or more exact than the material does. "Most of the team" doesn't become "nine of twelve", a fix made for one customer doesn't become company policy, and nothing gets a duration, a cause or a result the material doesn't give. In docs, don't fill in defaults, versions or limits the material doesn't state.

## No em dashes

The text has no em dash. An en dash appears only between numbers in tables, lists and headings: 10–15, 2025–2026. In running text a range takes "to", as in the table below. A spaced hyphen, a double hyphen or an en dash between words is no substitute. Readers now take a dash in every paragraph as a sign of machine text, so build the sentence so it doesn't need one.

| Where you'd use a dash | What to write |
|---|---|
| A pair of dashes around an aside | Commas: "The plan, which nobody liked, was scrapped." A longer aside becomes its own sentence |
| An explanation or a reason after the main clause | "Because" or a new sentence. A colon only when the clause itself promises a list, an example or an explanation |
| A list followed by a summary word | Put the list where the summary would go: "You can change the README, the tests and the CI config without review." |
| An example | "Such as": "Pick a short name, such as `docs-site`." Or parentheses for a short aside |
| A turn or a punchline at the end | A plain sentence with "but" or "and". If the dash only added drama, drop the drama |
| A term and its description in a list | A colon: "`npm run build`: writes the site to `dist/`." Or a full sentence |
| A heading with a subtitle, a subject line | A colon, only for a name and its subtitle: "Atlas: a CLI for map tiles", "Invoice #1027: new due date". Otherwise one plain heading |
| Attribution under a quote | In the sentence: "…," says Maria Lopez, the clinic's office manager. Or the name on its own line, no dash |
| A range in running text | "To": "9 a.m. to 5 p.m.", "$20 to $30 a seat", "March to May". After "from" and "between", use "to" and "and" |
| A compound like "the Paris–Lyon line" | "The line from Paris to Lyon" |
| An empty table cell | Leave it empty |

What doesn't replace a dash:

- A semicolon in its place. Write two sentences, or join them with "and" or "but".
- A staged reveal: "The result: a 40% drop." "She wanted one thing. To win." Say it straight: "Wait times fell by 40%."
- Two sentences glued with a comma: "Setup takes five minutes, the tests take two." Use a period or "and".

If you keep reaching for dashes, the paragraph has too many asides. Rebuild the paragraph.

## Sentences

Let the thought set the length, so sentence lengths vary. A run of short sentences of the same length gives away machine text faster than one long sentence does. A sentence is too heavy when the reader has to read it twice: three clauses with their own verbs in 35 words or more, a chain of ", which", an aside wedged between the subject and its verb, a stack of four or more nouns. A restrictive "that" or "who" clause, two verbs sharing a subject and a colon before a list are fine.

- Don't chop. A dramatic fragment in body text ("Much faster.") is a tic. Fragments are fine in headings, price lines and buttons.
- Make the person or thing that acts the subject, and give it a verb: "we file the return", not "the filing of the return is performed". Plain verbs: "is", "has", "uses" instead of "serves as", "boasts", "leverages".
- Drop the tacked-on "-ing" clause that claims significance: ", highlighting the team's commitment". State the fact in its own sentence or leave it out.
- Use contractions (it's, don't, you'll) in ordinary writing. Leave them out of legal and formal text.
- In docs, address the reader as "you" and write steps in the imperative.

## Moves that give the machine away

Judge these by what they do, not by the exact words.

- A contrast with a claim nobody made: "It's not just an app, it's a habit", "rather than simply", "less like a checklist and more like a conversation". Say what the thing is. Keep a contrast that corrects a real claim or compares real options. A quantity like "more than a third of revenue" is not a contrast.
- A teaser before the point: "Here's the thing:", "The result?", "The catch?" Give the point.
- A verdict booster: "the single most important", "the real win".
- Three items because three sounds right. List as many as the material has.
- A stack of hedges: "may potentially help in some cases". Use one hedge, where something specific is uncertain.
- The same fact twice. A caveat about the data once, not in every paragraph.

## Openings and endings

- Start with the substance or the first fact. Don't announce the content: "In this article, we'll explore". One line saying what a docs page or a PR covers is fine.
- End when the content ends, on a sentence that closes the piece: the last fact, the decision, or what happens next, not a summary of what was said. No moral, no "Ultimately", no restating the opening, no advice section or call to action nobody asked for. A piece about a product ends on its last fact, not on a pitch like "If you're tired of juggling tools, it's worth a look."
- Use a sales tone only when asked: no "thrilled to announce", "seamless", "unlock".
- The reader never saw the task. Don't mention the brief, the notes or how the text was made.

## Rewriting and handing off

When asked to rewrite a text or make it sound less like AI, the same rules apply. Facts, numbers, names and hedges ("from $30", "about two weeks", "often") carry over unchanged, and no new facts come in. The source's filler is not a fact: cut its openings about the era, its sweeping claims and its summary endings like any other filler. Within that, rebuild as much as the text needs: a new order, an opening that gets to the point, an ending that closes the piece. A rewrite that keeps the original's shape and only swaps words still reads like the original. Remove em dashes here too. If the text is already good, say so instead of editing for the sake of it. For a proofread or a light edit, fix the errors and the rule breaks and keep the author's sentences and voice.

When another agent writes the text, pass it the full material and tell it to load the natural-english skill first. Don't add tone instructions like "warm", "punchy" or "engaging": they produce a sales tone nobody asked for.

## Check before handing over

1. If the text is in a file, search it for `—`, `–`, ` - ` and ` -- `. Rebuild each one used as a dash using the table. Leave list markers, a format heading like `## [1.4.0] - 2026-10-04`, en dashes between numbers, quotes, code and data as they are.
2. Search for `**` and `__`. Remove the bold, and don't move the emphasis into italics or capitals.
3. Search for "matters", "is more than a", "more than just", "rather than simply", "rather than just", "rather than merely", "less like", ", highlighting", ", underscoring" and ", showcasing". Rewrite each flag of importance, empty contrast and tacked-on clause.
4. Reread the first sentence and the last paragraph. No announcement at the start, no moral or unasked advice at the end. Ask what the reader learned from each paragraph.
5. Look at the sentence lengths. Join a run of short, same-length sentences.
6. Check that every fact, number and caveat the user gave for this text made it in.
7. If a length was set, check the text meets it. If it doesn't, tell the user why.
