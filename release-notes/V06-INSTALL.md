# v0.6 installation
Merge this overlay at the repository root over v0.5. No deletions required. Commit or back up first. Run `bundle exec jekyll clean` and `bundle exec jekyll serve`, then open `/network-portfolio/network-plus/practice/`.

- 750 questions, 30 per objective; previous 500 records and storage key retained.
- 25 new technical review sections, with hands-on tasks and reference names.
- Adaptive plan ranks objectives by twice the missed count plus unseen count, chooses up to two distinct domains when available, and serves up to ten missed/unseen questions per objective. It is a transparent heuristic, not a validated mastery predictor. Filters do not constrain adaptive sessions.
- Existing CSV and print-to-PDF reports retained; CSV adds tracked attempts and first result when available. Older first results cannot be reconstructed.
- No upload/import. Existing flashcards and guided exercises retained; exercise scores are not persisted.
- Check 750 load, filters, objective review links, adaptive session on fresh and existing progress, missed retest, CSV and PDF. Static syntax and schema checks only; Jekyll/browser testing and independent technical editorial review remain pending. New difficulty tags are provisional; many scenarios are straightforward application rather than advanced analysis. New explanations are objective-level, not individualized distractor rationales. References are reading pointers, not verified live links. No commercial training PDFs included.
