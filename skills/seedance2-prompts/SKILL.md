---
name: seedance2-prompts
description: Create, refine, rewrite, or diagnose prompts for Doubao Seedance 2.0 / Seedance2 video generation. Use when Codex needs to turn an idea, script, storyboard, image/video/audio references, video editing request, video extension request, text-in-video request, dialogue/audio requirement, or generation failure into a clear Seedance 2.0 prompt with subject binding, shot order, camera movement, style, quality, and constraints.
---

# Seedance2 Prompts

## Goal

Draft Seedance 2.0 prompts as engineering-style video direction: bind references precisely, describe what changes over time, and end with style, quality, audio, and constraint terms.

Use Chinese by default unless the user asks for another language. Return the usable prompt first. Keep explanations brief unless the user asks for rationale or variants.

## Workflow

1. Identify the task type:
   - **Multimodal reference**: create a new video from image/video/audio references.
   - **Video edit**: modify an existing video while unmentioned content stays unchanged.
   - **Video extension**: extend a video forward or backward, or bridge multiple video tracks.
   - **Combined task**: reference one asset while editing/extending another.
   - **Text/dialogue/audio task**: generate visible text, subtitles, speech bubbles, voice, sound effects, or music.

2. Inventory the assets:
   - Use `图片1`, `图片2`, `视频1`, `音频1` style labels exactly.
   - Assign each asset a role when useful: character anchor, scene/style reference, camera/action reference, effect reference, audio/timbre reference.
   - Prefer 4-5 total assets: 1-2 character images, 1 scene image, 1 camera/action video, 1 audio track. Too many assets can dilute priority.

3. Bind subjects before action:
   - For precise characters or objects, define labels with 2-3 stable static features.
   - Example: `将图片1中黑色短发、穿白色衬衫的女孩定义为女主。`
   - If a subject is not formally defined, mention it as `主体@图片N` every time.
   - If a subject is defined, use the same label consistently. Do not alternate with vague pronouns.
   - Never use an Asset ID alone as a reference; still write `图片N` or `视频N`.

4. Compose with the advanced formula:
   - `精准主体 + 动作细节 + 场景环境 + 光影色调 + 镜头运镜 + 视觉风格 + 画质 + 约束条件`
   - For complex videos, use `镜头1`, `镜头2`, `镜头3` in event order.
   - In each shot, include one camera move, subject action/expression, location or spatial change, and audio if relevant.

5. Add stability constraints:
   - Include quality: `高清，细节丰富，色彩自然，光影柔和，动作自然流畅`.
   - Include defect controls: `人物面部稳定不变形，无卡顿无闪烁，无穿模`.
   - Include text/logo controls unless text is requested: `保持无字幕，避免生成任何文字或字幕，不要生成Logo，不要生成水印`.

Read `references/seedance2-guide.md` when you need deeper templates, troubleshooting, or examples.

## Task Patterns

### Multimodal Reference

Use `参考...` only when an asset is a reference for a new video:

```text
参考图片1中的主体外观，参考视频1中的动作/运镜/特效，参考音频1中的音色/节奏，生成...
```

For audio timbre, describe both the reference and the timbre:

```text
参考音频1中低厚温润、带细碎颗粒感的中年男声音色说{...}
```

### Video Editing

For editing, directly name the edited video. Do not write `参考视频N`, because that can be misread as a reference task.

```text
严格编辑视频1，将其中的[原特征]修改为[新特征]，其余人物、动作、镜头和背景保持不变。
```

For adding elements, specify feature, timing, and position:

```text
在视频1的[位置]添加[元素特征]，[出现时机]自然出现，光影与原场景一致。
```

For deletion, name what to remove and what must remain:

```text
清除视频1中的[元素]，保留[主体/动作/背景/镜头]不变。
```

### Video Extension

For extension, directly name the video. Do not write `参考视频N`.

```text
向后延长视频1，生成视频1之后的内容：...
向前延长视频1，生成视频1之前的内容：...
```

For track bridging:

```text
视频1，[过渡画面描述]，接视频2，[过渡画面描述]，接视频3。
```

### Combined Tasks

When referencing one asset while editing another:

```text
参考图片1的[参考维度]，严格编辑视频2，将...，其余内容保持不变。
```

## Action And Shot Rules

- Prefer slow, continuous, small actions over extreme jumps, flips, frantic running, or very explosive motion.
- Describe body parts and intensity: `缓慢抬手`, `微微低头`, `用力蹬地`, `快速转头`.
- Add transitions between actions: `借着转身惯性顺势抬手`, `从停顿状态自然过渡到举手`.
- Externalize emotions through behavior, not only adjectives:
  - Sadness: `低头，肩膀微微颤抖，手指攥紧衣角`.
  - Joy: `嘴角上扬，眉眼舒展，脚步轻快`.
  - Tension: `频繁看手表，呼吸急促，眼神闪躲`.
  - Anger: `双拳紧握，下颌线紧绷，胸口起伏`.
- Use one camera movement per shot: `固定镜头`, `中景平稳跟拍`, `缓慢推近`, `平稳横移`, `特写`, `全景`.
- Avoid exact second-by-second timing unless required; Seedance responds more reliably to shot order than strict timestamps.

## Text And Audio Syntax

Use these symbols consistently:

| Information | Symbol | Example |
|---|---|---|
| Music | `（）` | `（背景中播放着轻柔钢琴）` |
| Sound effect | `<>` | `<门外传来轻微脚步声>` |
| Dialogue | `{}` | `女孩轻声说{我回来了}` |
| Subtitle/title text | `【】` | `画面中央出现【第一章：启程】` |

Keep dialogue language consistent. For small-language dialogue, name the language: `用日语说道{こんにちは}`.

If visible text is requested, define content, timing, position, appearance, and avoid rare characters or unusual symbols. If visible text is not requested, explicitly prohibit subtitles/text.

## Output Shape

For normal requests, output:

```text
【Seedance 2.0 提示词】
[final prompt]

【可选备注】
[only include if there are assumptions, asset-order warnings, or stability suggestions]
```

For prompt repair requests, output the improved prompt first, then 2-5 concise changes made.
