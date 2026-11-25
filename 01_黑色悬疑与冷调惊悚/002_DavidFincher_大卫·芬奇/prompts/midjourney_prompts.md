# Midjourney 提示词模板 — David Fincher 大卫·芬奇风格

> 使用方法：将 `[SUBJECT]` 替换为你的主体描述，按需调整参数

---

## 一、通用风格标签（Universal Style Tags）

```
in the style of David Fincher, dark thriller film still,
dark green-yellow palette, grimy cold texture, low-key lighting,
psychological thriller mood, morbid distortion,
cinematic film grain, moody atmosphere
```

---

## 二、人物肖像模板

### 模板 A：主角肖像

```
[SUBJECT: a mysterious figure in a dark coat],
in the style of David Fincher,
precise symmetrical composition, side backlighting, predominantly cool tones with warm yellow accents,
dark green-yellow palette shadows with sickly yellow-green highlights,
psychological thriller expression, existential anxiety atmosphere,
cinematic medium close-up shot, film grain,
fluorescent green --ar 3:4 --style raw --s 750 --v 6
```

### 模板 B：剪影人物

```
[SUBJECT: a silhouetted figure standing in a doorway],
David Fincher style, dark thriller,
low angle shot,
dark green-yellow palette, dramatic backlighting,
morbid distortion, urban alienation,
low angle shot,
grainy cinematic texture --ar 2:3 --style raw --s 500 --v 6
```

---

## 三、场景环境模板

### 模板 C：经典场景

```
[SUBJECT: rainy night manhunt],
in the style of David Fincher,
dark green-yellow palette, swamp dark green+rotten yellow amber,
slow dolly push-in,
psychological thriller atmosphere, filth, despair, hunt,
cinematic wide shot, film grain, dramatic lighting,
--ar 16:9 --style raw --s 700 --v 6
```

### 模板 D：室内氛围

```
[SUBJECT: a dimly lit interior room with low-key lighting],
David Fincher film aesthetic,
side backlighting, predominantly cool tones with warm yellow accents, grimy cold texture,
venetian blind shadows,
existential anxiety, obsessive-compulsive aesthetics,
cinematic atmosphere, film grain --ar 16:9 --style raw --s 650 --v 6
```

---

## 四、静物与道具模板

### 模板 G：象征静物

```
[SUBJECT: a symbolic object on a dark table],
David Fincher style still life,
side backlighting, predominantly cool tones with warm yellow accents, creating long shadows,
dark green-yellow palette ambient light, grimy cold texture,
psychological thriller, mysterious atmosphere,
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
| 心理悬疑氛围 | 提示词中加 `暗绿黄色调, 病态扭曲` |