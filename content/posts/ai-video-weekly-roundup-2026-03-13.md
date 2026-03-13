---
title: "AI Video Weekly Roundup — March 13, 2026"
date: 2026-03-13T09:00:00-05:00
description: "Sora 1 retires as OpenAI eyes ChatGPT integration, Runway launches real-time avatar API, Luma Agents bring agentic creative workflows to ad agencies, and NVIDIA pushes local 4K video to RTX PCs at GDC."
tags:
  [
    "ai-video",
    "weekly-roundup",
    "sora",
    "openai",
    "runway",
    "luma",
    "nvidia",
    "comfyui",
    "ltx",
    "avatars",
    "agents",
  ]
categories:
  - "Weekly Roundup"
slug: "ai-video-weekly-roundup-2026-03-13"
image: "/img/roundup-2026-03-13.png"
draft: false
---

The standalone AI video app had a rough week. Sora 1 officially sunsets in the US today — and the numbers behind that decision tell a story the industry should take seriously. At the same time, Runway and Luma both shipped products that point toward what replaces the standalone generator: real-time avatars embedded in enterprise workflows, and agentic pipelines that handle creative production end to end. The theme this week isn't a new model. It's a new architecture for how AI video gets used.

---

## 📉 Sora 1 Is Gone — And Sora 2 Is Headed Into ChatGPT

Sora 1 officially retired for US users today, March 13. Sora 2 is now the only experience available, and any content created in Sora 1 that wasn't manually exported before this date is gone. OpenAI's recommendation was to pull data from Settings > Data Controls before the deadline — no automatic migration, no grace period.

The retirement is relatively clean technically. But the business context behind it is messier. A report from The Information this week revealed that OpenAI is planning to fold Sora's video generation directly into ChatGPT, mirroring how image generation via DALL-E was absorbed into the chatbot interface. The rationale isn't hard to find: Sora app installs dropped 45% month-on-month in January 2026, and the app fell out of Apple's US top 100. As a standalone destination, Sora hasn't held.

The strategic logic for moving Sora into ChatGPT is obvious. OpenAI's 900 million weekly ChatGPT users represent distribution that no standalone AI video app — from any company — can match. The tradeoff is moderation: deepfake risk at Sora's current scale is manageable; at ChatGPT scale, it becomes a structurally different problem. OpenAI hasn't confirmed a launch date.

For users, the practical near-term impact is positive. Sora 2 has meaningfully improved narrative coherence and reduced visual flickering compared to Sora 1, and the ability to extend clips from the final frame now makes short-form sequencing viable. Image-to-video with people, added under strict consent guardrails, rounds out the feature set.

The Disney deal signed in December — 200+ characters from Disney, Marvel, Pixar, and Star Wars, plus a $1 billion equity stake from Disney — gives Sora a legitimate licensed IP library that no other video model has. That's a differentiation play that makes more sense inside ChatGPT's reach than it does inside a niche standalone app.

**Why it matters:** OpenAI is effectively admitting that AI video doesn't work as a standalone product category at this stage. The winner will be whoever controls the interface users are already in — not whoever builds the best generator. This is a distribution bet, not a quality bet.

---

## 🎭 Runway Characters: Video Generation Becomes a Conversation

Runway shipped something qualitatively different this week. Runway Characters, launched March 9, is a real-time video agent API built on GWM-1 that lets developers generate fully conversational digital avatars from a single image — no fine-tuning required. The avatars render with realistic lip-sync, facial expressions, eye contact, and gesture, sustained over extended multi-minute conversations.

The use cases Runway is targeting — customer support, training simulations, branded marketing — are a clear pivot away from cinematic video generation. Early partners include BBC and Silverside, both deploying Characters for interactive content experiences. Enterprise teams can start building immediately via dev.runwayml.com; preset consumer avatars are also available in the Runway web app.

What makes this notable isn't just the product — it's the signal. Runway, after raising $315 million at a $5.3 billion valuation in February, is explicitly positioning its general world model as infrastructure for persistent interactive characters, not just video clips. GWM-1 generates frame-by-frame in real time, runs at 24fps at 720p, and can take live input from camera pose or audio to guide the simulation. That's a foundation for real-time interactive experiences, not batch generation.

The 720p ceiling and the constraint that characters are pre-defined from a single image (rather than fully generative) are current limitations. But the architecture underneath — a real-time physics-aware world simulator — is new ground.

**Why it matters:** Runway is making a direct play for the enterprise avatar market currently dominated by HeyGen and Synthesia. The difference is that Characters is built on a world model rather than a video diffusion pipeline, which means it can sustain interactive, responsive behavior rather than just rendering pre-scripted outputs. If the GWM-1 foundation proves robust, the competitive gap will be difficult to close.

---

## 🤖 Luma Agents: The First Agentic Creative Pipeline Hits Production

Luma launched Luma Agents on March 5, and by March 10, deployments were live at Publicis Groupe and Serviceplan Group. Adidas, Mazda, and Saudi AI company Humain are listed as early brand clients.

The underlying technology is Luma's Uni-1 model — the first in its "Unified Intelligence" family — which reasons and plans across text, image, video, and audio in a single architecture. Luma Agents can orchestrate other models mid-task: the system coordinates with Luma's own Ray 3.14 for video, Google's Veo 3 and Nano Banana Pro for photorealistic rendering, ByteDance's Seedream for specific generation tasks, and ElevenLabs for voice. An agent receives a creative brief, plans the asset suite, generates each element, evaluates and refines through iterative self-critique, and delivers a finished campaign package.

The pitch to ad agencies is that a campaign brief — copy, visuals, video, audio — can be executed without a human handing off between specialist tools or vendors. Persistent context across assets and creative iterations is a key technical feature: Luma Agents remember what was generated in earlier steps and can revise upstream elements when downstream evaluation surfaces a problem.

Luma is being careful about what it's claiming. The early deployments are for specific production types — social content, brand video, product demos — not open-ended creative development. The self-critique loop improves consistency, but the outputs are only as good as the models underneath, and quality control at scale is still a human task.

**Why it matters:** Luma Agents is the first credible production deployment of a multimodal creative agent pipeline. The fact that Publicis — one of the world's largest ad holding companies — went live at launch, not in beta, suggests real confidence in the output quality. If this holds up at scale, it compresses timelines and headcounts in lower-stakes video production in ways that will be felt across the industry within the year.

---

## 🖥️ NVIDIA and ComfyUI Bring Local AI Video to GDC — and the Masses

At the Game Developers Conference this week in San Francisco, NVIDIA announced a set of updates to its AI video pipeline for GeForce RTX users that add up to a meaningfully lower barrier for local generation.

The headline numbers: NVFP4 and FP8 model variants deliver up to 2.5x performance gains on RTX 50 Series GPUs, with 60% lower VRAM usage for video generation. The RTX Video Super Resolution node for ComfyUI delivers 4K upscaling 30x faster than competing local upscalers. These improvements apply to LTX-2.3 — Lightricks' open-source 22B-parameter model released this week — which now ships with a desktop video editor that lets the full pipeline run locally, including native audio, up to 20 seconds at 4K, on consumer hardware.

The other significant change is ergonomic: ComfyUI's new App View strips away the node-graph interface that intimidates newcomers, presenting a simplified prompt-in/video-out UI while keeping the full node graph available for power users underneath. For game developers using AI video for concept art, animatics, and storyboarding — the GDC audience — this removes a real adoption barrier.

NVIDIA also released a free Python package via PyPI and accompanying GitHub samples for developers who want to integrate RTX-accelerated video generation into their own pipelines. Looking ahead, NVIDIA GTC 2026 starts Monday, March 16 in San Jose. Jensen Huang's keynote is expected to address physical AI, a new unannounced chip, and enterprise-scale inference infrastructure — any of which could meaningfully affect local AI video capabilities further.

**Why it matters:** Local 4K AI video with native audio, running on consumer RTX hardware, now requires neither a cloud dependency nor a computer science degree to operate. The combination of the simplified ComfyUI App View, NVFP4 acceleration, and LTX-2.3's open-source desktop editor puts professional-quality local generation within reach of a much broader creator base — and removes cost and privacy concerns for studios that have hesitated to move AI video work to the cloud.

---

## 📈 By the Numbers

- **45%** — Month-on-month drop in Sora app installs in January 2026, prompting OpenAI's reported plan to fold the tool into ChatGPT
- **200+** — Licensed characters from Disney, Marvel, Pixar, and Star Wars now available for Sora generation under OpenAI's December deal with Disney
- **$1B** — Disney's equity investment in OpenAI as part of the Sora licensing agreement
- **2.5x** — Performance gain for AI video generation on RTX 50 Series GPUs via NVIDIA's NVFP4 acceleration in ComfyUI
- **30x** — Speed advantage of NVIDIA's RTX Video Super Resolution over competing local 4K upscalers
- **$5.3B** — Runway's valuation following its $315M Series C closed in February 2026

---

## 🔮 What to Watch Next Week

- **NVIDIA GTC 2026** runs March 16–19 in San Jose. Jensen Huang's keynote on Monday is the event of the quarter — watch for new silicon, physical AI infrastructure, and any video-specific announcements that follow the GDC previews
- **Sora in ChatGPT** — no official launch date, but the reporting from The Information suggests the decision has been made; any confirmation from OpenAI would accelerate the shift away from standalone AI video tools for casual users
- **Runway Characters early reviews** — BBC and Silverside are deploying in production; the first independent assessments of real-time avatar quality and session reliability will clarify how competitive the GWM-1 foundation actually is

---

_RCTV's AI Video Weekly Roundup is published every Friday. Subscribe to stay ahead of the curve._

{{< subscribe >}}
