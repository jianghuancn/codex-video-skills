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
