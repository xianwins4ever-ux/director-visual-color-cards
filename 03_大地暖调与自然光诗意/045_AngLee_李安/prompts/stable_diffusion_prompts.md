# Stable Diffusion 提示词模板 — 李安 Ang Lee 风格

---

## 风格触发词
`ang lee style, Ang Lee film aesthetic, soft diffused natural light, warm earth palette, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Ang Lee,
soft diffused natural light, gentle side lighting, warm window fill,
warm earth palette, jade green, bamboo forest light,
eastern-western fusion aesthetic, quiet restraint,
nature as emotional mirror, gentle melancholy,
cinematic lighting, 35mm film grain, anamorphic lens, depth of field
```

## 反向提示词
```
(worst quality, low quality:1.4), harsh contrast, neon bright,
fast action, cartoon, anime, 3d render,
oversaturated colors, dramatic theatrical,
overexposed, blurry, deformed, text, watermark
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 平衡构图 | Canny/LineArt | 0.7-0.9 |
| 柔光效果 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩参考 | IP-Adapter(电影截图) | 0.5-0.7 |
| 自然风景 | Segmentation | 0.6-0.7 |

## LoRA训练建议
- 推荐训练集：《卧虎藏龙》《断背山》《饮食男女》高清截图各30-50张
- 重点标签：soft light, warm earth, bamboo, gentle melancholy
- 训练步数：2000-3000步，保留柔和质感

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
