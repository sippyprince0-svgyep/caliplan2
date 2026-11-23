CaliPlan Smart Coach v19 — Phase 5 Coaching Refinement
======================================================

PHASE 5: FINAL COACHING IMPROVEMENTS
------------------------------------
1. Fixed a premature skill-mastery issue: a single logged set at the target no longer marks a skill mastered. Mastery now follows the workout-level progression rules, requiring all prescribed sets to meet the target and repeated successful sessions before a progression step advances.
2. Added a Skill Progression Focus panel on Coach. It shows the selected goal, the current safe prerequisite movement, the track step, and a reminder not to jump to maximal attempts.
3. Added a 14-day Training Balance panel based on logged sets, categorized as push, pull, legs and core. It only flags a possible exposure imbalance when enough data exists and explicitly warns that set counts are not a measure of muscle stimulus or recovery.
4. Updated skill and auto-plan explanations to accurately describe repeated-session progression rather than implying that one target hit is sufficient.
5. Bumped the service-worker cache to caliplan-v19.

VALIDATION RUN
--------------
- Inline JavaScript syntax check passed.
- Service-worker JavaScript syntax check passed.
- Manifest JSON validation passed.
- ZIP integrity validation passed.
- Source-level checks confirm that single-set auto-mastery was removed from the set logger and the Coach screen includes both new panels.

LIMITATIONS
-----------
- An automated interactive browser run was attempted but this environment blocked Chromium navigation, so this build does not claim a fresh full browser-runtime pass.
- No Android-device test has been performed. Release testing remains a separate final step on the user's phone.
- Training balance is an estimate from logged set counts and simple exercise-name classification, not an assessment of actual muscle stimulus, technique, injury risk or recovery.
- CaliPlan remains an offline, rules-based coach, not an AI model or medical/sports-science diagnostic system.

INSTALLATION
------------
1. Before replacing files, use Progress → Copy backup and save the text somewhere safe.
2. Replace index.html, sw.js and manifest.json with this package.
3. Keep your existing icon-192.png and icon-512.png in the same folder.
4. Reload CaliPlan. The service-worker cache key is now v19.
5. Your saved data continues using the existing "caliplan2" key.
