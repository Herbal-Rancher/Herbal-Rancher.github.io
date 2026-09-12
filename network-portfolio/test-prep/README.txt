TEST PREP SITE — STRUCTURE

Root landing page:
- index.markdown
  Permalink: /test-prep/

Current exam track:
- 01-sf-1041-network-exam-prep.md
  Permalink: /sf-1041-network-exam-prep/

- 02-sf-1041-targeted-review.md
  Permalink: /sf-1041-network-exam-prep/review/

- 03-sf-1041-test-engine.md
  Permalink: /sf-1041-network-exam-prep/test-engine/

Recommended study flow:
1. Open /test-prep/
2. Choose an exam track.
3. Open that exam's Prep Home.
4. Use Targeted Review.
5. Use Test Engine.
6. Retest missed questions and repeat.

FUTURE EXPANSION

When adding Network+ or Security+, keep the same pattern:

Network+:
- network-plus-exam-prep.md
- network-plus-targeted-review.md
- network-plus-test-engine.md

Security+:
- security-plus-exam-prep.md
- security-plus-targeted-review.md
- security-plus-test-engine.md

Then add one new card to index.markdown that links to the new exam-prep home.

BASE PATH NOTE

The navigation currently includes /network-portfolio/ because the production GitHub Pages site uses that project base path.

If Jekyll is already prepending baseurl automatically, convert these hard-coded links to Liquid relative_url filters instead.

ENGINE NOTE

The SF 1041 test engine still contains:
- 150 original questions
- Quick Drill
- 25-question City Simulation
- Focused Review
- Retest Missed
- Local progress tracking
- Domain scoring
