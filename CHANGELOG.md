# Changelog

## v5.1 — Learning and reasoning improvements
- Added an evidence-aware, capped learning ledger in existing IndexedDB metadata.
- Added explicit positive/negative feedback capture and relevance-based lesson retrieval.
- Updated system and team prompts to favour structured problem-solving, evidence checks and uncertainty over exposed `<think>` tags.
- Added a blank-generation fallback.
- Made Llama 3.2 1B the default model and the fallback for auto-restoring a previously selected 3B model.
- Kept existing UI, controls, search actions, document retrieval, memory, voice, goals, and agent team features.

## v5.2 — Training pipeline and portable learning ledger
- Full memory export/import now includes Bob's capped explicit-feedback learning ledger.
- Added separate TRAINING pipeline: dataset preparation, LoRA/QLoRA fine-tuning, baseline/candidate generation, side-by-side comparison, and adapter merge.
- Added held-out starter evaluation tasks and privacy/licensing/deployment guidance.
- Existing dashboard and browser model selection remain unchanged; tuned weights are not automatically deployed.

## v5.4 — Caring persona
- New default personality "Caring & supportive": acknowledges how the user feels first, patient and encouraging, uses their name, honest rather than flattering.
- A short care instruction is now part of the core system prompt for every personality; Classic is warmer too.
- Team agents (Planner/Reviewer) use a warm, caring tone.
- Token budget rebalanced (system core 700, profile/RAG 1100) so the longer prompt is not truncated.
- Users who already saved a personality keep it; pick "Caring & supportive" in Settings to switch.

## v5.5 — Reliable news and search
- Replaced the dead RSS gateways (feed2json.org, personal Vercel proxy) with a gateway chain (direct, allorigins, corsproxy, codetabs) raced in parallel, with in-browser RSS/Atom/RDF parsing.
- Six sources for top news (BBC, Guardian, Al Jazeera, NPR, DW, Google News); GDELT, Hacker News and Wikipedia as fallbacks.
- New news on a topic: chip plus plain chat ("news about Thailand", "what's happening in Ukraine").
- 10-minute cache and last-saved headlines when offline; clickable Sources list under each news answer.
- Article summaries now read the full text (reader service, then gateway extraction) instead of only metadata.
- Research adds Wikipedia full-text search and recent headlines.
- Settings: Test news sources shows which services work on this device.
