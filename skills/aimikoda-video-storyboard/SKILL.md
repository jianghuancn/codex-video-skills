---
name: aimikoda-video-storyboard
description: Use when Codex needs an Aimikoda-style video storyboard prompt, rough previs board, animatic track board, reference-image workflow, product demo, action scene, transformation, performance board, cinematic shot-size or lighting plan, or Seedance2 storyboard-to-video prompt from a video idea, script, shot list, visual concept, or uploaded references.
---

# Aimikoda Video Storyboard

## Goal

Create Aimikoda-style video storyboard workflows: bind identity/reference assets, generate a motion-readable storyboard or animatic board, then produce a concise Seedance2 prompt that tells the model how to interpret the board as video.

Default to Chinese unless the user asks for another language. Return copyable prompts first and keep explanation brief.

## Output Shape

Return:

```text
【ChatGPT/GPT Image 故事板提示词】
[prompt to create the storyboard / previs / animatic reference image]

【Seedance2 视频提示词】
[prompt to generate the final video after uploading the storyboard as 图像1]

【制作备注】
[short assumptions, layout choice, or practical warning]
```

## Core Workflow

1. Extract the video brief:
   - content type: action, dance, product demo, short drama, UI motion, transformation, portrait performance, logo/environment sequence
   - duration and aspect ratio
   - final style and tone
   - continuity anchors: character, product, prop, location, color palette, lighting, costume
   - emotional target and visual emphasis: environment, action, emotion, detail, rhythm, or prop state

2. Bind references:
   - Define asset roles explicitly: `图像1=角色身份参考`, `图像2=产品/道具参考`, `图像3=场景/风格参考`.
   - If the storyboard is uploaded later, reserve `图像1` for the storyboard in the Seedance2 prompt unless the user gives a different order.
   - Preserve identity, silhouette, outfit, proportions, material, color identity, signature prop, and pose language.

3. Choose the board family:
   - **Rough previs board**: action, dance, sports, combat, chase, transformation, motion readability.
   - **Detailed production board**: ads, short drama, product demo, cinematic continuity.
   - **Identity/performance board**: FACS, valence-arousal, facial acting, costume or expression consistency.
   - **Animatic track board**: 12-24 fast cuts, product assembly, UI motion, sabotage, beat-synced montage.

4. Generate the storyboard prompt:
   - Prefer one single board image when possible.
   - Make each panel one extractable shot or key action beat.
   - Keep storyboard style separate from final-video style. Rough boards can be graphite or sketch; final style goes in a style packet or tiny swatches.
   - Include shot order, shot size, camera, action, blocking, lighting, rhythm, prop state, continuity, and final payoff.
   - Use shot size to split information: 远景/全景 establishes environment, 中景 shows action, 近景 carries facial emotion, 特写 isolates the decisive detail or prop state.
   - Use lighting to set mood: 冷色顶光 for pressure or danger, 逆光/轮廓光 for romance or hero reveal, 底光 for horror or unease, 丁达尔光 for sacred, solemn, or epic spaces.
   - Use track rows for fast work: `BEAT / CAMERA / ACTION / RHYTHM / STATE / STYLE`.

5. Generate the Seedance2 prompt:
   - Treat the storyboard as an authoritative shot blueprint, not a collage.
   - Tell Seedance2 to follow panel order, camera logic, action beats, motion direction, rhythm, prop state, and continuity.
   - Tell it not to render storyboard artifacts: borders, labels, text, arrows, notes, track board, style swatches, page layout, or panel numbers.
   - Explain what to preserve, what to interpolate, and what not to invent.

Read `references/aimikoda-methods.md` before complex storyboard work or when choosing between board families.
Read `references/output-templates.md` for copyable prompt skeletons.

## Aimikoda Rules

- Make the board useful for video generation, not just attractive as an image.
- Prefer planning readability over polish for action: strong silhouettes, clear body momentum, one beat per panel, minimal shading.
- For cinematic narrative boards, guide viewer attention by shot size: environment first, action second, emotion third, detail/payoff last. Avoid one overloaded wide shot containing all story information.
- Do not use generic `电影感光影` alone. Name the light direction/type and mood effect, and avoid `全亮平光` unless the video should feel like an interview, catalog, or neutral tutorial.
- Use explicit cause-effect chains: action happens, object state changes, consequence follows.
- Avoid disconnected cool shots. Every panel should advance action, emotion, reveal, transformation, rhythm, or state.
- For fast sequences, label rhythm: `hold`, `burst`, `fast`, `snap`, `impact`, `rise`, `peak`, `drop`, `final spike`.
- For products, devices, UI, sabotage, or assembly, track exact state after every panel.
- For performance, use FACS, valence-arousal, Laban, IPA/phonetics, or SFX only when they make the prompt more controllable.
- Keep the Seedance2 prompt shorter than the storyboard prompt when the board already contains detailed shot logic.

## Defaults

- Duration: 8-15 seconds if missing.
- Aspect ratio: `9:16` for social shorts, `16:9` for cinematic/YouTube, or match the user's request.
- Layout: `3x3` for simple 8-15s sequences, `4x4` for 16-beat performance/action, `4x6` for 24-shot animatics.
- Language: Chinese output by default.
