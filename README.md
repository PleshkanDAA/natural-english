# Natural English

A skill for AI agents that write English. It makes the text read like a careful person wrote it: no bold on every other line, no em dashes, no heading over every two sentences, no filler and no details the agent made up.

## When it helps

We gave three Claude models 19 tasks without the skill, most of them writing: setup docs, a README, a changelog entry, a blog post, a landing page, a support report, a customer email and rewrites of AI-written text. Each model wrote about 15,000 words. Here is what came back:

- Bold type in almost every text, 14 to 19 times per 1,000 words, on list lead-ins, labels, dates and prices.
- A heading every 40 words or so, and one sentence in five was a list item.
- Sentences averaging 11 to 12 words, with little variation, which reads as a machine rhythm.
- Haiku 4.5 wrote about 12 em dashes per 1,000 words. Sonnet 5.5 and Opus 5.5 rarely did, but all three put one before the name under a quote. Opus also filled empty table cells with them, and Sonnet put an en dash between words in an email subject line.
- Small invented facts from all three models: a customs inspection that was "now complete", a free delivery the email promised to "apply to your account automatically", research from "several business schools".
- Blog posts that ended with an advice section or a moral nobody asked for.

With the skill, on the same tasks:

- Bold type, semicolons and em dashes outside quotes were gone, and list items fell from one sentence in five to about one in nine.
- In articles and reports, sentences grew from 13 or 14 words on average to about 16 to 18, with more variety in length.
- On Sonnet 5.5 the average score of the 11 writing tasks rose from 0.85 to 0.96, three runs per task. Across all 19 tasks with one run per model, Haiku 4.5 went from 0.76 to 0.89, Sonnet 5.5 from 0.88 to 0.96 and Opus 5.5 from 0.84 to 0.97.
- Three AI reviewers (Claude Opus 5.5 and Sonnet 5.5) compared the texts in pairs without knowing which one used the skill. They preferred the skill's version in 8 of 11 pairs and marked none as overdone.

The skill works best with Sonnet and Opus. Haiku 4.5 follows it only in part: with the skill it still scored below 0.8 on five tasks, mostly articles written without source material and rewrites of AI text.

The skill loads when the agent writes or rewrites English prose for people: docs, README files, changelogs and release notes, pull request descriptions, articles, web pages, reports, emails and posts. It covers formatting by genre, a rewrite for each job a dash usually does, sentence rhythm, filler, and the moves that give machine text away, such as a flag of importance where the reason should be. It changes the form of the text, not the task: content, facts and length stay as the user asked. If the material runs short, the agent writes less and says so. A project's own format wins over the skill's layout rules, so a Keep a Changelog heading or a PR template stays as it is. Em dashes and bold still stay out.

It does not touch code, commit messages, data files, quotes or text in other languages.

## Install

In Claude Code:

```
/plugin marketplace add PleshkanDAA/natural-english
/plugin install natural-english@pleshkan-natural-english
```

Background auto-update is off for third-party marketplaces. To get new versions automatically, open `/plugin`, go to Marketplaces, select pleshkan-natural-english and choose Enable auto-update.

In other agents that support the open [Agent Skills](https://agentskills.io) format:

```
npx skills add PleshkanDAA/natural-english
```

## If the skill does not load

An agent picks skills by their description, so now and then it may write English text without loading this one. If you see that, add a line to your global `CLAUDE.md` or `AGENTS.md`:

```
Before writing English text for people (docs, README files, changelogs, articles, web pages, reports, emails), load the natural-english skill.
```

## Features that work only in Claude Code

None.

## Scripts and network access

None.

## License

MIT
