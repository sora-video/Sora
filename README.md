# Sora

Sora is OpenAI's text-to-video model; Sora 2 generates short clips with synchronized dialogue, sound effects and realistic physics.

> **Try Sora online →** [https://kyncept.com/video/pro](https://kyncept.com/video/pro?utm_source=github&utm_medium=ugc&utm_campaign=sora-video&utm_content=readme-top&utm_term=tier-b)

Sora is OpenAI's video generation model. It was first shown in February 2024 as a research preview with demo clips of up to a minute, went public in December 2024 at sora.com for ChatGPT Plus and Pro subscribers, and was replaced by Sora 2 at the end of September 2025. Sora 2 was a step change: the model generates synchronized audio, including dialogue and sound effects, alongside the picture, follows the laws of motion far more convincingly than the first version, and launched together with a standalone social app built around sharing and remixing generated clips.

The model is a diffusion transformer that treats video as sequences of spacetime patches, an approach OpenAI described in its original technical report and which most later video models adopted. Sora 2 added the audio track, better object permanence and a set of product features unique to OpenAI: Cameos, which let a person record a short verification clip and then appear in generated scenes with control over who may use their likeness, and Remix, which lets any clip be altered by a new prompt.

Sora 2 sits in the same top tier as Google Veo 3, Kuaishou Kling and MiniMax Hailuo. Its strengths are audio-visual coherence, dialogue that matches lip movement, and how much narrative a single prompt can carry; its weaknesses are clip length, limited resolution options through the API, tight content restrictions around real people and copyrighted characters, and availability that has varied by region and tier since launch.

## Contents

- [What Sora can do](#what-sora-can-do)
- [Versions](#versions)
- [How to access Sora](#how-to-access-sora)
- [Prompt examples](#prompt-examples)
- [Sora vs alternatives](#sora-vs-alternatives)
- [Pricing](#pricing)
- [FAQ](#faq)
- [Links](#links)

## What Sora can do

- Text-to-video and image-to-video with synchronized audio: dialogue, ambient sound and effects are generated together with the picture in Sora 2.
- Clip lengths of 4, 8 or 12 seconds through the API, and longer clips in the app depending on plan; the original Sora web version reached 20 seconds.
- Resolutions of 1280x720 and 720x1280 with sora-2, and higher-resolution portrait and landscape output with sora-2-pro.
- Cameos: record a short video and audio clip of yourself, then place your likeness in generated scenes, with settings that control who else may use it.
- Remix: take any clip, including other users' public clips in the app, and change the scene, style or action with a new prompt.
- Storyboard, Re-cut, Blend and Loop tools on sora.com for planning multi-shot sequences, trimming, merging two clips and making seamless loops.
- Reference image input to fix the first frame or the look of a scene, and a remix endpoint in the API for iterating on a previous generation.
- Noticeably improved physics: object permanence, buoyancy, rigid-body collisions and plausible failure when an action cannot succeed.

Known limitations: single generations are short, with a hard 12 second cap in the API; there is no 4K output; text inside the frame rarely renders correctly; real people can only appear through consented Cameos and many copyrighted characters are blocked; every output carries a visible watermark in the app and C2PA metadata everywhere; generation queues lengthen during peak hours; and the standalone app and its free tier have been limited to specific countries, with availability and limits changed several times since launch.

## Versions

| Version | Released | Notes |
|---|---|---|
| Sora (research preview) | 2024-02 | Announced with demo clips of up to 60 seconds and a technical report on spacetime patches; not publicly available |
| Sora (sora.com) | 2024-12 | Public launch for ChatGPT Plus and Pro: up to 1080p and 20 seconds, Storyboard, Remix, Re-cut, Blend and Loop |
| Sora 2 | 2025-09 | New model with synchronized audio, much better physics and Cameos; launched with the invite-only Sora iOS app in the US and Canada |
| Sora 2 API (sora-2, sora-2-pro) | 2025-10 | Video endpoints in the OpenAI API: 4, 8 or 12 second clips, 720p and higher-resolution Pro tier, reference images and remix |
| Sora Android app | 2025-11 | App expanded to Android in the same launch regions, with the invite requirement dropped in most of them |

## How to access Sora

Sora is a closed, hosted model. The official ways to use it are:

- sora.com in the browser, signed in with a ChatGPT account. Free accounts get a limited number of generations; ChatGPT Plus and Pro raise the limits, resolution and clip length.
- The Sora app for iOS and Android, which combines generation with a feed, Remix and Cameos. It launched in the United States and Canada and later expanded to other countries including Japan, South Korea, Taiwan, Thailand and Vietnam.
- The OpenAI API, where the sora-2 and sora-2-pro models are exposed through the video endpoints for generation, remix and download, billed per second of output.
- Microsoft Azure AI Foundry, which hosts the same models under Microsoft's terms.

Availability of the app, the free tier and the per-plan limits has changed several times since launch, and the app is not offered in every country where ChatGPT is; the official Sora page is the only authoritative source for the current state. If Sora is not available in your region, or you want to generate a clip without a ChatGPT subscription or API setup, [Sora](https://kyncept.com/video/pro) offers pay-per-generation access in the browser with no waitlist.

**Fastest way to try it:** [Try Sora online](https://kyncept.com/video/pro?utm_source=github&utm_medium=ugc&utm_campaign=sora-video&utm_content=readme-access&utm_term=tier-b) — no waitlist, runs in the browser.

## Prompt examples

**Dialogue scene**

```text
Two friends sit at a diner counter at night, one says 'You actually did it?' and the other laughs and replies 'I told you I would.' Warm tungsten light, rain on the window behind them, slow push-in on a 50mm lens, natural room tone and the clink of a coffee cup
```

**Physics showcase**

```text
A skateboarder attempts a kickflip down a five-stair set, the board flips twice, he lands slightly off balance and stumbles forward before recovering, late afternoon sun, handheld camera following from the side, sound of wheels on concrete
```

**Nature with ambient audio**

```text
A humpback whale surfaces beside a small research boat in a fjord, water pouring off its back, gulls overhead, the crew gasps, wide shot from the boat's bow, overcast light, realistic ocean sound and wind
```

**Stylised animation**

```text
A hand-painted 2D animated short: a fox in a raincoat waits at a bus stop in a rainy village, the bus arrives and splashes a puddle, the fox sighs; soft watercolour textures, gentle piano and rain sounds, static shot
```

**Image-to-video with reference**

```text
Starting from the uploaded photo of the lighthouse, the camera slowly pulls back and rises to reveal the rocky coastline at dusk while the lamp begins to rotate, waves break against the rocks with matching sound, no people, no text
```

## Sora vs alternatives

| Model | Max resolution / duration | Native audio | Editing and reference support | Access | Price tier |
|---|---|---|---|---|---|
| Sora 2 (OpenAI) | Up to 1080p-class, 4 to 12 s via API, longer in app | Yes, including dialogue | Image input, Remix, Cameos, Storyboard on sora.com | sora.com, Sora app, OpenAI API, Azure | Mid to high |
| Google Veo 3 / 3.1 | 1080p (4K in some tiers), 8 s | Yes, including dialogue | Reference images, first/last frame, extend, ingredients | Gemini app, Flow, Vertex AI API | Mid to high |
| Kling 2.6 / 3.0 (Kuaishou) | 1080p, 10 s, extendable to about 3 min | Yes (2.6 onward) | Start/end frame, Elements references, Motion Brush, lip sync, multi-shot | Kling web app, API, fal.ai | Low to mid |
| MiniMax Hailuo 2.3 | 1080p, 6 or 10 s | No | Subject reference, first/last frame, camera tags | Hailuo web app, API, fal.ai | Low |
| Runway Gen-4 | 1080p, 5 or 10 s | Separate audio tools | Reference images, Aleph video editing, camera control | Runway web app, API | Mid |

Sora 2 and Veo 3 are the two models where audio and video are generated as one thing, and they trade the lead on public arenas depending on the test. Sora 2 is usually preferred for dialogue-driven scenes and for its Cameo and Remix workflow; Veo 3 tends to win on visual polish and offers a longer route to 4K. Kling and Hailuo are cheaper per second and give more direct control over motion and framing, which makes them the usual choice for image-to-video production work, while Runway remains popular for its editing tools rather than raw generation quality.

## Pricing

As of the last public information, Sora is included in ChatGPT plans rather than sold separately: free accounts get a small daily or monthly generation allowance, ChatGPT Plus adds more generations at higher resolution and length, and ChatGPT Pro provides the largest allowance, the longest clips and access to the Pro model quality without a watermark. Extra generations beyond the plan allowance have at times been sold as add-on packs in the app.

The API is billed per second of generated video. sora-2 was launched at roughly $0.10 per second, and sora-2-pro at several times that rate depending on resolution; the OpenAI pricing page is the only authoritative source and rates may have changed. Because a single 12 second Pro clip can therefore cost a few dollars, subscriptions make sense for daily use, and for occasional clips pay-per-generation access such as the [Sora](https://kyncept.com/video/pro) link on this page avoids a monthly commitment.

## FAQ

**What is Sora?**

Sora is OpenAI's video generation model. Sora 2, the current version, turns text prompts or images into short clips with synchronized dialogue, sound effects and realistic motion, and it powers sora.com, the Sora app and the sora-2 API models.

**Is Sora free?**

Partly. Free ChatGPT accounts and the Sora app include a limited number of generations with a watermark, while ChatGPT Plus and Pro subscriptions raise the limits, resolution and clip length. The API is pay-per-use with no free tier.

**Is there a Sora API?**

Yes. Since October 2025 the OpenAI API exposes sora-2 and sora-2-pro through video generation, remix and download endpoints, billed per second of output. Microsoft also hosts the same models on Azure AI Foundry.

**Does Sora have an official GitHub repository?**

No. Sora is a closed model; OpenAI has published a technical report, a system card and API documentation but not weights or code. This page is an independent collection of publicly available information about it.

**How do I try Sora online?**

Sign in at sora.com with a ChatGPT account or install the Sora app in a supported country. If Sora is not available in your region or you do not want a subscription, https://kyncept.com/video/pro offers pay-per-generation access in the browser.

**What are the limits?**

API clips are 4, 8 or 12 seconds at 720p with sora-2 or higher resolution with sora-2-pro; the app allows somewhat longer clips on paid plans. There is no 4K, text inside the frame rarely renders correctly, real people appear only through consented Cameos, and many copyrighted characters are blocked.

**What are Sora Cameos?**

Cameos are Sora 2's way of putting a real person into generated video with consent. You record a short video and audio clip once to verify your identity and likeness, after which you, and anyone you allow, can prompt scenes that include you, and you can revoke that permission or delete clips at any time.

## Links

- [Sora official page (OpenAI)](https://openai.com/sora)
- [Sora 2 is here (OpenAI announcement)](https://openai.com/index/sora-2/)
- [OpenAI video generation guide](https://platform.openai.com/docs/guides/video-generation)
- [sora.com](https://sora.com)
- [Try Sora online](https://kyncept.com/video/pro)

---

*This is an independent, community-maintained information repository about Sora. It is not affiliated with, endorsed by, or sponsored by OpenAI. All trademarks belong to their respective owners. Corrections welcome via issues.*
