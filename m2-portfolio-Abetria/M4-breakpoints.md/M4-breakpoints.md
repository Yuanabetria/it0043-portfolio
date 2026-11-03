# Milestone 4 - Breakpoint Choices & Testing Notes
Name: Yuan V. Abetria

## 1. Breakpoint Choices

- 480px (Mobile Nav): Below 480px, the 4 navigation links are stacked vertically so they are easy to tap on phones. Once the screen hits 480px, there is enough room to put them side-by-side in one row without crowding.
- 768px (Tablet Layout): At 768px, keeping the form in one single column looked too stretched out. I changed the form fields to a 2-column grid and added a bit more card padding so the space is used better.
- 1024px (Desktop Spacing): The cards already have a max-width of 650px to keep text easy to read. At 1024px and wider monitors, I just bumped up the body padding so the page doesn't look stuck to the top and side borders.

## 2. QA AI Challenge & Defense

Challenge 1: Why stack the nav links vertically on mobile if the buttons are small enough to fit?
Defense: When I checked on 320px screen width in DevTools, putting all links in one row made the buttons too close together, leading to misclicks. A vertical stack gives better tap space for mobile users.

Challenge 2: Why switch to a 2-column form on tablets if the cards are already centered?
Defense: On tablet screens, a 1-column input field stretches all the way across and looks awkward to fill out. The 2-column layout makes the inputs shorter and cleaner to look at.

Challenge 3: Why write a 1024px media query just to adjust padding?
Defense: Without the extra padding, wide desktop screens (like 1440px) leave too little margin around the centered content. Increasing padding at 1024px keeps the whitespace balanced.

## 3. AI Usage & Verification

### AI Disclosure
I used Google Gemini to act as a simulated QA tester for Step 2 (generating bug symptoms) and to ask challenge questions about my breakpoints in Step 4. All CSS edits, media queries, DevTools testing, and final fixes were done by me.

"I can explain every line of this submission without assistance."

Signed: Yuan V. Abetria

### Revision Table
| AI Suggestion / Bug Report | How I Checked It | Result | What I Did |
|---|---|---|---|
| Use flex-wrap on nav links at 320px | Tested mobile view in Chrome DevTools (320px) | Valid | Changed nav to flex-direction: column on mobile. |
| Form inputs broke into 2 columns at 320px | Inspected form on 320px mobile viewport | False alarm (AI hallucination) | **Rejected:** The form was already in 1 column on mobile, so no change was needed. |
| Desktop layout needs more outer margin at 1440px | Checked desktop view in DevTools (1440px) | Valid | Added extra body padding inside the 1024px media query. |