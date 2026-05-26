---
name: storyboard-video-prompts
description: Create detailed Seedance2-ready production storyboard prompts for ChatGPT/GPT Image 2/OpenAI image2. Use when Codex needs to turn an idea, script, product ad, music video, short drama, shot list, visual concept, action choreography, product demo, identity-board workflow, rough previs, animatic, Aimikoda-style storyboard grid, camera-movement plan, dialogue blocking, cinematic shot-language prompt, or storyboard-to-video reference into a multi-panel storyboard image that includes shot order, shot size, camera angle, camera movement, character action, blocking/path, depth of field/lens, environment, lighting, transition, continuity anchors, rhythm/action/state tracking, and paired Seedance2 video-generation prompts.
---

# Storyboard Video Prompts

## Goal

Create a detailed production storyboard that can be used directly as a Seedance2 reference image, plus a paired Seedance2 prompt.

Default to Chinese unless the user asks for another language. Return usable prompts first. Keep explanations brief.

## Default Output

Default to a **Seedance2-ready storyboard workflow**, not a generic pretty storyboard. Choose the board style that best fits the request:

- **Rough previs board** for action, choreography, timing, camera planning, and model-readable motion.
- **Detailed production board** for ads, products, short drama, cinematic continuity, or shots needing text guidance.
- **Identity/performance board** when character consistency, FACS expressions, valence-arousal, costume, prop, or emotional range is the main problem.
- **Animatic track board** when the video needs many fast cuts, beat-synced rhythm, product assembly, UI motion, sabotage, or exact prop state changes.

Read `references/aimikoda-methods.md` before complex action, choreography, rough sketch previs, identity-board-to-storyboard workflows, beat-synced videos, product assembly boards, or when the user mentions Aimikoda-style prompts.

Read `references/camera-language.md` before dialogue scenes, character entrances, emotional scenes, action/chase shots, multi-shot continuity, or when the user asks for stronger 运镜/镜头感/电影感.

Each storyboard panel must contain:

- a video keyframe image area
- a compact production annotation strip outside the keyframe area
- shot number and time range
- shot size/framing: 全景, 中景, 近景, 特写, 低角度, 俯拍, 过肩, etc.
- camera angle and movement: 低机位, 平视, 俯拍, 过肩, 荷兰倾斜, 固定, 缓慢推近, 平稳跟拍, 横移, 上摇, 环绕, 拉焦, etc.
- subject action and emotion
- blocking/path: where the subject starts, moves, stops, turns, looks, or interacts
- depth of field/lens language: 浅景深, 背景虚化, 广角空间感, 长焦压缩, 拉焦
- environment and lighting: scene detail, weather, time of day, color palette, key light
- transition or continuity note to the next shot

The annotation text is production metadata for Seedance2 and must not be treated as visible video content. In the paired Seedance2 prompt, explicitly instruct the model to use the annotations as shot guidance and not render text, captions, panel borders, or grids into the final video.

## Core Workflow

1. Extract the video brief:
   - purpose: ad, short drama, MV, game concept, product demo, tutorial, trailer, character intro
   - aspect ratio: default to `9:16` for shorts/social, `16:9` for cinematic/YouTube, or match the user's request
   - duration: default to 8-15 seconds if missing
   - style: cinematic realism, anime, product commercial, documentary, fashion editorial, etc.
   - continuity anchors: character, product, location, prop, color palette, lighting, costume

2. Build the reference stack:
   - Identify each uploaded asset role: character sheet, identity board, product reference, environment reference, logo/reference shape, style reference, storyboard/previs, audio/music, or UI source.
   - If identity matters, define the fixed identity source before the storyboard: `图像1是角色身份参考，图像2是分镜参考。`
   - If the storyboard should use rough sketches but the final video should look polished, separate the two: storyboard panels stay simple; final-video style appears in a style packet or tiny swatches.
   - Preserve exact source roles. Do not call a storyboard image a style image, and do not call a character sheet a storyboard.

3. Design the camera language:
   - Assign each shot a purpose: entrance, reveal, dialogue, emotional pressure, isolation, action speed, environmental exposition, or transition.
   - Use the camera formula: `视觉风格 + 主体动作 + 镜头角度 + AI运镜指令 + 环境光影 + 输出参数`.
   - For the same subject across cuts, change camera angle by at least 30 degrees and usually change shot size too.
   - For two-person dialogue, keep a stable 180-degree axis and fixed left/right positions.
   - Use camera movement to reveal background or emotion instead of only describing emotions directly.

4. Choose a storyboard form:
   - For one Seedance2 reference image, prefer a single detailed grid image.
   - Use `3x3` for 8-15 second videos and compact action-readable sequences.
   - Use `4x2` for 8-shot ads or product demos.
   - Use `3x4` or `4x3` for 15-30 second montage or trailer beats.
   - Use `4x4` or 16 panels for performance grids, FACS/valence-arousal grids, or hyper-dynamic action routines.
   - Use `4x6` or 24 panels for fast assembly, sabotage, UI motion, or many extractable micro-shots.
   - Use multiple storyboard images only for 30s+ or scene-heavy stories.
   - Read `references/storyboard-layouts.md` when you need layout rules.

5. Write the ChatGPT/GPT Image storyboard prompt:
   - Ask for a single detailed production storyboard image.
   - Specify reading order: left-to-right, top-to-bottom.
   - Ask each panel to be one extractable shot or keyframe. For rough previs, prefer low-detail graphite sketch, strong silhouettes, and readable motion over finished illustration.
   - Keep labels, director strips, panel numbers, timing, shot notes, arrows, or track boards outside the final keyframe area unless the user explicitly wants visible annotations inside the board.
   - Preserve character/product consistency across panels.
   - Include all motion, blocking, screen direction, prop state, camera angle, camera movement, rhythm, and end-state details in the panel description, director strip, or track board.
   - Keep annotation text short and structured so it fits: `镜头/时长/景别/运镜/动作/走位/景深/光影/转场`, or for animatics: `BEAT / CAMERA / ACTION / RHYTHM / STATE / STYLE`.

6. Write the Seedance2 prompt:
   - Bind the asset: `将图像1定义为详细制作故事板参考图。`
   - Tell Seedance2 to follow the storyboard as a timeline, not as a collage.
   - Tell it to read the annotations as production instructions.
   - Tell it not to render the storyboard text, panel borders, headers, notes, arrows, color marks, grids, track boards, style swatches, or labels into the final video.
   - Add subject binding, shot order, camera motion, blocking, quality, and defect controls from the `seedance2-prompts` style.
   - Do not repeat every storyboard detail unless the video model needs reinforcement. Prefer describing how to interpret the board, what to preserve, what to interpolate, and what not to invent.

## Output Shape

For normal requests, output:

```text
【ChatGPT 详细故事板图片提示词】
[prompt to paste into ChatGPT/GPT Image 2]

【Seedance2 视频提示词】
[prompt to paste into Seedance2 after uploading the detailed storyboard as 图像1]

【制作备注】
[only include assumptions, layout choice, or one practical warning]
```

If the user asks only for a storyboard, still make it detailed and Seedance2-ready by default. If the user explicitly asks for a clean no-text board, remove the annotation strips and represent motion with arrows, motion trails, poses, depth cues, and clear composition.

## Aimikoda-Derived Rules

- Prefer planning readability over illustration quality for action: rough sketches, strong silhouettes, one clear beat per panel, and minimal shading often work better than polished concept art.
- Use a clear cause-effect chain for action and product work: tool engages, body shifts, object changes state, consequence happens. Avoid disconnected cool shots.
- For action, dance, sports, and combat, require escalation: calm hook, first burst, mid-sequence complexity, impact or reversal, final held payoff.
- For beat-synced work, make each beat a separate shot or panel and label rhythm explicitly: `hold`, `burst`, `snap`, `impact`, `rise`, `peak`, `drop`, `final spike`.
- For identity-heavy work, generate or reference an identity board before the storyboard. Preserve face, silhouette, outfit, proportions, color identity, signature prop, and pose language.
- Use FACS, valence-arousal, Laban movement, IPA/phonetics, and SFX only when they directly improve controllability. Keep them as concise production metadata.
- For Seedance2, always instruct that storyboard artifacts are reference-only and must not appear in the final video.

## Camera-Language Rules

- Do not write vague camera notes like `多运镜` alone. Name the angle, movement, speed/energy, subject relation, and emotional purpose.
- Use low-angle rising shots for important entrances; rear follow plus scan for mystery; eye-level follow plus orbit for character/environment exposition.
- Use over-the-shoulder reverse shots and a fixed 180-degree axis for dialogue. Avoid crossing from one side of the axis to the other unless a deliberate disorientation is requested.
- Use POV high-angle shots for oppression, rear-only views for loneliness, Dutch tilt for tension, and ground-level tracking for chase/action.
- Keep Dutch tilt below 25 degrees and short. Add `人物比例正常无畸变` when using very low angles.
- For consecutive shots of the same subject, require at least a 30-degree camera-angle change and preferably a shot-size change.

## Seedance2 Reference Rules

- Always refer to the storyboard image as `图像1` unless the user gives a different asset order.
- Use precise wording: `严格参考图像1中的分镜顺序，按照从左到右、从上到下的阅读顺序生成连续视频。`
- Add this anti-collage instruction when using grid storyboards: `不要生成九宫格拼贴画面，不要把所有分镜同时显示在画面中；请把每个分镜格视为时间线上的连续镜头参考。`
- Add this annotation instruction for detailed boards: `图像1中的文字标注仅作为制作说明，请理解其中的景别、运镜、人物动作、走位、景深、光影和转场信息，但不要在最终视频中生成任何文字、字幕、编号、网格线或标注栏。`
- For recurring subjects, define labels with stable features before action: `将图像1中反复出现的[subject]定义为[label]，保持其外观、服装、比例和颜色一致。`
- Prefer one primary camera move per shot. If a shot needs multiple moves, describe the dominant move first and keep the secondary move subtle.
- Prefer stable blocking: walk, stop, turn, look, raise hand, pick up object, interact, reveal. Avoid extreme jumps unless requested.

## References

- Read `references/storyboard-layouts.md` for panel count, annotation strip design, and Seedance2-ready layout choices.
- Read `references/prompt-templates.md` for copyable detailed storyboard and Seedance2 templates.
- Read `references/aimikoda-methods.md` for Aimikoda-derived method patterns from the 59 provided prompts: rough previs, identity boards, motion-readable grids, track boards, performance grids, and authoritative storyboard-to-video prompts.
- Read `references/camera-language.md` for camera-movement requirements, dialogue continuity, 180-degree axis, 30-degree cut rules, entrance shots, emotional shots, and action tracking.
