# Prompt Templates

Copy and adapt these templates. Replace bracketed placeholders.

## ChatGPT Detailed Storyboard Grid Prompt

```text
请生成一张可以直接作为 Seedance2 图像1参考图的详细制作故事板图片。

主题：[video idea]
视频用途：[ad / short drama / MV / product demo / trailer]
最终视频比例：[9:16 / 16:9 / 1:1]
整体风格：[visual style]
时长目标：[duration]
主体连续性：[character/product/location/style anchors]

画布与布局：
- 生成单张 [3x3 / 4x2 / 3x4] 详细制作故事板网格图，按从左到右、从上到下顺序阅读。
- 每个分镜格分为两个区域：上方/主体区域是真实视频关键帧；下方/窄边栏是制作信息标注。
- 关键帧区域不要出现文字，必须像真实视频画面。
- 制作信息标注要短小清晰，包含：镜头编号、时长、景别、运镜、人物动作、走位、景深/镜头、光影环境、转场。
- 整张图是专业动画/影视制作分镜板，信息完整但不拥挤。

统一要求：
- 所有分镜保持同一主体/产品/场景的视觉一致性。
- 每格只表达一个主要动作或视觉变化。
- 走位要清楚：写明主体从哪里开始、向哪里移动、在哪里停下、看向哪里、与什么互动。
- 运镜要具体，不要只写“多运镜”：每格写明镜头角度、主运镜、速度/能量、主体关系和情绪目的。
- 同一主体连续切镜头时，镜头角度至少变化30度，并同时改变景别，例如从中景切到特写。
- 双人对话保持180度轴线法则，固定人物左右位置；不要让镜头跨轴导致角色互换方向。
- 景深要明确：浅景深、背景虚化、前景遮挡、焦点从A拉到B、广角空间感或长焦压缩。
- 运镜要明确且每镜头以一个主运镜为主：固定、缓慢推近、平稳跟拍、横移、上摇、下摇、轻微环绕、拉焦。
- 不要生成Logo、水印、字幕、对话框；标注文字只放在每格制作信息区，不要覆盖关键帧。

分镜内容：
镜头1：[time]｜景别：[shot size]｜运镜：[camera move]｜人物动作：[action/emotion]｜走位：[blocking/path]｜景深/镜头：[depth/lens]｜光影环境：[lighting/environment]｜转场：[transition]
镜头2：[time]｜景别：[shot size]｜运镜：[camera move]｜人物动作：[action/emotion]｜走位：[blocking/path]｜景深/镜头：[depth/lens]｜光影环境：[lighting/environment]｜转场：[transition]
镜头3：[time]｜景别：[shot size]｜运镜：[camera move]｜人物动作：[action/emotion]｜走位：[blocking/path]｜景深/镜头：[depth/lens]｜光影环境：[lighting/environment]｜转场：[transition]
...

输出为一张高质量详细故事板参考图，画面清晰，标注规整，镜头顺序明确，适合后续直接上传给 Seedance2 作为图像1。
```

## Camera-Language Storyboard Prompt Add-On

Use this block when the user asks for cinematic camera movement, dialogue, entrances, emotion, action, or stronger 镜头感.

```text
镜头语言要求：
- 每个镜头按公式设计：视觉风格 + 主体动作/对白/情绪 + 镜头角度 + AI运镜指令 + 环境光影 + 输出参数。
- 重要人物登场：优先使用极低机位缓慢上升仰视，镜头从脚部/衣摆向上移动并停在脸部或眼神，写明人物比例正常无畸变。
- 神秘登场：使用背面跟拍 + 缓慢上升 + 横向扫描，先展示环境，再聚焦侧脸。
- 人物与环境同时交代：使用平视跟拍 + 以人物为中心的慢速环绕。
- 深入对话或冲突：使用过肩反打镜头，前景肩部虚化，对面人物清晰。
- 双人对话：固定人物A在画面左侧、人物B在画面右侧，所有镜头保持同一侧180度轴线范围内拍摄。
- 情绪压迫：使用第一人称主观俯拍，从强势方肩膀高度向下看对方。
- 孤独或离别：使用纯背面视角，人物背对镜头，环境留白。
- 紧张或悬疑：使用15-20度荷兰倾斜镜头，轻微手持抖动，单镜头不要超过3秒。
- 动作或追逐：使用地面视角跟拍，镜头贴近地面跟随脚步快速移动。
- 同一主体连续切镜头：镜头角度至少变化30度，并同时改变景别，避免跳帧或PPT感。
```

## Aimikoda-Style Rough Previs Board Prompt

Use when the user wants action, choreography, sports, combat, chase, transformation, music-video movement, or any Seedance2-friendly rough board.

```text
请生成一张可以直接作为 Seedance2 分镜参考图的 rough previs / 动画预演故事板。

项目：[title]
视频目标：[duration]，[aspect ratio]，[purpose]
参考资产：[图像1=角色/产品/Logo/风格参考；图像2=场景/第二角色/道具参考]
最终视频风格：[final-video style]

故事板画面风格：
- 故事板本身必须是低细节 rough sketch / graphite-gray / manga thumbnail / animation previs 风格。
- 重点是动作、构图、镜头、走位、节奏和连续性，不是精修插画。
- 每格只表现一个清楚动作 beat，主体轮廓强，运动方向明确。
- 避免复杂渲染、厚重阴影、概念设定图质感、重复残影或拥挤细节。

版式：
- 单张 [3x3 / 3x4 / 4x4 / 4x6] 故事板，按从左到右、从上到下阅读。
- 面板编号、镜头说明、动作说明和导演条必须放在画面外侧或底部信息区，不要覆盖关键帧主体。
- 如果需要箭头或彩色标记，只作为制作标注使用，并保持少量、清楚、可读。
- 可在顶部加入很小的 final-video style swatches，但不要让色块干扰分镜。

连续性：
- 严格保持[角色/产品/道具/地点]一致。
- 保持屏幕方向、运动方向、空间关系和道具状态连续。
- 每个动作都要有可见因果：准备 -> 接触/触发 -> 状态变化 -> 结果。
- 结尾必须有清楚 payoff：[final image/payoff].

镜头节奏：
[用 8-24 个镜头列出 beat / camera / action / rhythm / state]

输出为一张清晰、可读、适合 Seedance2 直接理解的 rough previs 故事板参考图。
```

## Animatic Track Board Prompt

Use for fast-cut assembly, UI motion, product demos, sabotage, beat-synced montage, or 12-24 extractable shots.

```text
请生成一张 [aspect ratio] 的专业 animatic track board。

Project: [title] | [genre] | Goal: [duration] [panel count]-panel animatic of [core action]
Continuity: [project id] | Identity source: [asset roles] | Final-video style packet: [style, color, lighting, texture, VFX]

Scene: [one paragraph with location, subject roles, start state, end state, props/effects, must-read causal idea]

Sheet design:
- 单张 [4x3 / 4x4 / 4x6] 网格。
- 每个面板是一个可提取的镜头，关键帧区域低细节、清楚、可读。
- 面板外侧或底部包含 compact track board: BEAT / CAMERA / ACTION / RHYTHM / ESCALATION / STATE / STYLE。
- 不要在关键帧区域内生成字幕、Logo、水印、可读 UI 文本或无关技术标记。

Panel rules:
- one clear pose/action per panel
- no ghost poses, duplicate silhouettes, heavy cross-hatching, dense shadows, or concept-art finish
- every prop/state change must be visually caused by the previous beat
- screen direction and geography must stay readable

Track board:
BEAT: [P01 ...]
CAMERA: [ECU / wide / insert / macro / overhead / OTS / low angle / push-in / whip pan / orbit ...]
RHYTHM: [hold / burst / fast / snap / rise / impact / peak / drop / final spike ...]
ACTION: [per-panel verb phrase]
STATE: [per-panel prop or story state]
STYLE: [per-panel sketch/style note]

Sequence:
01 [title]: [camera/lens] / [action] / strip: [beat / camera / action / rhythm / state / style]
02 ...
```

## Seedance2 Prompt For Detailed Storyboard Reference

```text
将图像1定义为详细制作故事板参考图。严格参考图像1中的分镜顺序，按照从左到右、从上到下的阅读顺序生成连续视频。不要生成网格拼贴画面，不要把所有分镜同时显示在画面中；请把每个分镜格视为时间线上的连续镜头参考。

图像1中的文字标注仅作为制作说明，请理解其中的景别、运镜、人物动作、走位、景深、光影环境和转场信息，但不要在最终视频中生成任何文字、字幕、编号、标注栏、网格线、Logo或水印。

将图像1中反复出现的[subject/product]定义为[label]，保持其外观、服装/材质、比例、颜色和核心细节一致。

视频内容：[one-sentence story]
镜头节奏：[slow cinematic / fast-cut montage / elegant product ad / anime OP]
运镜执行：严格按照图像1每格标注的运镜执行，每个镜头以一个主运镜为主，镜头衔接自然。
人物动作与走位：严格按照图像1每格标注的人物动作和走位执行，保持动作连续、方向明确、重心稳定。
景深与焦点：参考图像1每格的景深/镜头标注，保持焦点目标清晰，背景虚化和前后景关系自然。
光影色调：[lighting and color]
视觉风格：[style]

生成 [duration] 的 [aspect ratio] 视频，动作自然流畅，镜头衔接顺滑，保持视觉连续性。高清，细节丰富，色彩自然，光影柔和。人物面部稳定不变形，产品形状稳定，避免闪烁、卡顿、穿模、错位、过度变形。保持无字幕，避免生成任何文字、Logo、水印。
```

## Authoritative Storyboard Blueprint Prompt

Use when the storyboard already contains the shot details and Seedance2 should mostly obey, not reinvent.

```text
将图像1定义为权威分镜/预演/动画蓝图。严格按照图像1从左到右、从上到下的顺序，把每个分镜格作为时间线上的连续镜头或关键动作点来生成视频。不要把整张故事板当作拼贴画、分屏、海报或静态页面。

图像1里的面板边框、编号、标题、文字标注、箭头、颜色标记、导演条、风格色块、轨道表、页面排版和制作备注都只是给模型理解镜头、动作、节奏和连续性的参考，最终视频中不要生成这些元素。

保留分镜中的镜头顺序、构图、主体位置、运动方向、动作节拍、道具状态、空间关系、情绪递进和最终姿态。根据分镜自然补足中间动作，但不要新增主要角色、地点、道具、事件或替代镜头。

身份参考：[图像2/图像3 中的角色、产品或道具定义]
最终视频风格：[style packet]
节奏：[slow cinematic / hard-cut beat sync / rapid staccato / smooth continuous one-take]
画质与约束：[quality and defect controls]
```

## Strict Detailed Storyboard-To-Video Prompt

Use this when the detailed storyboard image is already final and video generation should not invent new shots.

```text
严格根据图像1的详细制作故事板生成视频。按照图像1从左到右、从上到下的分镜顺序，逐镜头转化为连续视频。每个镜头都要匹配对应分镜的关键帧构图、主体位置、景别、运镜、人物动作、走位、景深、光影环境和转场说明。不要重新排序，不要新增分镜中没有的主要场景，不要把故事板网格、文字标注或信息栏直接显示在视频里。

[Define subject/product identity and continuity.]
[Describe motion rhythm and camera language.]
[Describe final style, quality, and constraints.]
```

## Clean Board Fallback

Use only when the user explicitly needs a no-text storyboard reference.

```text
请生成一张无文字、无编号、无标注栏的干净故事板图。每格通过视觉方式表达制作信息：用构图表达景别，用运动轨迹和姿态变化表达人物动作与走位，用焦点清晰度和背景虚化表达景深，用光线方向和色调表达光影环境，用相邻画面的动作连续性表达转场。不要生成任何文字、字幕、Logo或水印。
```
