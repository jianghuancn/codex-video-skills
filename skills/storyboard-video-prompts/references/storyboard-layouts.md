# Storyboard Layouts

Use these rules when choosing a detailed storyboard prompt format for ChatGPT/GPT Image 2/OpenAI image2.

## Default Selection

| Use case | Duration | Recommended layout | Notes |
|---|---:|---|---|
| Short social clip | 8-15s | 3x3 detailed grid | Best default for one Seedance2 reference image |
| Product/ad sequence | 12-18s | 4x2 detailed grid | Good for 8 clear product beats |
| Character intro | 6-10s | 3x2 detailed grid | Prioritize identity, pose, and costume continuity |
| Fast-cut montage | 15-30s | 3x4 or 4x3 detailed grid | Keep annotations short to avoid crowding |
| Trailer beat sheet | 20-40s | multiple 3x3 boards | Split by scene or emotional phase |
| Long story | 30s+ | multiple storyboard images | Generate one Seedance clip per board/scene |

## Seedance2-Ready Detailed Board

Default to a detailed production board that can be uploaded directly as `图像1`.

Each panel should have two zones:

1. **Keyframe zone**: a clean video-still image representing the shot.
2. **Annotation strip**: compact production notes outside the keyframe, ideally below the frame or in a narrow side strip.

The annotation strip should include:

- 镜头编号 and time range
- 景别/framing
- 运镜/camera movement
- 人物动作/subject action
- 走位/blocking or path
- 景深/lens/depth cue
- 光影环境/lighting and scene
- 转场/continuity to next shot

Keep annotation text short. The image should still read visually even if the text is small.

## Visual Detail Rules

Each keyframe zone should visibly encode:

- shot type: wide shot, medium shot, close-up, over-the-shoulder, top-down, low-angle
- action: one clear subject action or visual change
- blocking: arrows, footprints, gaze direction, object interaction, start/end pose when useful
- camera intent: push-in, pan, tracking, fixed, rack focus, orbit, tilt
- depth: foreground/midground/background separation, shallow depth of field, background blur, focus target
- lighting/color: morning light, neon, soft studio, golden hour, moonlight, rim light
- continuity anchor: same character/product/location/prop/color palette

Avoid:

- overcrowded labels that cover the keyframe
- too many subjects changing at once
- unreadably tiny action details
- large jumps in costume, location, or object shape
- chaotic camera movement unless explicitly requested

## Clean Board Exception

Only make a no-text clean board when the user explicitly asks for it or the target workflow cannot tolerate text in reference images.

For a clean board, encode details visually instead:

- camera move arrows in the margins
- motion trails for subject movement
- start/end pose silhouettes
- focus plane or blur cues
- lighting arrows or glow direction
- consistent panel order and gutters

Then include the full shot details in the paired Seedance2 text prompt.

## Aspect Ratio

- `9:16`: short video, TikTok/Reels/Shorts, portrait ads.
- `16:9`: cinematic, YouTube, landscape product videos.
- `1:1`: square social posts or when the video platform is unknown.

For Seedance2, prefer a storyboard board whose keyframe zones match the final video aspect ratio. The full grid image can have extra space for annotation strips.
