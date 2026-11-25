# Stable Diffusion 提示词模板 — James Cameron 詹姆斯·卡梅隆风格

> 适用于 SDXL / 1.5，配合 LoRA 使用效果更佳

---

## 一、风格 LoRA 触发词（推荐组合）

```
james cameron style, blockbuster sci-fi film,
blue-steel mechanical, chrome metal aesthetic,
80s 90s sci-fi cinematic, high contrast warm-cool,
epic cinematic composition, bioluminescent glow
```

---

## 二、正向提示词模板（Positive Prompt）

### 模板结构
`[主体描述] + [风格标签] + [光线色彩] + [构图运镜] + [质量标签]`

### 完整示例：终结者T-800

```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still of a muscular cyborg in black leather,
chrome metal endoskeleton visible under torn skin,
glowing red eye, holding a large weapon,
standing in a rain-soaked dark alley at night,
in the style of james cameron, terminator aesthetic,
cold blue-steel lighting, orange fire reflections on chrome,
rain-slicked streets reflecting neon lights,
low angle imposing shot, expressionless face,
80s sci-fi action film, film grain,
high contrast between cold blue and warm orange,
detailed metal texture, cinematic lighting
```

### 完整示例：阿凡达潘多拉森林

```
masterpiece, best quality, ultra detailed, 8k,
vast alien forest at night with bioluminescent plants,
Na'vi blue-skinned humanoid figure among glowing trees,
cyan-green bioluminescence everywhere,
purple and magenta alien foliage,
floating glowing seeds, multiple moons in sky,
in the style of james cameron, avatar aesthetic,
epic alien landscape, magical natural wonder,
vivid saturated cyan-green and purple colors,
wide cinematic shot, film grain, blockbuster scale,
ethereal bioluminescent lighting
```

### 完整示例：深海幽光

```
masterpiece, best quality, ultra detailed, 8k,
deep ocean abyss with bioluminescent creatures,
deep blue-black water, light beams from above,
cyan and blue glowing alien creatures,
underwater submersible with headlights,
bubbles and particles floating,
mysterious glowing underwater structure,
in the style of james cameron, the abyss aesthetic,
ethereal underwater lighting, sense of immense depth,
cinematic underwater shot, blue-dominated palette,
film grain, awe-inspiring deep sea atmosphere
```

---

## 三、反向提示词（Negative Prompt）

```
(worst quality, low quality:1.4),
pastel colors, soft dreamy, washed out,
cheap CGI look, low budget, cartoon, anime,
bright cheerful, romantic comedy, sunny day overexposed,
blurry, deformed, ugly, bad anatomy,
shaky cam, found footage, phone camera look,
medieval, fantasy magic, sword and sorcery,
text, watermark, logo, signature
```

---

## 四、ControlNet 推荐组合

| 效果 | ControlNet 模型 | 强度 |
|------|---------------|------|
| 机械/机甲精确设计 | Canny / LineArt | 0.7-0.9 |
| 史诗构图/景深 | Depth Map | 0.7-0.8 |
| 人物姿态（战士/动作） | OpenPose | 0.8 |
| 光线控制（爆炸/水下光） | Depth + IP-Adapter | 0.6-0.8 |
| 色彩匹配（终结者/阿凡达截图） | IP-Adapter (参考电影截图) | 0.5-0.7 |

---

## 五、采样参数推荐

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Steps | 30-50 | DPM++ 2M Karras |
| CFG Scale | 7-10 | 大片感需要较高CFG |
| Sampler | DPM++ 2M Karras | 金属质感和光影表现好 |
| 分辨率 | 1536×1024 (宽屏) / 2048×1024 (超宽) | SDXL 原生尺寸 |
| 高分辨率修复 | 0.4-0.6 denoising | 增强金属细节和爆炸质感 |

---

## 六、LoRA 训练建议

如要自制 Cameron LoRA：

- **训练素材**：20-25张高清截图（终结者2/阿凡达/深渊/异形2各4-6张）
- **触发词**：`james cameron style, terminator aesthetic`
- **类别词**：`80s sci-fi film, blockbuster cinematic, sci-fi action movie still`
- **训练步数**：2500-3500步（SDXL）
- **重点捕捉**：蓝钢冷色调、镀铬金属反射、火焰橙暖光对比、生物荧光青、史诗广角构图
