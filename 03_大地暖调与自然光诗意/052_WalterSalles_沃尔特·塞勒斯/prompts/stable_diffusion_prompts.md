# Stable Diffusion 提示词模板 — Walter Salles 沃尔特·塞勒斯风格

---

## 风格触发词
`Walter Salles style, brazilian road movie aesthetic, south american earth tones, warm tropical golden sunlight, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k, photorealistic,
cinematic film still, in the style of Walter Salles,
brazilian road movie aesthetic, south american landscape,
warm tropical golden sunlight, golden hour side light,
dusty highway travel, brazilian savanna ochre,
andean mountain brown, highway golden dust,
tropical sunset orange, caramel skin tone,
cerrado green foliage, vintage leather brown,
journey of self-discovery, mentor and mentee bond,
moving vehicle perspective, dust and heat haze,
wide horizon lines, film grain, warm earthy palette
```

## 反向提示词
```
(worst quality, low quality:1.4), sci-fi, neon, cyberpunk,
cool blue tones, studio lighting, modern city skyscrapers,
winter snow, 3d render, cartoon, anime,
overexposed, deformed, text, watermark,
glossy commercial look, wealthy setting
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 公路构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |
| 人物 | ControlNet OpenPose | 0.7-0.8 |

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024 (风景) 或 1024x1536 (肖像)
