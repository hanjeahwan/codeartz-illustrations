# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一起。

生成调用必须把 `assets/codeartz-ai-cat-reference.png` 作为图像参考输入一并传入。不要只把文件路径写进 prompt；路径文字不会约束角色形象。参考图负责锁定 Codeartz AI 猫的身份、比例、五官、耳机和角色配色；prompt 负责当前图的文章隐喻、构图和动作。

使用内置 `image_gen` 时，先用 `view_image` 打开 `assets/codeartz-ai-cat-reference.png`，再调用 `image_gen`。`image_gen` 不接收文件路径参数；在 prompt 里把这张会话中已可见图片标成 reference image / identity lock。只看图但不在后续 prompt 里绑定它，不算使用参考图。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Input images:
The visible codeartz-ai-cat-reference.png is the reference image and identity lock for Codeartz AI Cat.

Image reference:
Use the attached codeartz-ai-cat-reference.png as the identity lock for Codeartz AI Cat. Preserve the reference character's rounded white cat body, large deep-blue eyes, round tech headphones with cyan glow rings, lavender inner ears, pink blush, small chest screen/paw mark, tail ring, and thin black hand-drawn outline. Adapt the pose and action to the current composition, but do not redesign the character. Do not replace it with a generic cat, black creature, 3D robot, sticker mascot, or commercial cartoon character.

Visual DNA:
Pure white background. Minimalist black hand-drawn product-sketch style. Thin slightly wobbly pen lines. Lots of empty white space. Clean absurd product-sketch feeling with Codeartz AI Cat as the recurring IP character. Global illustration colors are sparse red/orange/blue handwritten accents: orange for the main flow/path/arrows, red for key warnings/problems/results, blue for secondary notes or system feedback. The AI Cat has its own character palette: white body, light gray-blue shadows, bright cyan-blue only on headphones/tail ring/chest screen/glowing hardware, deep blue eyes, pink blush, lavender inner ears. Do not let the bright cyan-blue character accent become the global scene palette. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
Codeartz AI Cat, matching the attached reference image, a soft white AI/robot cat assistant with a round head, large blue eyes, small body, black thin outline, tech headphones with bright cyan-blue glowing rings, lavender inner ears, pink blush, a small chest screen or paw icon, and a tail ring with cyan-blue glow. The AI Cat must perform the core conceptual action, not decorate the scene. It should feel friendly, smart, collaborative, and slightly playful, but not childish. Do not draw it as a black creature, ordinary pet cat, 3D robot, sticker mascot, or commercial poster character.

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
Use this global palette for the illustration: black for line art and main labels, orange for main flow/path/arrows, red only for key warnings/problems/results, blue only for secondary notes or system state. Use the AI Cat palette only on the character: white body, light gray-blue shadows, bright cyan-blue headphones/tail ring/chest screen/glowing hardware, deep blue eyes, pink blush, lavender inner ears. Keep cyan-blue limited and sparse; never use it for the main path, arrows, background, or global scene objects.

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
Regenerate this illustration with the same core meaning and simple layout. Use the attached codeartz-ai-cat-reference.png as the identity lock for Codeartz AI Cat, and make the cat more central to the conceptual action. The AI Cat should be doing the work that explains the idea, not standing beside the diagram. Preserve the clean white background, thin black hand-drawn contour lines, sparse red/orange/blue handwritten accents, and the AI Cat's character palette from the reference image: white body, small cyan-blue hardware glow, pink blush, lavender ear accents. Keep cyan-blue limited to the character hardware or tiny status lights, not the whole scene.
```
