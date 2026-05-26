# Aimikoda Prompt Methods

Use these patterns when a storyboard needs to behave like a production blueprint for Seedance2 rather than a decorative storyboard. This reference is derived from the 59 prompt entries in `aimikoda_may_prompts_extracted.md`; do not copy the original prompts verbatim. Extract the method, then adapt it to the user's subject, assets, aspect ratio, duration, and style.

## Core Thesis

The recurring workflow is:

1. Create or bind identity references.
2. Create a motion-readable storyboard, previs sheet, performance grid, or animatic board.
3. Give Seedance2 a short authoritative interpretation prompt that says how to read the board and which artifacts to ignore.

The storyboard image should carry shot order, staging, motion, rhythm, prop states, and style intent. The Seedance2 prompt should mostly explain how to translate the board into continuous video.

## Coverage Map From The 59 Prompts

- 1-2: couple identity sheet plus gentle relationship video. Extract shared identity, emotional continuity, couple chemistry, and soft motion reveal.
- 3-5: simple sketch previs for a rescue chase. Extract rough board readability, arrows/boxes as planning marks, and Seedance interpreting panels as sequential keyframes.
- 6: horror previs to video. Extract mood, lighting, and motion-reference binding from a storyboard.
- 7: character reference plus music-video action. Extract fixed character identity plus rhythmic shot progression.
- 8: handheld social clip. Extract `FORMAT / SCENE / STYLE` blocks for fast engagement and physical camera feel.
- 9-11: reference-driven UI and sequential source images. Extract scene-by-scene source binding, UI preservation, and cursor/action timing.
- 12: storyboard as one continuous shot. Extract the special case where panels are key moments inside a continuous 15s take, not cuts.
- 13: beat-synced close-up performance. Extract short beat lists, gentle camera variation, and strict identity preservation.
- 14: storyboard plus character/logo references. Extract multi-reference hierarchy and final reveal logic.
- 15: FACS Action Unit grid. Extract expression-control grids and concise facial metadata.
- 16-18: latte, jump rope, and musical/performance boards. Extract simple concept-to-storyboard prompts, kinetic manga energy, music sync, and final reveal.
- 19-22: dance and sword-combat storyboards plus Seedance prompts. Extract 12-16 beat action escalation, monochrome rough sketches, color-coded annotations, and exact progression preservation.
- 23-24: valence-arousal and emotional grid. Extract emotion-coordinate metadata and smooth expression transitions across panels.
- 25-26: identity board plus expression-performance video. Extract identity-board-first workflow and soft controlled close-up acting.
- 27-30: forest dancer and kung fu performance. Extract professional previs layout, low-detail mannequin boards, motion arrows, FACS cues, Laban movement logic, and elemental escalation.
- 31: Midjourney character seed. Extract that external image generation can create a character source before GPT Image storyboard work.
- 32: cute-to-crazy expression scale. Extract controlled emotion spectrum boards.
- 33-34: two-character POV fight and pop-out frame-break storyboard. Extract strict multi-character identity, alternating POV order, and foreground intrusion.
- 35-36: reference-image cinematic grid and director-language workflow. Extract optional director-language as abstract style guidance, not imitation, before storyboard generation.
- 37-38: batting cage performance storyboard plus Seedance. Extract athletic prop readability, music-synced beats, and final slow-motion hero payoff.
- 39-40: copyright-safe identity board and multi-tool character workflow. Extract original identity creation before storyboard and Seedance.
- 41-42: product breakdown and product demo video. Extract premium product-board structure, feature/motion studies, and clean product demo sequencing.
- 43-44: student/master training storyboard. Extract two-character contrast, continuity, action timing sheets, and exact camera/action following.
- 45: beat-synced portrait video. Extract 16 hard-cut facial beats with FACS and minimal camera movement.
- 46-47: fan kata storyboard plus Seedance. Extract sakuga planning thumbnails, color-coded annotation keys, spatial continuity, and reference-only production marks.
- 48: hyper-lapse selfie travel. Extract location-beat lists and strict identity continuity across hard cuts.
- 49-52: metamorphosis and fantasy performance workflows. Extract transformation continuity, ribbon/shape evolution, action planning boards, and final active reveal.
- 53-54: anime style catalog. Extract style variation grids while preserving a recognizable subject core.
- 55: logo-as-environment sequence. Extract shape-reference continuity across multiple environments.
- 56: Midjourney plus storyboard plus Seedance workflow. Extract two-character identity inputs, rough-sketch storyboard, and video prompt that uses storyboard as shot blueprint.
- 57-58: 24-panel teleport-device animatic and authoritative Seedance prompt. Extract track boards for `BEAT / CAMERA / RHYTHM / ACTION / STATE / STYLE`, prop-state continuity, and explicit exclusion of board artifacts.
- 59: 12-shot sabotage action. Extract staccato insert triplets, causal mechanical detail, route readability, SFX metadata, and no impossible part failure.

## Board Families

### Rough Previs Board

Use for action, dance, sports, combat, chase, transformation, or anything where movement readability matters more than beautiful frames.

- Ask for rough sketch, graphite, manga thumbnail, wireframe mannequin, or low-detail storyboard style.
- Prioritize silhouettes, body momentum, camera arrows, motion paths, and one clear action beat per panel.
- Keep shading minimal. Avoid polished concept-art finish when the board is meant to guide motion.
- Use annotations as production marks: camera framing, force direction, impact timing, environment interaction, or rhythm.

### Detailed Production Board

Use for ads, short drama, cinematic stories, product demos, and scenes where Seedance benefits from reading compact shot metadata.

- Use keyframe area plus annotation strip or director strip.
- Keep text outside the video keyframe area when possible.
- Include shot number, framing, camera move, action, blocking, depth/lens, lighting, transition, and continuity.
- Make each panel an extractable shot or a fixed key moment in a continuous shot.

### Identity Or Performance Board

Use when consistency is the risk.

- Bind the identity source first: character sheet, identity board, product board, logo, prop design, or style source.
- Preserve face, silhouette, outfit, proportions, colors, signature prop, material, and personality.
- For faces, use FACS or valence-arousal only when the user needs precise expression control.
- For motion, use Laban-like descriptors only when they help: direct/indirect, sudden/sustained, strong/light, bound/free.

### Animatic Track Board

Use for 12-24 shots, hard cuts, product assembly, UI sequences, sabotage, fast demos, or beat-synced work.

- Add a compact track board with rows such as `BEAT`, `CAMERA`, `ACTION`, `RHYTHM`, `ESCALATION`, `STATE`, and `STYLE`.
- Use prop-state language: broken, scattered, core set, bolt locked, assembled, portal forming.
- Use rhythm words: hold, burst, fast, snap, impact, rise, peak, drop, final spike, unresolved.
- For causal actions, require the visible cause before the effect.

## Seedance2 Interpretation Prompt Pattern

When the storyboard image is final, write a Seedance2 prompt that says:

```text
将图像1定义为权威分镜/预演/动画蓝图。严格按照从左到右、从上到下的顺序，把每个分镜格作为时间线上的连续镜头或关键动作点来生成视频。不要把整张故事板当作拼贴画、分屏、海报或静态页面。

图像1里的面板边框、编号、标题、文字标注、箭头、颜色标记、导演条、风格色块、轨道表、页面排版和制作备注都只是给模型理解镜头、动作、节奏和连续性的参考，最终视频中不要生成这些元素。

保留分镜中的镜头顺序、构图、主体位置、运动方向、动作节拍、道具状态、空间关系、情绪递进和最终姿态。根据分镜自然补足中间动作，但不要新增主要角色、地点、道具、事件或替代镜头。
```

Then add identity references, final visual style, quality controls, and constraints.

## Prompt Assembly Checklist

Before returning the final answer:

- Define asset roles in order.
- Choose a board family and panel count.
- State final video duration and aspect ratio.
- Separate storyboard style from final video style.
- Ensure every panel has one main action beat.
- Add continuity anchors: identity, location, prop, screen direction, color palette, lighting.
- Add rhythm or state tracking for fast sequences.
- Add Seedance2 artifact-exclusion text.
- Keep the user-facing output copyable: storyboard prompt first, Seedance2 prompt second, notes last.
