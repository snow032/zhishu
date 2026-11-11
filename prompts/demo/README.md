# 三张样图 · 规格卡与实际出图提示词

用 `../知乎头图-单次出图版.md` 的流程本地实跑，覆盖三类最容易翻车的分支。
输出均为 1920×1080 PNG。

---

## 01 · 具名人物 + 数据类（最严：主角必须缺位）

模拟话题：`某球员砍下 13 分 4 板 4 助`

```json
{
  "主语类型": "A 具名人物（篮球运动员）+ 数据类",
  "主体形态": "具名公众人物 + 成绩数据 → 不得出现本人及同项目从业者",
  "信号元素": "篮球与篮筐、三根递增发光数据柱（不可替换）",
  "具象主体层": "球场木地板与篮筐一角空景，前景一只比赛用球",
  "信息表达层": "三根发光数据柱自左向右递增，读出「得分 / 篮板 / 助攻」三项",
  "表达层级": "L2 场景全景（无人物）",
  "画面要素": ["室内球场木地板与边线", "篮筐与网", "前景比赛用球", "三根金色发光递增数据柱"],
  "人物核对": "无具名人物出镜 ✓ / 无同项目运动员作为主体 ✓",
  "镜头构图": "中近景，低角度仰视篮筐，浅景深，背景球馆虚化",
  "媒介": "写实概念摄影",
  "色调": "球场暖木色 + 鲜草绿 #4CAF6E + 数据柱金光 #E8C87A",
  "自检": "无本人形象 / 无同项目运动员主体 / 数字有承载 / 无文字标识 / 双层信息齐备 / 明亮通透"
}
```

实际送入图像模型的描述（英文，便于模型遵循）：

> Realistic conceptual sports photography, 16:9 horizontal composition. An empty indoor basketball court corner: warm honey-colored wooden floor with painted boundary lines, a basketball hoop with a white net seen from a low upward angle, and one game basketball resting in the foreground. Rising from the floor on the right side are three abstract glowing golden vertical light bars of increasing height, pure glowing geometry with soft bloom. Absolutely no people anywhere in the frame. Bright, airy, high-key lighting with soft warm light from the upper side, shallow depth of field, softly blurred arena background. Color palette: warm wood tones, fresh grass green, golden glow. Leave roughly 25 percent low-detail space on the right side for a title overlay. Absolutely no text, no letters, no numbers, no logos, no signage, no scoreboard characters, no badges, no flags anywhere in the image.

出图核验：无人物 ✓｜无文字与标识 ✓｜器材可读（篮筐 + 球）✓｜数据柱递增可读 ✓｜明亮通透 ✓
偏差：三根光柱占用了右侧留白区，叠标题需改到左下。

---

## 02 · 平台 / 机构 + 发布新规类（必须品类道具 + 规则承载物双层）

模拟话题：`某阅读平台发布创作新规`

```json
{
  "主语类型": "C 机构组织 / D 平台产品 + 发布新规",
  "主体形态": "平台不可指认 → 用品类通用道具代替，禁 logo 与界面真实文字",
  "信号元素": "成摞小说与手稿 + 条款文件与印章（不可替换）",
  "具象主体层": "书桌平铺：成摞小说、翻开的空白书页、抽象色块界面手机、钢笔",
  "信息表达层": "条款文件上的红色方框标注 + 圆形印章 + 印章上方金色光环 + 天平",
  "表达层级": "L2 场景全景（无人物）",
  "画面要素": ["成摞小说与手稿", "翻开的空白书页", "抽象色块界面手机", "钢笔", "带红框标注的条款文件与印章", "黄铜天平"],
  "人物核对": "无人物出镜 ✓",
  "镜头构图": "微俯平铺，中景，柔和投影",
  "媒介": "干净质感概念静物摄影",
  "色调": "洁净暖白 + 深蓝 #1B3A6B + 暖金 #D9A94A",
  "自检": "品类可读 ✓ / 新规可读 ✓ / 无 logo 无真实文字 / 双层信息齐备 / 明亮通透"
}
```

> Bright clean conceptual still-life photography, 16:9 horizontal composition, a desk scene shot slightly from above: a tall stack of novels and handwritten manuscript pages, one book lying open with completely blank featureless pages, a smartphone lying flat whose screen shows only abstract soft gray color blocks as a reading interface, a fountain pen, a single printed document sheet marked with a red rectangular highlight frame and a round red ink stamp impression beside it, and a small brass balance scale. A soft glowing golden halo ring floats above the stamp. Bright high-key daylight from above, airy and clean, warm white background with deep navy blue and warm gold accents. Leave roughly 25 percent low-detail empty area in the upper left for a title overlay. No people. Absolutely no readable text, no letters, no numbers, no logos, no brand marks: every page, paper sheet and screen is blank color blocks and abstract lines only.

出图核验：品类道具齐 ✓｜规则承载物齐（红框 + 印章 + 天平 + 钢笔）✓｜无人物 ✓｜左上留白 ✓
偏差：手稿页出现了抽象手写笔迹、圆形印章内有疑似纹样字符 —— 属「无字符」边界情况。
量产时建议在提示词里补一句：手稿只用等距抽象横线，印章只有纯色同心圆环与素面纹路，内部不得有任何笔画。

---

## 03 · 身份指代人物类（必须出人、必须东亚面孔、必须数量承载）

模拟话题：`女子首次跑马拉松跑进三小时`

```json
{
  "主语类型": "A' 身份人物（女性跑者）+ 成绩数据",
  "主体形态": "身份指代 → 鼓励出现人物，可出正脸，普通路人长相",
  "信号元素": "红色塑胶跑道与白色分道线 + 跑者 + 递增发光柱（不可替换）",
  "具象主体层": "塑胶跑道上奔跑中的女性跑者，运动背心短裤 + 空白号码布",
  "信息表达层": "跑道内侧一组递增发光柱，承载「成绩推进」的程度感",
  "表达层级": "L2 场景全景（含人物）",
  "画面要素": ["红色塑胶跑道与白色分道线", "奔跑中的东亚女性跑者", "空白号码布", "一组递增发光柱", "虚化树木与晨光"],
  "人物核对": "性别 女 ✓ / 年龄 三十上下 ✓ / 装束 运动背心短裤与跑鞋 ✓ / 国籍 东亚面孔 ✓ / 数量 1 人 ✓ / 行为 真的在跑 ✓",
  "镜头构图": "侧向跟拍中景，浅景深，背景轻微动势模糊",
  "媒介": "写实概念摄影",
  "色调": "跑道砖红 + 鲜草绿 #4CAF6E + 暖白 + 金色光",
  "自检": "身份无错位 / 无名人相似度 / 数字有承载 / 无号码数字 / 无赞助标识 / 明亮通透"
}
```

> Realistic conceptual sports photography, 16:9 horizontal composition. A single East Asian woman runner in her early thirties with an ordinary everyday face, wearing a plain solid-color running singlet and shorts and a completely blank white bib card with no characters on it, captured mid-stride running on a red rubber running track with white lane lines, body language relaxed and powerful, expression focused. Along the inner edge of the track, three abstract glowing ascending light bars of increasing height rise from the ground as pure geometry with soft bloom. Bright clear morning sunlight, high-key and airy, slight motion blur in the background, shallow depth of field. Color palette: track brick red, fresh grass green, warm white, golden light accents. Leave roughly 25 percent low-detail space on the left for a title overlay. Absolutely no text, no letters, no numbers, no logos, no sponsor marks, no flags, no team emblems anywhere in the image. The face must look like an ordinary anonymous person, not resembling any real celebrity.

出图核验：东亚女性 ✓｜装束与动作一致 ✓｜号码布空白 ✓｜无任何文字与赞助标识 ✓｜左侧留白 ✓
偏差：光柱出了 4 根而非指定的 3 根 —— 图像模型对小数量计数不稳定。
若数量本身是话题信息（如「三连冠」），需改用「阶梯台阶」「成组堆叠实物」这类有物理结构的承载物，或生成后人工复核。

---

## 复用要点

1. 三段英文描述都严格按转写模板的语序写：媒介 → 主体 → 要素 → 信息层 → 镜头 → 光线 → 色调 → 留白 → 无字符。同批保持语序不变，风格才稳定。
2. 负面约束一律写成「替代物 + 否定」的组合：先说清楚空白号码布、抽象色块界面、空白书页，再补一句总的禁止，命中率远高于只写禁止。
3. 图像模型不可靠的两件事：小数量精确计数、印章与纸面上的细碎纹样。涉及数字落地时优先选有物理结构的承载物。
