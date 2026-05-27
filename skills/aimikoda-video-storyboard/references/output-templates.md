# Output Templates

Use these skeletons when producing Aimikoda-style storyboard outputs. Replace bracketed placeholders.

## Rough Previs Storyboard Prompt

```text
请生成一张可以直接作为 Seedance2 分镜参考图的 rough previs / 动画预演故事板。

项目：[title]
视频目标：[duration]，[aspect ratio]，[purpose]
参考资产：[图像1=角色/产品/Logo/风格参考；图像2=场景/第二角色/道具参考]
最终视频风格：[final-video style]

故事板画面风格：
- 低细节 rough sketch / graphite-gray / manga thumbnail / animation previs 风格。
- 重点是动作、构图、镜头、走位、节奏和连续性，不是精修插画。
- 每格只表现一个清楚 action beat，主体轮廓强，运动方向明确。
- 避免复杂渲染、厚重阴影、概念设定图质感、重复残影或拥挤细节。

版式：
- 单张 [3x3 / 3x4 / 4x4 / 4x6] 故事板，按从左到右、从上到下阅读。
- 面板编号、镜头说明、动作说明和导演条放在画面外侧或底部信息区，不要覆盖关键帧主体。
- 可加入少量制作箭头或彩色标记，但必须清楚、少量、可读。
- 可在顶部加入很小的 final-video style swatches，但不要干扰分镜。

连续性：
- 严格保持[角色/产品/道具/地点]一致。
- 保持屏幕方向、运动方向、空间关系和道具状态连续。
- 每个动作都有可见因果：准备 -> 接触/触发 -> 状态变化 -> 结果。
- 结尾必须有清楚 payoff：[final image/payoff].

镜头节奏：
[列出 8-24 个 beat / camera / action / rhythm / state]
```

## Animatic Track Board Prompt

```text
请生成一张 [aspect ratio] 的专业 animatic track board。

Project: [title] | [genre] | Goal: [duration] [panel count]-panel animatic of [core action]
Continuity: [project id] | Identity source: [asset roles] | Final-video style packet: [style, color, lighting, texture, VFX]

Scene: [location, subject roles, start state, end state, props/effects, must-read causal idea]

Sheet design:
- 单张 [4x3 / 4x4 / 4x6] 网格。
- 每个面板是一个可提取镜头，关键帧区域低细节、清楚、可读。
- 面板外侧或底部包含 compact track board: BEAT / CAMERA / ACTION / RHYTHM / ESCALATION / STATE / STYLE。
- 不要在关键帧区域内生成字幕、Logo、水印、可读 UI 文本或无关技术标记。

Track board:
BEAT: [P01 ...]
CAMERA: [ECU / wide / insert / macro / overhead / OTS / low angle / push-in / whip pan / orbit ...]
RHYTHM: [hold / burst / fast / snap / rise / impact / peak / drop / final spike ...]
ACTION: [per-panel verb phrase]
STATE: [per-panel prop or story state]
STYLE: [per-panel sketch/style note]
```

## Seedance2 Authoritative Blueprint Prompt

```text
将图像1定义为权威分镜/预演/动画蓝图。严格按照图像1从左到右、从上到下的顺序，把每个分镜格作为时间线上的连续镜头或关键动作点来生成视频。不要把整张故事板当作拼贴画、分屏、海报或静态页面。

图像1里的面板边框、编号、标题、文字标注、箭头、颜色标记、导演条、风格色块、轨道表、页面排版和制作备注都只是给模型理解镜头、动作、节奏和连续性的参考，最终视频中不要生成这些元素。

保留分镜中的镜头顺序、构图、主体位置、运动方向、动作节拍、道具状态、空间关系、情绪递进和最终姿态。根据分镜自然补足中间动作，但不要新增主要角色、地点、道具、事件或替代镜头。

身份参考：[图像2/图像3 中的角色、产品或道具定义]
最终视频风格：[style packet]
节奏：[slow cinematic / hard-cut beat sync / rapid staccato / smooth continuous one-take]
画质与约束：[quality and defect controls]
```
