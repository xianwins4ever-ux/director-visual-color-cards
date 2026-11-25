# Stable Diffusion 提示词模板 — George Lucas 乔治·卢卡斯风格

---

## 风格触发词
`George Lucas style, star wars space opera aesthetic, tatooine desert gold, binary sunset orange, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k, photorealistic,
cinematic film still, in the style of George Lucas,
star wars space opera aesthetic,
tatooine desert gold, binary sunset orange,
deep space navy blue, jedi robe brown,
used universe grime, worn and lived-in look,
epic wide establishing shot, low angle hero reveal,
silent film composition, symmetric framing,
lightsaber practical glow, cockpit point of view,
mythic hero's journey, archetypal good vs evil,
film grain, anamorphic lens flares, high contrast
```

## 反向提示词
```
(worst quality, low quality:1.4), modern sci-fi, cyberpunk,
cartoon, anime, 3d render, realistic earth photography,
horror vibe, low budget feel, overexposed,
deformed, text, watermark, clean pristine look
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |
| 对称构图 | ControlNet Tile | 0.5-0.6 |

## 采样参数
Steps:30-40, CFG:7-10, Sampler:DPM++ 2M Karras, 分辨率:1792x1024 (宽幅) 或 1536x1024 (标准)
