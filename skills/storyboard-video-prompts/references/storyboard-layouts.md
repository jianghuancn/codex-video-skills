# Storyboard Layouts

Use these rules when choosing a detailed storyboard prompt format for ChatGPT/GPT Image 2/OpenAI image2.

## Default Selection

| Use case | Duration | Recommended layout | Notes |
|---|---:|---|---|
| Short social clip | 8-15s | 3x3 detailed grid | Best default for one Seedance2 reference image |
| Product/ad sequence | 12-18s | 4x2 detailed grid | Good for 8 clear product beats |
| Character intro | 6-10s | 3x2 detailed grid | Prioritize identity, pose, and costume continuity |
| Fast-cut montage | 15-30s | 3x4 or 4x3 detailed grid | Keep annotations short to avoid crowding |
| Performance/action routine | 10-20s | 4x4 rough previs grid | Good for 16 readable beats, FACS/performance grids, sports, combat, or music-synced motion |
| Assembly/sabotage/UI animatic | 10-20s | 4x6 track board | Good for 24 micro-shots with prop-state or UI-state continuity |
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
- 角度 and 运镜/camera angle and movement
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
- camera intent: low-angle rise, rear follow, eye-level follow, push-in, pan, tracking, fixed, rack focus, orbit, tilt, Dutch tilt, ground-level follow
- depth: foreground/midground/background separation, shallow depth of field, background blur, focus target
- lighting/color: morning light, neon, soft studio, golden hour, moonlight, rim light
- continuity anchor: same character/product/location/prop/color palette

Avoid:

- overcrowded labels that cover the keyframe
- too many subjects changing at once
- unreadably tiny action details
- large jumps in costume, location, or object shape
- chaotic camera movement unless explicitly requested

## Camera Movement Requirements

Every production storyboard should describe camera language with enough specificity for video generation:

- **Entrance power**: extreme low angle, slow rise from feet/clothing to face, normal proportions, no distortion.
- **Mystery**: rear follow, slow vertical rise, lateral scan, environment first, side-face reveal second.
- **Character plus environment**: eye-level follow while slowly orbiting around the subject.
- **Dialogue**: medium two-shot for basic exchange; over-the-shoulder reverse shots for deeper emotion or conflict.
- **Dialogue continuity**: keep A/B left-right placement fixed and stay on one side of the 180-degree axis.
- **Oppression**: first-person high-angle POV from the dominant side looking down.
- **Loneliness**: pure rear view, stillness or slow walk, large negative space.
- **Suspense**: Dutch tilt 15-20 degrees with slight handheld movement, held briefly.
- **Action/chase**: ground-level tracking close to footsteps, fast follow movement, strong speed and impact.
- **Cut continuity**: when cutting on the same subject, change angle by at least 30 degrees and preferably change shot size.

## Rough Previs Rules

Use rough previs when motion needs to be readable to Seedance2:

- Prefer graphite, pencil, manga thumbnail, wireframe mannequin, or semi-mannequin planning sketches.
- Keep one action beat per panel.
- Use strong silhouettes, clear screen direction, and simple body momentum.
- Add only the annotations that help staging: camera frame, motion direction, force arrow, timing accent, impact point, or environment interaction.
- Separate storyboard style from final-video style. The board can be monochrome while the final video style is described in a style packet or tiny swatches.
- Avoid finished illustration, dense shadows, repeated ghost bodies, and tiny unreadable details.

## Track Board Rows

For animatics with many shots, add a compact track board outside the keyframes:

- `BEAT`: short panel label, such as `reflect`, `reveal`, `insert`, `impact`, `payoff`.
- `CAMERA`: shot and move, such as `ECU`, `wide`, `insert`, `macro`, `overhead`, `OTS`, `push-in`, `whip pan`, `orbit`, `pullback`.
- `ACTION`: the visible action in verb form.
- `RHYTHM`: `hold`, `burst`, `fast`, `snap`, `rise`, `impact`, `peak`, `drop`, `final spike`.
- `STATE`: the continuity state after that panel, especially for products, devices, UI, props, costumes, or transformations.
- `STYLE`: rough sketch note or final-video style cue.

Use track boards for fast cause-effect sequences. A state change must be visibly caused by the preceding action.

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
