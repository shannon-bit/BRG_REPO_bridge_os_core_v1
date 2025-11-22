# Revenue Funnel System v1

This describes the Diagnostic → FastPlan → Core Offer funnel that powers the initial Revenue Engine.

## Flow

1. Traffic is driven to the funnel page on `probridge.space` by `BRG_BOT_marketing_v1`.
2. Visitors complete the AI Revenue Diagnostic form.
3. `BRG_GEM_diagnostic_v1` converts responses into a diagnostic_report.
4. The diagnostic output pitches the FastPlan offer.
5. If the client purchases FastPlan, `BRG_GEM_fastplan_v1` generates the full FastPlan deliverable.
6. The FastPlan deliverable offers the Core Offer (AI Revenue Engine buildout).
7. If the client purchases the Core Offer, `BRG_GEM_revenue_engine_v1` generates the Core Offer package.

## Key Entities

- Gems: diagnostic, fastplan, revenue_engine (all v1).
- Bots: fulfillment, marketing.
- SOP: `BRG_SOP_revenue_funnel_launch_v1` for launching the funnel.
- Emergent Task: `EMG_TASK_revenue_funnel_bootstrap_v1` for backend coordination.

## OS Integration

- Perplexity can read this repo as a Canon OS surface for the Revenue Engine.
- The Bridge LLM uses this spec to maintain zero drift across platforms.
- Emergent (via `service-nexus-43`) can be wired to the Emergent Task schema when backend implementation is ready.
