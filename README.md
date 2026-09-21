# bus-4040-week-3-homework-quiz-sim

## What type of quiz did I create?
A single self-contained `index.html` quiz simulator, black-and-gold University of Idaho themed, built entirely from the weeks 1–3 course narratives in `class-material/`. It has 20 questions (13 multiple choice, 7 true/false) pulled directly from the material, presented one at a time in a shuffled order each run. Every answer shows immediate feedback, the correct answer, a short explanation, and which week/slide to review. At the end it shows a total score, a breakdown by week, and lets me retry just the questions I missed.

## What worked
Claude Code correctly scoped the quiz to only the material in the `class-material` folder and didn't invent facts outside of it. It also caught things worth skipping on its own — like a line in the Week 1 narrative that wasn't clear enough to turn into a fair question, and some model-naming details that weren't solid enough to quiz on. The retry-missed-questions feature and the week/slide references worked correctly on the first real test run, and the black-and-gold theme rendered cleanly with no external dependencies.

## What did not work
The file couldn't be opened directly from within the coding tool's preview — I had to locate it in Finder and double-click it to actually open it in a real browser to test it properly. Claude Code also initially left `class-material/` and a `.DS_Store` file untracked after the first commit, so they weren't included in the pull request; I had to catch that and add them separately.

## Did I have to make adjustments?
Yes — I had to specifically ask for the branch/PR workflow instead of committing straight to main, and I had to direct Claude Code to include the source material folder in the repo so the PR was self-contained. I also gave direction on the visual theme (University of Idaho black and gold) rather than accepting a generic default style.

## How could I apply this to other activities?
This same approach — feeding a defined set of source material to Claude Code with the instruction to build a self-contained, single-file tool — could work for building study tools for other classes, practice tools for interview prep, or even simple internal training checks. The key pattern is being precise about scope (use only these files, skip anything unclear) so the output stays accurate and doesn't hallucinate facts, plus verifying by actually clicking through it before trusting or submitting it.
