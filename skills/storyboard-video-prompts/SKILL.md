---
name: storyboard-video-prompts
description: Create detailed Seedance2-ready production storyboard prompts for ChatGPT/GPT Image 2/OpenAI image2. Use when Codex needs to turn an idea, script, product ad, music video, short drama, shot list, or visual concept into a multi-panel storyboard reference image that includes shot order, shot size, camera movement, character action, blocking/path, depth of field/lens, environment, lighting, transition, continuity anchors, and paired Seedance2 video-generation prompts.
---

# Storyboard Video Prompts

## Goal

Create a detailed production storyboard that can be used directly as a Seedance2 reference image, plus a paired Seedance2 prompt.

Default to Chinese unless the user asks for another language. Return usable prompts first. Keep explanations brief.

## Default Output

Default to a **detailed Seedance2-ready storyboard**, not a clean unlabeled board.

Each storyboard panel must contain:

- a video keyframe image area
- a compact production annotation strip outside the keyframe area
- shot number and time range
- shot size/framing: 全景, 中景, 近景, 特写, 低角度, 俯拍, 过肩, etc.
- camera movement: 固定镜头, 缓慢推近, 平稳跟拍, 横移, 上摇, 环绕, 拉焦, etc.
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

2. Choose a storyboard form:
   - For one Seedance2 reference image, prefer a single detailed grid image.
   - Use `3x3` for 8-15 second videos and compact action-readable sequences.
   - Use `4x2` for 8-shot ads or product demos.
   - Use `3x4` or `4x3` for 15-30 second montage or trailer beats.
   - Use multiple storyboard images only for 30s+ or scene-heavy stories.
   - Read `references/storyboard-layouts.md` when you need layout rules.

3. Write the ChatGPT/GPT Image storyboard prompt:
   - Ask for a single detailed production storyboard image.
   - Specify reading order: left-to-right, top-to-bottom.
   - Ask each panel to look like a real video still, with annotation strips outside the frame.
   - Preserve character/product consistency across panels.
   - Include all motion and blocking details in the panel description, not only in a separate table.
   - Keep annotation text short and structured so it fits: `镜头/时长/景别/运镜/动作/走位/景深/光影/转场`.

4. Write the Seedance2 prompt:
   - Bind the asset: `将图像1定义为详细制作故事板参考图。`
   - Tell Seedance2 to follow the storyboard as a timeline, not as a collage.
   - Tell it to read the annotations as production instructions.
   - Tell it not to render the storyboard text, borders, grids, or labels into the final video.
   - Add subject binding, shot order, camera motion, blocking, quality, and defect controls from the `seedance2-prompts` style.

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
