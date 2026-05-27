# Camera Language Requirements

Use this reference when a storyboard needs stronger cinematic camera direction. These patterns are derived from `tata_ai_shots_prompt_summary.md`; adapt the methods, do not paste long source text.

## Universal Camera Formula

Use this formula for each important shot:

```text
视觉风格 + 主体动作/对白/情绪 + 镜头角度 + AI运镜指令 + 环境光影 + 输出参数
```

For storyboard annotation strips, compress it to:

```text
景别 / 角度 / 运镜 / 主体动作 / 走位 / 光影 / 连续性
```

Good camera notes name:

- shot-size function: establishing environment, readable action, facial emotion, decisive detail
- angle: low angle, eye level, high angle, POV high angle, rear view, over-the-shoulder, Dutch tilt, ground-level
- movement: push-in, pullback, follow, tracking, pan, tilt up/down, scan, orbit, handheld drift, rack focus
- subject relation: from behind, from A shoulder to B, camera at eye height, near ground, from dominant character POV
- emotional purpose: entrance power, mystery, exposition, intimacy, oppression, loneliness, instability, speed
- lighting mood: top light, backlight/rim light, bottom light, Tyndall beams, soft window light, neon, moonlight
- safety: normal proportions, no distortion, fixed left/right positions, same side of axis

## Shot Size And Information Flow

Use shot size to split story information and control the audience's viewing order. Avoid cramming environment, action, emotion, and key detail into one all-purpose shot.

| Shot size | Function | Use for | Prompt pattern |
|---|---|---|---|
| 远景/全景 | Establish the whole environment and atmosphere | location, spatial scale, story world | `远景/全景，展示[地点/整体环境]，营造[氛围]` |
| 中景 | Focus on the subject's readable action | walking, entering, interaction, relation between characters | `中景，[人物]正在[动作]，让观众注意到[行为重点]` |
| 近景 | Capture expression and emotional change | gaze shift, hesitation, attraction, fear, decision | `近景，捕捉[表情/眼神变化]，传递[情绪]` |
| 特写 | Magnify the detail that carries the feeling | hand, eye, object, texture, key moment | `特写，[手指/眼神/物品]轻微动作，突出[细节与情绪]` |

### Four-Shot Cinematic Breakdown

Use this pattern when a simple prompt feels flat:

```text
用四个景别拆分同一场景：
1. 远景/全景：交代[地点/环境]，营造[氛围]。
2. 中景：表现[人物动作]，让观众关注[行为重点]。
3. 近景：捕捉[人物表情/眼神变化]，传递[情绪]。
4. 特写：放大[关键细节]，强化[情绪/故事含义]。
整体风格：电影感、自然光影、叙事性镜头语言。
```

Example structure: bakery scene

- 远景/全景: warm bakery exterior/interior atmosphere, shelves and window glow establish place.
- 中景: boy enters and looks around; action becomes readable.
- 近景: boy pauses, gaze catches the bread display; emotion starts.
- 特写: fingers hover near or touch the glass; a concrete detail carries the feeling.

## Lighting Direction And Mood

Use lighting to set mood, not just visibility. Avoid `全亮平光` unless the request needs an interview, e-commerce, catalog, tutorial, or neutral corporate look.

| Lighting | Function | Best scenes | Mood keywords | Prompt pattern |
|---|---|---|---|---|
| 顶光 | Shadows fall from above and carve the face | prison break, interrogation, danger, pressure | mysterious, tense, dangerous, oppressive | `冷色顶光从上方打下，人物面部形成阴影，危险紧张氛围` |
| 逆光 | Rim light outlines hair, shoulders, and silhouette | proposal, reunion, romantic memory, gentle encounter | romantic, dreamy, warm, cinematic outline | `逆光照亮人物轮廓和发丝，背景柔和发光，浪漫电影感` |
| 底光 | Upward light breaks normal shadow logic | horror, thriller, uncanny or abnormal scenes | eerie, unsettling, frightening, unnatural | `底光从下方向上照射，面部阴影反常，制造不安恐怖感` |
| 丁达尔光 | Visible light beams add depth and sacred scale | church, library, forest, trial, temple, epic space | sacred, solemn, spatial, epic | `丁达尔光穿过空气/尘埃形成光束，增强空间纵深和神圣感` |

Lighting prompt template:

```text
场景：[具体场景]
情绪目标：[紧张/浪漫/恐怖/神圣]
光线设计：[顶光/逆光/底光/丁达尔光]
画面效果：通过光线方向和阴影关系塑造[氛围]，避免全亮平光，增强电影感和故事感。
```

## Shot Patterns

### Important Character Entrance

Use when a role needs presence, expectation, or power.

```text
极低机位仰拍，镜头贴近地面，从脚部/衣摆缓慢向上移动，最后停在面部或眼神；人物比例正常无畸变。
```

Avoid adding ultra-wide distortion unless the user explicitly wants exaggeration.

### Mystery Entrance

Use for unknown identity, suspense, corridor/window/street reveals.

```text
背面视角跟随，镜头缓慢上升并横向扫描，先展示空旷环境和光影，再聚焦人物侧脸。
```

Delay the face reveal. Use environment details to build curiosity.

### Character And Environment Exposition

Use when the audience must read both character state and surrounding clues.

```text
平视视角，镜头与人物视线平齐，跟随人物行走，同时以人物为中心做慢速环绕，展示人物状态与周围环境细节。
```

Keep the orbit slow enough that identity and geography stay readable.

### Basic Dialogue

Use for ordinary conversation or information exchange.

```text
双人中景，人物A固定在画面左侧，人物B固定在画面右侧，镜头稳定，保持两人同框对话。
```

### Deep Dialogue Or Conflict

Use for negotiation, argument, confession, or emotional confrontation.

```text
过肩反打镜头，从人物A肩后拍摄人物B，人物A在前景虚化，人物B清晰位于主体位置，观众视角站在人物A一侧。
```

Alternate A-over-shoulder and B-over-shoulder only while preserving the 180-degree axis.

### Background Revealed By Dialogue

Use when a line should naturally reveal danger, worldbuilding, or stakes.

```text
人物说出关键信息后，高位下降镜头或缓慢后拉露出背景环境，让废墟、人群、战场、工厂、城市或自然环境逐渐进入画面。
```

### Emotion From Background

Use when the mood should come from lighting/composition rather than direct emotion labels.

```text
先描写远处背景光影和空间压迫，再让镜头从背景水平环绕至人物正面，使环境情绪包围人物。
```

### Oppression Or Helplessness

Use for interrogation, workplace pressure, confrontation, or strong/weak power relations.

```text
第一人称主观俯拍，从强势方肩膀高度向下俯拍对面人物，利用明显高度差制造压迫感。
```

### Loneliness

Use for loss, farewell, isolation, quiet aftermath, or unresolved sadness.

```text
纯背面视角，人物背对镜头，静止或缓慢前行，环境留白占据大部分画面。
```

### Tension Or Suspense

Use for danger, psychological instability, thriller, or approaching threat.

```text
荷兰倾斜镜头，倾斜15-20度，轻微手持抖动，单个镜头保持短促。
```

Keep tilt below 25 degrees and avoid holding it longer than about 3 seconds.

### Chase Or Fast Action

Use for running, parkour, pursuit, panic, or kinetic motion.

```text
地面视角跟拍，镜头贴近地面跟随人物快速移动，突出脚步、速度感、冲击力和地面反光。
```

## Continuity Rules

### 180-Degree Axis

For two-person dialogue, choose one side of the axis and stay there.

- Wide shot: A remains left, B remains right.
- A close-up: A looks screen-right toward B.
- B close-up: B looks screen-left toward A.
- Do not write camera moves that cross from one side of the axis to the opposite side unless disorientation is intentional.

Use this prompt fragment:

```text
固定人物左右位置，人物A始终在画面左侧，人物B始终在画面右侧，所有镜头保持在同一侧180度轴线范围内拍摄。
```

### 30-Degree Cut Rule

For consecutive shots of the same subject:

- Change camera angle by at least 30 degrees.
- Also change shot size when possible, such as medium shot to close-up.
- Use this to avoid jump-cut / frozen-PPT feeling.

Use this prompt fragment:

```text
同一人物连续切镜头时，镜头角度至少变化30度，并同时改变景别，例如从中景切到特写。
```

## Anti-Patterns

Avoid these unless the user asks for them:

- vague `多运镜` without naming exact movements
- single-shot prompts that dump environment, action, emotion, and detail into one frame
- `全亮平光` when the scene needs story tension, romance, horror, mystery, or sacred scale
- generic `电影感光影` without naming direction, source, shadow behavior, or mood target
- crossing dialogue axis accidentally
- tiny angle changes between consecutive shots
- extreme Dutch tilt held too long
- low-angle ultra-wide shots that distort human proportions
- orbiting around both sides of a dialogue pair without continuity control
- emotional labels without supporting camera, lighting, or background behavior
