# Alfiery Personality Test

**40 questions. Four letters. Find your type and compare with friends.**

👉 **Take the test:** https://alfierie.github.io/alfiery-personality-test/

A free personality type quiz in the style of the Myers-Briggs (MBTI) four-letter types. It runs entirely in the browser: no sign-up, no ads, no tracking, and your answers never leave your device.

## What you get

- **Your four-letter type**, like `INFJ` or `ESTP`, with a short description, strengths and things to watch out for.
- **A spectrum for each letter pair** showing how strongly you lean, from *Slight* to *Very clear*.
- **Close-call warnings.** If you land near 50/50 on a pair, the result says so and shows you the neighbouring type to compare.
- **A copy-and-paste result** to drop into the group chat.
- **Saved progress.** Close the tab halfway and pick up where you left off.
- Works on phones, supports light and dark mode, and can be answered with the keyboard (keys `1`–`7`, `←` to go back).

## The four pairs

| Pair | Measures | Example statement |
| --- | --- | --- |
| **E / I** · Extraversion or Introversion | Where you get your energy | "Even after a fun social event, I need time alone to recover." |
| **S / N** · Sensing or Intuition | What information you trust | "I'm more interested in what something could become than in what it is now." |
| **T / F** · Thinking or Feeling | How you make decisions | "Keeping the peace in a group matters more to me than proving I'm right." |
| **J / P** · Judging or Perceiving | How you handle plans | "I do my best work in a burst right before a deadline." |

## How the scoring works

- There are **10 statements per pair**, answered on a 7-point scale from *Strongly disagree* (−3) to *Strongly agree* (+3).
- **Half of each pair's statements point toward each letter.** This cancels out the habit of agreeing with everything, a common reason quick quizzes give wrong results.
- Statements from the four pairs are **interleaved**, so it's harder to guess what each question is measuring.
- Each pair's score is turned into a percentage between the two letters:

  ```
  percent toward first letter = 50 + (sum of answers ÷ highest possible sum) × 50
  ```

- Over 50% gives the first letter (E, S, T, J), under 50% the second (I, N, F, P). An exact 50% shows as `x`.

## Run it locally

It's a single static file with no build step.

```bash
git clone https://github.com/alfierie/alfiery-personality-test.git
cd alfiery-personality-test
open index.html
```

## Make it your own

Everything lives in [`index.html`](index.html):

- **Questions:** edit the `ITEMS` object. Keep 5 statements with `1` (agreeing points to the first letter) and 5 with `-1` (agreeing points to the second) in each pair.
- **Type descriptions:** edit the `TYPES` object.
- **Colors and fonts:** change the CSS variables at the top of the `<style>` block.

Push to `main` and GitHub Pages republishes the site within a minute or two.

## A note on accuracy

The four letters describe *preferences*, not abilities, and nobody is purely one side. Results are most trustworthy on pairs where you lean clearly; pairs near the middle can flip on a retake. This quiz is inspired by Jung's type theory and is not the official MBTI® assessment. MBTI and Myers-Briggs Type Indicator are trademarks of The Myers-Briggs Company.
