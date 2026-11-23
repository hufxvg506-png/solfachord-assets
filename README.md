# 《女杰和弦》角色差分资产库 (Solfachord Assets)

> 酒馆 (SillyTavern) 角色卡《女杰和弦 · 天穹重奏》全域 229 位女杰头像表情差分云端素材库。

---

## 📖 项目简介 (Overview)

本仓库用于托管酒馆角色卡《女杰和弦》中全部 229 位角色的 8 种官方标准表情差分头像、立绘资源及清单文件 (`manifest.json`)。

当你在酒馆中与角色对话并触发对白渲染标签时，前端助手脚本会自动根据角色名与当前情绪状态，动态拉取并展示对应的面部表情。

---

## 🎨 资源规格标准 (Asset Specifications)

- **图像格式**：`.webp`（高压缩比、高色彩保真度）
- **分辨率**：`512 × 512` 像素（正方形）
- **构图规范**：纯头部与微半身近景（紧凑 Headshot Portrait，保留头饰、帽子、光环上缘呼吸空间）
- **背景风格**：干净纯白背景 (`solid white background`)，无边框残留，自然动漫色彩

### 8 种官方标准表情分类 (Official 8 Expressions)

| 组别 | 包含表情 (Expressions) | 视觉特征描述 |
| :--- | :--- | :--- |
| **第 1 组** | **微笑** (smile) / **生气** (angry) | 温柔闭口笑、欢快眼神 vs 怒目圆睁、微蹙眉、咬牙切齿 |
| **第 2 组** | **惊讶** (surprised) / **疲惫** (tired) | 瞳孔骤缩、张嘴吃惊 vs 半闭眼皮、疲乏脱力、虚汗 |
| **第 3 组** | **委屈** (sad) / **黑化** (yandere) | 泪眼盈眶、嘴角微瘪 vs 空洞眼神、诡异轻笑、阴影脸 |
| **第 4 组** | **害羞** (blush) | 视线移开、脸颊与鼻尖深粉红晕、微窘局促 |
| **第 5 组** | **战损** (damaged) | 脸颊划痕、微尘与创口贴、坚毅或吃痛神情 |

---

## 🚀 酒馆前端调用语法 (SillyTavern Integration)

在酒馆对话中，助手脚本与正则会自动解析以下标签格式：

```html
<say char="芙莉西亚之虫惑魔" diff="生气">你……你在乱摸哪里啊！笨蛋！</say>
```

前端会根据 `char`（角色名）与 `diff`（表情名），优先从本地缓存或 CDN 匹配对应的头像：
```
img/chord_diff/<角色名>/<表情>.webp
```

---

## 🌐 在线 CDN 镜像加速 (jsDelivr CDN)

本仓库已接入 jsDelivr 免费全球加速 CDN，国内直连高速免翻墙：

```text
https://fastly.jsdelivr.net/gh/hufxvg506-png/solfachord-assets@main/<角色名>/<表情>.webp
```

**示例链接**：
- 芙莉西亚之虫惑魔 · 微笑：
  `https://fastly.jsdelivr.net/gh/hufxvg506-png/solfachord-assets@main/芙莉西亚之虫惑魔/微笑.webp`
- 资源清单文件 (`manifest.json`)：
  `https://fastly.jsdelivr.net/gh/hufxvg506-png/solfachord-assets@main/manifest.json`

---

## 📂 仓库目录结构 (Directory Structure)

```text
solfachord-assets/
├── README.md               # 仓库项目说明文档
├── manifest.json           # 差分资源全量清单索引
└── <角色名>/                # 229 位角色独立目录
    ├── 微笑.webp
    ├── 害羞.webp
    ├── 委屈.webp
    ├── 生气.webp
    ├── 惊讶.webp
    ├── 战损.webp
    ├── 黑化.webp
    └── 疲惫.webp
```

---

## 📜 许可说明 (License)

本仓库素材仅用于《女杰和弦》个人二创与非营利性酒馆 AI 角色卡测试交流，禁止任何形式的商业转售与未授权商用。
