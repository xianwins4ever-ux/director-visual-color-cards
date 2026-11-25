# Midjourney 提示词模板 — John Carpenter 约翰·卡朋特风格

> 使用方法：将 `[SUBJECT]` 替换为你的主体描述，按需调整参数

---

## 一、通用风格标签（Universal Style Tags）

```
in the style of John Carpenter, dark thriller film still,
dark blue shadows, synthwave blue tone, warm yellow point light source,
survival fear mood, isolation and helplessness,
cinematic film grain, moody atmosphere
```

---

## 二、人物肖像模板

### 模板 A：主角肖像

```
[SUBJECT: a mysterious figure in a dark coat],
in the style of John Carpenter,
widescreen composition, hard side lighting, predominantly single light source, heavy shadows,
dark blue shadows shadows with warm amber yellow highlights,
survival fear expression, unknown creature atmosphere,
cinematic medium close-up shot, film grain,
police lights red and blue --ar 3:4 --style raw --s 750 --v 6
```

### 模板 B：剪影人物

```
[SUBJECT: a silhouetted figure standing in a doorway],
John Carpenter style, dark thriller,
low angle shot,
dark blue shadows, dramatic backlighting,
isolation and helplessness, sci-fi horror,
flashlight beam composition,
grainy cinematic texture --ar 2:3 --style raw --s 500 --v 6
```

---

## 三、场景环境模板

### 模板 C：经典场景

```
[SUBJECT: Antarctic base exploration],
in the style of John Carpenter,
dark blue shadows, deep ocean dark blueblack+flashlight yellow,
porch framing,
survival fear atmosphere, isolation and helplessness, unknown creature, trust collapse,
cinematic wide shot, film grain, dramatic lighting,
--ar 16:9 --style raw --s 700 --v 6
```

### 模板 D：室内氛围

```
[SUBJECT: a dimly lit interior room with warm yellow point light source],
John Carpenter film aesthetic,
hard side lighting, predominantly single light source, heavy shadows, synthwave blue tone,
atmospheric smoke,
unknown creature, synth score,
cinematic atmosphere, film grain --ar 16:9 --style raw --s 650 --v 6
```

---

## 四、静物与道具模板

### 模板 G：象征静物

```
[SUBJECT: a symbolic object on a dark table],
John Carpenter style still life,
hard side lighting, predominantly single light source, heavy shadows, creating long shadows,
dark blue shadows ambient light, synthwave blue tone,
survival fear, mysterious atmosphere,
extreme close-up macro shot, cinematic lighting,
film grain --ar 1:1 --style raw --s 650 --v 6
```

---

## 五、负面提示词

```
--no bright colors, cartoon style, anime,
happy cheerful expression, flat lighting,
overexposed, low contrast, blurry,
modern smartphone, digital displays
```

---

## 六、参数速查

| 效果 | 参数 |
|------|------|
| 电影感最强 | `--s 750 --style raw --v 6` |
| 更写实/更低干预 | `--s 250 --style raw --v 6` |
| 更艺术化 | `--s 900 --v 6` |
| 宽银幕电影 | `--ar 16:9` |
| 肖像竖版 | `--ar 3:4` |
| IMAX 宽屏 | `--ar 2.35:1` |
| 生存恐惧氛围 | 提示词中加 `暗蓝阴影, 孤立无援` |