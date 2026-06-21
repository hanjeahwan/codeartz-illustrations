# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一起。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Visual DNA:
Pure white background. Minimalist hand-drawn product-sketch style. Thin black slightly wobbly contour lines. Lots of empty white space. Use the Codeartz AI Cat as the recurring IP character. The color logic is white body + cyan-blue tech glow + pink/lavender cute accents. Use light gray-blue for soft shadows and structure turns, bright cyan-blue for glowing devices and system paths, deep blue for eye dark areas and tech emphasis, pink for blush or gentle emotional accents, and lavender for inner ears and small highlights. Sparse handwritten Chinese annotations in deep blue, cyan-blue, or small pink/lavender accents. No gradients, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no dense explainer page, no realistic UI.

Recurring IP character required:
Codeartz AI Cat, a soft white AI/robot cat assistant with a round head, large blue eyes, small body, black thin outline, tech headphones with bright cyan-blue glowing rings, lavender inner ears, pink blush, a small chest screen or paw icon, and a tail ring with cyan-blue glow. The AI Cat must perform the core conceptual action, not decorate the scene. It should feel friendly, smart, collaborative, and slightly playful, but not childish. Do not draw it as a black creature, ordinary pet cat, 3D robot, sticker mascot, or commercial poster character.

Theme:
{正文配图主题}

Structure type:
{结构类型：Workflow / 系统局部 / 前后对比 / 角色状态 / 概念隐喻 / 方法分层 / 地图路线 / 小漫画分镜}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：AI 猫在哪里、正在做什么、主要物件是什么、信息如何流动}

Suggested elements:
{元素1} / {元素2} / {元素3} / {元素4}

Chinese handwritten labels:
{标注词1} / {标注词2} / {标注词3} / {标注词4} / {可选标注词5}

Color use:
White for the AI Cat body and clean background. Black for thin outlines and a few main labels. Light gray-blue for shadow and structure turns. Bright cyan-blue for glow, path, feedback state, headphones, tail ring, and chest screen. Deep blue for eyes and tech emphasis. Pink only for blush or small emotional notes. Lavender only for inner ears or tiny highlights. Avoid the old red/orange-heavy palette.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten Chinese labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, dense explainer, commercial poster, or childish cartoon. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, cute but not childish, techy but not heavy, strange but clean.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

增强角色参与感：

```text
Regenerate this illustration with the same core meaning and simple layout, but make the Codeartz AI Cat more central to the conceptual action. The AI Cat should be doing the work that explains the idea, not standing beside the diagram. Preserve the white body, cyan-blue tech glow, pink blush, lavender ear accents, thin black contour lines, clean white background, and sparse handwritten Chinese labels.
```
