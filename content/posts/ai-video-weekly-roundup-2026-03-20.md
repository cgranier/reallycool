---
title: "AI Video Weekly Roundup — March 20, 2026"
date: 2026-03-20T09:00:00-05:00
description: "Runway demos sub-100ms video on Vera Rubin at GTC, NVIDIA resets the AI infrastructure ceiling, DLSS 5 sets sights on Hollywood, and a Senate bill declares AI training not fair use."
tags:
  [
    "ai-video",
    "weekly-roundup",
    "nvidia",
    "gtc",
    "runway",
    "vera-rubin",
    "dlss",
    "regulation",
    "copyright",
    "inference",
  ]
categories:
  - "Weekly Roundup"
slug: "ai-video-weekly-roundup-2026-03-20"
image: "/img/roundup-2026-03-20.png"
draft: false
---

No new consumer models dropped this week. That's not because the industry was quiet — it's because the entire AI video world was watching San Jose. NVIDIA GTC 2026 ran March 16–19, and the announcements there didn't change what you can generate today. They changed what will be possible, at what cost, and at what speed, by the end of this year. Runway brought the most video-specific proof: a real-time generation demo with time-to-first-frame under 100 milliseconds. And in Washington, a Senate bill proposed declaring AI training on copyrighted works categorically not fair use.

---

## 🎬 Runway Demos Sub-100ms Video Generation on Vera Rubin

The clearest signal of what GTC 2026 means for AI video came from Runway. In a research preview developed in collaboration with NVIDIA and shared at the conference, Runway demoed a new real-time video generation model running on Vera Rubin hardware — generating HD video with time-to-first-frame under 100 milliseconds.

To calibrate that number: the human eye blinks in 100–400ms. Runway's demo sits at the floor of human perception. CEO Cristóbal Valenzuela framed the company's direction: "Video generation is rapidly advancing toward longer context and more flexible, agent-driven creative workflows. We see Rubin CPX as a major leap in performance, supporting these demanding workloads to build more general, intelligent creative tools."

The preview also surfaced a previously unannounced detail: Runway is running Gen-4.5 on Vera Rubin ahead of its public release. No launch timeline was given, but the implication is that Runway's next commercial model will be architected around Vera Rubin's performance profile from the start — not ported to it retroactively.

This is a research preview, not a product. Vera Rubin hardware won't be in the hands of cloud providers until the second half of 2026. But the demonstration establishes a new benchmark for what "real-time" means in video generation — one that enables entirely new use cases in interactive content, game cinematics, live streaming, and persistent AI characters that would be impossible at current 10–30 second generation times.

**Why it matters:** AI video has been a batch-generation medium since its inception. Sub-100ms generation doesn't just speed up existing workflows — it creates a different category of product entirely. Runway is explicitly building toward that category, and it now has the hardware partner to do it.

---

## 🖥️ NVIDIA GTC 2026: The Infrastructure Ceiling Moves Up

Jensen Huang's keynote on Monday set the context for everything else this week. NVIDIA unveiled the Vera Rubin platform — seven new chips configured into five rack-scale systems operating as a unified supercomputer — and projected $1 trillion in combined orders for Blackwell and Vera Rubin through 2027, doubling the $500 billion projection from GTC 2025.

The headline Vera Rubin specs: each GPU carries 288GB of HBM4 memory at 22 TB/s bandwidth, 50 PFLOPS of NVFP4 compute, and 336 billion transistors built on TSMC 3nm. The flagship NVL72 configuration — 72 Rubin GPUs and 36 Vera CPUs in a single NVLink 6 fabric — delivers 3.6 exaFLOPS of NVFP4 inference. For context, that's the performance footprint of a large AI video training run available as an inference cluster.

The number most directly relevant to AI video economics: 10x reduction in inference token cost versus Blackwell. Video generation is compute-intensive even by LLM standards — long-context diffusion steps are expensive. A 10x cost reduction at the infrastructure layer, passed through to cloud provider pricing, would materially change the per-second economics of every commercial AI video model by late 2026.

Separate from Vera Rubin, NVIDIA unveiled the Groq 3 LPU — a dedicated inference chip from the startup NVIDIA acquired for $20 billion in December 2025, shipping Q3 2026. Rubin CPX, a purpose-built GPU for million-token and generative video workloads, was included in NVIDIA's pre-show materials but was absent from Jensen Huang's keynote slides, where Groq 3 took its place. Whether CPX was quietly shelved or simply subordinated to the LPU narrative remains unclear. AWS, Google Cloud, Microsoft Azure, and OCI are all confirmed to deploy Vera Rubin-based instances in the second half of 2026.

**Why it matters:** NVIDIA just published the roadmap for AI video's infrastructure layer through end of 2026. The cost curve, the latency ceiling, and the memory capacity constraints that limit current model architectures are all moving in the same direction at the same time. The commercial models that get to market on Vera Rubin first will have a significant window of competitive advantage.

---

## ✨ DLSS 5: Neural Rendering Eyes Hollywood

NVIDIA also announced DLSS 5 at GTC — describing it as the most significant breakthrough in computer graphics since real-time ray tracing debuted in 2018. The technology is distinct from DLSS 4's frame generation: rather than interpolating frames, DLSS 5 uses a generative AI model to infuse scenes with photoreal lighting and materials anchored to source 3D geometry, consistent frame to frame.

The input is a game or 3D application's color and motion vectors. The output is a scene where lighting, surface materials, and environmental detail are generated, not rasterized. Major game publishers — including Bethesda, Capcom, Tencent, and Warner Bros. Games — are already on board. Even some of them were surprised by the announcement: PCWorld reported that multiple game developers said the reveal "blindsided" them.

But the headline that matters for this audience came from TechCrunch: "Nvidia's DLSS 5 uses generative AI to boost photorealism in video games, with ambitions beyond gaming." NVIDIA has explicitly positioned DLSS 5 for filmmaking, architecture, and design — use cases where real-time photorealistic rendering reduces VFX production time in ways that matter. DLSS 5 launches Fall 2026.

The connection to AI video is structural: DLSS 5 is NVIDIA teaching a model to understand 3D scene geometry and generate coherent, physically grounded visuals from it in real time. That's a capability with obvious applications in AI-driven cinematography tools, virtual production, and any workflow that requires compositing AI-generated elements into geometrically consistent environments. The game industry gets DLSS 5 first. The VFX pipeline gets it eventually.

**Why it matters:** AI video today generates images from diffusion processes that don't have a persistent model of the 3D world. DLSS 5 is a step toward a different architecture — one where the rendering engine understands scene geometry and generates lighting accordingly. That has long-term implications for how AI video handles environments, lighting consistency, and integration with live-action footage.

---

## ⚖️ A Senate Bill Declares AI Training Not Fair Use

While GTC dominated the week's attention, a significant regulatory development arrived Thursday. Senator Marsha Blackburn (R-TN) unveiled a draft AI legislative framework that takes direct aim at the legal question that has underwritten most AI video model development: whether training on copyrighted works constitutes fair use.

The Blackburn bill's answer is no. The draft explicitly states that the unauthorized "reproduction, copying or computational processing of copyrighted works" for the purpose of training or fine-tuning AI models does not constitute fair use under the Copyright Act. If enacted, this would effectively require AI companies to license training data from copyright holders — or stop using it.

The bill's other provisions include: abolishing Section 230 protections for platforms that knowingly host AI-generated deepfakes of real people; mandating third-party audits of AI systems for discriminatory outputs; requiring federal agencies to report the employment effects of AI; and establishing a National AI Research Resource to make compute and datasets available to researchers and small businesses.

Blackburn's bill is a draft, not an introduced bill, and the path to passage through a divided Congress is uncertain. But its framing — from a Republican senator, in a pro-industry administration — signals that the copyright question around AI training is no longer a fringe position. It's now part of the mainstream GOP legislative agenda. For AI video companies whose models were trained on unlicensed film and television footage, this is the version of events worth preparing for.

**Why it matters:** Every major AI video model was trained on copyrighted material. A ruling or statute that strips fair use protection from that training data doesn't just affect future models — it creates retroactive liability exposure for existing ones. ByteDance's Seedance is already frozen by Hollywood pressure. The Blackburn bill, if it advances, would formalize that pressure into law.

---

## 📈 By the Numbers

- **<100ms** — Time-to-first-frame for Runway's real-time video model running on NVIDIA Vera Rubin hardware, demoed at GTC
- **$1T** — Projected combined orders for NVIDIA Blackwell and Vera Rubin platforms through 2027, up from $500B projected at GTC 2025
- **10x** — Reduction in inference token cost with Vera Rubin versus Blackwell — the number that will reshape AI video per-second pricing by late 2026
- **3.6 exaFLOPS** — NVFP4 inference performance of the NVL72, NVIDIA's flagship Vera Rubin rack configuration
- **7** — New chips in the Vera Rubin platform (GPU, CPU, LPU, CPX, and interconnect variants)
- **Fall 2026** — Target launch window for DLSS 5, NVIDIA's neural rendering technology with stated ambitions in filmmaking and VFX

---

## 🔮 What to Watch Next Week

- **Gen-4.5** — Runway signaled at GTC that its next commercial model is being developed on Vera Rubin hardware; watch for an announcement once the research preview moves toward release
- **Seedance API freeze** — ByteDance has given no revised timeline since the Hollywood copyright action in February; the Blackburn bill's copyright provisions may further delay any resolution
- **Sora in ChatGPT** — OpenAI's reported plan to fold Sora into ChatGPT remains unconfirmed; any movement here would accelerate the platform consolidation story from last week

---

_RCTV's AI Video Weekly Roundup is published every Friday. Subscribe to stay ahead of the curve._

{{< subscribe >}}
