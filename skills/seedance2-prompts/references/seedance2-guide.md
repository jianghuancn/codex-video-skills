# Seedance 2.0 Prompt Reference

Use this reference for detailed template choices, prompt repair, and troubleshooting.

## Core Formulas

### Multimodal Reference

Extract selected elements from images, videos, or audio to generate a new video.

Recommended sentence patterns:

```text
参考图片N中的主体N，生成...
参考视频N中的动作/运镜/风格/音效，生成...
参考音频N中的音色，生成...
```

Best for action transfer, character reuse, atmosphere borrowing, style transfer, effect transfer, camera-language transfer, and audio timbre borrowing.

### Video Editing

Modify the original video locally or globally. Unmentioned parts should stay unchanged.

Recommended sentence patterns:

```text
在视频N的[位置]添加[元素特征]，[出现时机]出现，光影与原视频一致。
严格编辑视频N，将其中的[原特征]修改为[新特征]，其余内容保持不变。
删除视频N中的[元素]，保留[主体/动作/背景/镜头]不变。
```

Do not write `参考视频N` for edits.

### Video Extension

Continue the original video in time while preserving subject, narrative, audio, and visual style.

Recommended sentence patterns:

```text
向后延长视频N，生成视频N之后的内容：...
向前延长视频N，生成视频N之前的内容：...
视频1，[过渡画面描述]，接视频2，[过渡画面描述]，接视频3。
```

Do not write `参考视频N` for extension.

### Combined Tasks

Use when referencing one asset while editing another:

```text
参考图片/视频N的[参考维度]，严格编辑视频X，[具体编辑内容]。
```

## Subject Binding

Define subjects with stable, visible features:

```text
将图片1中穿红色连衣裙、戴草帽的女人定义为女主。
将图片1中的高个子男人定义为警察，将视频1中的矮个子男人定义为小偷。
```

For multiple assets describing the same subject:

```text
将图片1中黑色短发、穿白衬衫的女孩，以及图片2中同样黑色短发、穿蓝色校服的女孩定义为女主。
```

Rules:

- Use 2-3 static features for each subject.
- Repeat the defined label every time the subject appears.
- For undefined simple subjects, use `主体@图片N` every time.
- Keep descriptions compact and non-contradictory.
- Use the reference image for spatial relationships when possible instead of long text.
- Place the most important reference asset earlier in the prompt.

## Shot Sequencing

Complex prompts work best as a time-ordered storyboard.

Shot format:

```text
镜头1： [运镜/切换方式]，[主体]在[场景/位置]做[动作与表情]，[空间变化]，[音频]。
镜头2： ...
镜头3： ...
```

Guidelines:

- Use `镜头1`, `镜头2`, `镜头3` in event order.
- Prefer event order over exact timestamps such as `0-3秒`.
- Each shot should have one main camera move.
- Include action continuity between shots.
- End with a style/quality/constraint sentence.

Poor:

```text
男人在街头紧张地奔跑，画面很有电影感。
```

Better:

```text
镜头1：街巷侧拍，男人从停顿状态缓慢起跑，呼吸变得急促。
镜头2：男人撞翻水果摊，镜头切到手持近景，他快速转头，眼神慌乱。
镜头3：男人借着前冲惯性翻过矮墙，镜头缓慢拉远，定格在空荡街道。
```

## Action Writing

Prioritize:

- Body part detail: hand, leg, head, shoulder, back, eyes, fingers.
- Degree: speed, amplitude, force, softness.
- Low-speed continuous movement: walk, lift, turn, sit, look up, lower head.
- Transition logic: inertia, pause, follow-through, natural shift.
- Emotion as physical behavior.

Emotion conversion examples:

| Abstract emotion | Concrete detail |
|---|---|
| 悲伤 | 低头，肩膀微微颤抖，眼眶泛红，手指攥紧衣角 |
| 喜悦 | 嘴角上扬，眉眼舒展，脚步轻快，忍不住轻笑 |
| 紧张 | 频繁看手表，手指敲击桌面，呼吸急促，眼神闪躲 |
| 愤怒 | 双拳紧握，下颌线紧绷，胸口起伏，眼神锐利 |
| 释然 | 长舒一口气，肩膀放松，抬头望向远方，露出淡笑 |

Avoid piling up multiple large actions in one shot.

## Camera Language

Use standard terms directly:

- Framing: `全景`, `中景`, `近景`, `特写`, `过肩镜头`, `无人机俯瞰`.
- Movement: `固定镜头`, `缓慢推近`, `平稳横移`, `手持跟拍`, `缓慢拉远`, `环绕半圈`.
- Transition: `镜头切至`, `渐隐`, `变焦切换`, `从近景切到全景`.

Constraint: one shot should normally contain only one camera movement. Avoid asking for push, pull, pan, tilt, and tracking all at once.

## Quality, Style, And Constraints

Quality terms:

```text
高清，细节丰富，电影质感，色彩自然，光影柔和，动作自然流畅。
```

Style terms:

```text
复古胶片风格，日系清新，赛博朋克冷蓝紫色调，3D国漫CG仙侠风格，手绘漫画风格，电影纪实风。
```

Common constraints:

```text
保持无字幕，避免生成任何文字或字幕，不要生成Logo，不要生成水印。
人物面部稳定不变形，身体比例稳定，无穿模，无卡顿，无闪烁。
视频全程禁止出现外形、着装、配饰完全一致的人物，禁止生成同款分身、双胞胎效果。
```

If text is requested, do not use `保持无字幕`. Instead specify exact visible text and placement.

## Text Generation

Seedance 2.0 can generate common visible text such as slogans, subtitles, speech bubbles, and title cards. Prefer common characters. Avoid rare characters, unusual symbols, and overly long text.

Slogan template:

```text
画面[时机]逐渐模糊，画面[位置]出现文字“...”，文字为[颜色/风格/出现方式]。
```

Subtitle template:

```text
画面底部出现字幕，字幕内容为“...”，字幕需与音频节奏同步。
```

Speech bubble template:

```text
[角色]说{...}，说话时[角色]周围出现气泡，气泡里写着对应台词。
```

## Audio Writing

Use:

- `（）` for music.
- `<>` for sound effects.
- `{}` for dialogue.

Examples:

```text
（背景中播放着轻柔钢琴）
<远处传来地铁进站声>
女孩低声说{我终于到了}
```

For voice/timbre reference, combine reference label and descriptive timbre:

```text
参考音频1中低厚温润、带细碎颗粒感、语速平稳的中年男声音色，说{...}
```

To reduce Chinese pronunciation mistakes, replace rare or ambiguous words with common homophones when pronunciation matters.

## Asset Strategy

Recommended 4-role setup:

1. Character anchor: face close-up or clean single-subject image.
2. Scene/style reference: environment, lighting, art direction.
3. Camera/action/effect reference: video clip for motion, camera, or effect logic.
4. Rhythm/atmosphere: audio for emotion, music, timbre, or sound design.

Avoid using every possible asset. Too many references can create feature priority conflicts.

For character ID stability:

- Use a face close-up plus one full-body or costume image.
- Avoid multi-view character sheets for a single person when identity fidelity matters; they can be read as multiple subjects.
- Write: `女主的面部特征参考图片1，妆造参考图片2。`

For more than 4 characters:

- Split characters into groups first.
- Generate grouped images, then use grouped images for video generation.

## Failure Repair Checklist

### Character ID drift

Symptoms: face changes midway, character resembles a public figure, identity differs from reference.

Repair:

```text
女主的面部特征严格参考图片1的人脸特写，妆造参考图片2，全程保持同一张脸，五官比例稳定不变形。
```

Place the face reference earlier. Avoid multi-view sheets.

### Unexpected subtitles

Repair:

```text
保持无字幕，避免生成任何文字或字幕。
```

If reference images/videos contain unnecessary text, remove it before using the asset.

### Logo or watermark

Repair:

```text
不要生成Logo，不要生成水印。
```

### Style drift

Repair by naming the target style explicitly near the end and making reference assets match that style when possible:

```text
整体保持3D国漫CG仙侠风格，禁止漂移为真人写实风格。
```

### Twin / duplicate character issue

Repair:

```text
视频全程禁止出现外形、着装、配饰完全一致的人物，禁止生成同款分身、双胞胎效果，同一画面中每个定义角色仅出现一次。
```

Also define every character with a unique label and reference image.

### Extension jump cut

Prompt-side mitigation:

```text
续写段落从视频1结尾的动作惯性自然延续，主体位置、光影、镜头方向与结尾保持一致，优先在切镜或转场后进入新场景。
```

Post-production mitigation: trim around the join if needed, such as deleting a few frames from the previous segment and one frame from the next segment, then inspect continuity.

### Extension quality degradation

Repair:

- Prefer high-quality original reference images.
- Avoid repeated extension chains.
- For repeated generated-video extension, consider a white-model intermediate:

```text
将视频转为白色3D模型，人物统一为纯白3D模型，无色彩、无纹理、无阴影，纯白背景，结构稳定、运动流畅。
```

### Effects not matching

If a specific effect has precise timing or logic, use a reference video:

```text
参考视频1的金色粒子特效运动轨迹，让图片2中的人物吹笛子时身边环绕相同粒子特效。
```

## Ready-Made Examples

### Dorm Dialogue Short

```text
将图片1中黑色长发、穿浅色卫衣的女孩定义为女主。图片2作为宿舍场景参考，参考视频1的室内中景推近运镜，音频1作为轻柔环境声参考。

镜头1：傍晚，女主走到宿舍门口，镜头中景平稳跟拍，暖黄色日光从窗外洒进走廊，女主在门口停顿，轻轻深呼吸，手指微微攥紧书包带。
镜头2：女主推开门走进宿舍，镜头切到室内中景，舍友们整理书本时抬头看向女主，其中一人笑着问{考得怎么样呀，过了吗}，镜头在几人之间缓慢切换半身特写。
镜头3：女主先低头，肩膀微微收紧，随后抬头露出忍不住的笑意，说{骗你们的}，舍友们轻轻打闹，镜头缓慢拉远定格在宿舍全景。

全程高清电影纪实风，色调温暖，光影柔和，人物面部稳定不变形，动作自然流畅，无卡顿无闪烁；环境音效与音频1自然融合。
```

### Product Replacement Edit

```text
严格编辑视频1，将视频1中桌面中央的香水瓶替换成图片1中的面霜瓶，面霜瓶大小、透视和光影与原桌面一致。人物手部动作、镜头运动、桌面背景和其他物品保持不变。高清细节，材质真实，无穿模，无闪烁，不要生成Logo，不要生成水印。
```

### Backward Extension

```text
向后延长视频1，生成视频1之后的内容：白衣男子从停顿状态自然向前一步，肩膀放松，转头看向镜头外的朋友，语气平静地说{It’s not that bad. You are just stressed. Everyone goes through this.} 镜头保持视频1结尾的过肩视角和柔和室内光线，动作连贯，音色自然，画面高清稳定，无字幕，不要生成Logo，不要生成水印。
```
