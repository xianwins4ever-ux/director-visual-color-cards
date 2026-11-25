# Midjourney 提示词模板 — David Cronenberg 大卫·柯南伯格风格

> 使用方法：将 `[SUBJECT]` 替换为你的主体描述，按需调整参数

---

## 一、通用风格标签（Universal Style Tags）

```
in the style of David Cronenberg, dark thriller film still,
clinical cold tone, flesh tone, diseased green,
body horror mood, body philosophy,
cinematic film grain, moody atmosphere
```

---

## 二、人物肖像模板

### 模板 A：主角肖像

```
[SUBJECT: a mysterious figure in a dark coat],
in the style of David Cronenberg,
flesh close-up, predominantly diffuse soft light, localized hard light accentuating flesh texture,
clinical cold tone shadows with cool white-green highlights,
body horror expression, tech anxiety atmosphere,
cinematic medium close-up shot, film grain,
flesh and blood dark red --ar 3:4 --style raw --s 750 --v 6
```

### 模板 B：剪影人物

```
[SUBJECT: a silhouetted figure standing in a doorway],
David Cronenberg style, dark thriller,
symmetrical composition,
clinical cold tone, dramatic backlighting,
body philosophy, sex and violence,
symmetrical geometric composition,
grainy cinematic texture --ar 2:3 --style raw --s 500 --v 6
```

---

## 三、场景环境模板

### 模板 C：经典场景

```
[SUBJECT: transformation final chapter],
in the style of David Cronenberg,
clinical cold tone, flesh and blood dark red+diseased green,
fusion of organic and mechanical,
body horror atmosphere, body betrayal, pain and love, tragedy,
cinematic wide shot, film grain, dramatic lighting,
--ar 16:9 --style raw --s 700 --v 6
```

### 模板 D：室内氛围

```
[SUBJECT: a dimly lit interior room with diseased green],
David Cronenberg film aesthetic,
predominantly diffuse soft light, localized hard light accentuating flesh texture, flesh tone,
mirror reflection,
tech anxiety, identity dissolution,
cinematic atmosphere, film grain --ar 16:9 --style raw --s 650 --v 6
```

---

## 四、静物与道具模板

### 模板 G：象征静物

```
[SUBJECT: a symbolic object on a dark table],
David Cronenberg style still life,
predominantly diffuse soft light, localized hard light accentuating flesh texture, creating long shadows,
clinical cold tone ambient light, flesh tone,
body horror, mysterious atmosphere,
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
| 肉体恐怖氛围 | 提示词中加 `临床冷调, 身体哲学` |