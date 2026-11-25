# Stable Diffusion 提示词模板 — 安东尼·明格拉 Anthony Minghella风格

---

## 风格触发词
`anthony_minghella_style, Anthony Minghella film aesthetic, epic romance, cinematic film still`

## 正向提示词
```
masterpiece, best quality, ultra detailed, 8k,
cinematic film still, in the style of Anthony Minghella,
sahara desert gold, golden desert haze, soft memory diffusion, romantic natural light,
sweeping desert vistas, romantic close-up,
epic romance, memory and nostalgia atmosphere,
cinematic lighting, film grain, depth of field, natural lighting
```

## 反向提示词
```
(worst quality, low quality:1.4), flat lighting, cartoon, anime, 3d render,
clean sterile look, overexposed, blurry, deformed, text, watermark,
harsh shadows, modern digital aesthetic
```

## ControlNet推荐
| 效果 | 模型 | 强度 |
|------|------|------|
| 构图 | Canny/LineArt | 0.7-0.9 |
| 光线 | Depth+IP-Adapter | 0.6-0.8 |
| 色彩 | IP-Adapter(电影截图) | 0.5-0.7 |

## 采样参数
Steps:30-40, CFG:6-9, Sampler:DPM++ 2M Karras, 分辨率:1536x1024
