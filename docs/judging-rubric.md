# Self-assessment against a generic AI hackathon rubric

We don't yet have the official UCWS Singapore Hackathon 2026 rubric, so this is a self-grade against a common 6-dimension AI hackathon rubric. Each dimension is one short paragraph of self-assessment plus evidence pointers.

## 1. Problem fit

SMB commerce sellers in Singapore and SEA spend more per launch on photography (shoots, retouching, iterations) than on the product itself. The pain is highest in fashion and beauty where SKU count is high and trend cycles are short (48-hour launches are now common). Current alternatives are either expensive studios or generic AI tools that don't speak commerce. Evidence: chat examples and the request lifecycle in [`../ARCHITECTURE.md`](../ARCHITECTURE.md); deeper implementation detail available to evaluators under NDA.

## 2. Technical depth

5 deep engineering defenses + 9 supporting one-liners. The headline isn't the model choice — it's the commerce-vertical prompt and tool design (each tool wraps a domain-specific prompt pipeline with role-aware image handling). Supporting layers: prompt-injection / IP protection (system rules + tool-result sanitization), anti-evasion content filter (Unicode-aware, homoglyph-normalized, with space-insertion defeated), atomic billing with auto-refund, hallucinated tool-call recovery. Full detail: README section **"Why it's harder than it looks"** in [`../README.md`](../README.md). Source-level evidence available under NDA.

## 3. Demo quality

Live demo runs at popwiz.ai (production traffic). 90-second walkthrough video covers three flows: text-to-hero-shot, real-face-to-AI-model, product-to-ad-video. Full screenplay: [`demo-script.md`](demo-script.md). No mocked data in the video.

## 4. Business potential

Per-credit billing aligned with provider cost — economics work from one user upward without a "convert-to-paid" forcing function. Two complementary revenue paths: subscriptions (predictable creators) and credit packs (project-based brands). Atomic billing + auto-refund preserves trust at scale. Concrete signal: PopWiz is in production with paying users (numbers available to judges on request).

## 5. Team

<!-- Add additional teammates as `- Name — role · prior work · link` rows. -->
- **Zhiyu Zhang** — Founder & Engineer · building PopWiz end-to-end (commerce-vertical agent architecture, prompt and tool design, production infrastructure) · [GitHub @kizzhang](https://github.com/kizzhang)

## 6. Originality

Not just an LLM wrapper. The differentiator is the commerce-vertical tool decomposition (5 specialized tools instead of one freeform image-gen call) plus the engineering ring around it (defense-in-depth on prompt injection, content filter on both directions, atomic billing). Each layer is something a generic agent-builder kit doesn't give you, and that we built specifically because we hit the gap.
