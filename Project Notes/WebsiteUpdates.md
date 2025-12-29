You are Claude running in “code assistant” mode. Your job is to implement small, surgical UI/copy fixes on the Salesforce Rescue site based on the attached screenshots.

Context:
- This is a long-form emergency-response landing page (“Salesforce Rescue”) optimized for mobile.
- We are NOT redesigning the site. Only fix the specific issues below.
- Keep tone: calm, direct, professional. No profanity.

Inputs:
- Screenshots show:
  1) CTA button copy: “Take Free Emergency Assessment” — feedback suggests adding “A” or “The”.
  2) Free Assessment form: Q1 “What’s broken?” and Q3 appear better as multi-select (checkboxes) rather than single-select radios; concern about back-end scoring system.
  3) “Missing graphic” placeholder appears in the long-copy section (likely an icon/image failing to load).
  4) Copy line highlighted: “We fix problems in a fraction of the time of traditional Salesforce support or large consulting firms.” Feedback: it reads jumbled out loud; reword.

Task list (implement all):
A) CTA button microcopy
- Replace “Take Free Emergency Assessment” with a better version that includes an article.
- Provide 3 options and select 1 as default. Keep it short and action-oriented.
- Example direction: “Take a Free Emergency Assessment” or “Get a Free Emergency Assessment”.

B) Reword jumbled sentence
- Replace: “We fix problems in a fraction of the time of traditional Salesforce support or large consulting firms.”
- Write 3 alternatives; pick 1 and implement.
- Keep meaning but improve readability. Avoid hype; avoid unverifiable claims like “always”.

C) Multi-select on Assessment form (Q1 and Q3)
- Update Q1 (“What’s broken?”) and Q3 (wherever it appears) to allow multiple selections via checkboxes.
- Update the scoring algorithm accordingly:
  - New score = sum of selected option weights (cap at 100).
  - If no options selected, score contribution is 0.
  - Preserve existing weights for each option where possible.
- Ensure UI/UX is clear on mobile: checkboxes, spacing, and a short helper line like “Select all that apply.”
- Update any validation logic so the form can proceed with multiple selections.
- Add tests or a simple debug log if the project has no test harness.

D) Fix the missing graphic
- Identify what is rendering as “Missing graphic” (broken <img>, missing SVG, icon library, wrong path).
- Fix it properly:
  - Prefer replacing with an inline SVG or a local asset in the repo.
  - Avoid hotlinking external images unless already used elsewhere.
  - Ensure it loads in GitHub Pages / static hosting.
- Verify no console 404s for assets.

Deliverables:
1) Make the code changes in the repo (commit-ready).
2) In your response, include:
   - Files changed (paths)
   - Before/after copy for the two text items
   - A short explanation of the scoring change and how it caps at 100
   - How you verified the missing graphic fix (what you checked)

Constraints:
- Do NOT rewrite the entire page.
- Do NOT change branding/colors/layout beyond what’s required for the fixes.
- Keep changes minimal and focused on the issues above.