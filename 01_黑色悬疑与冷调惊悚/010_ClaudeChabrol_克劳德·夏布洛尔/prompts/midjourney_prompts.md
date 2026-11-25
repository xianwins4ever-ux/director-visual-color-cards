# Midjourney 提示词模板 — Claude Chabrol 克劳德·夏布洛尔风格

> 使用方法：将 `[SUBJECT]` 替换为你的主体描述，按需调整参数

---

## 一、通用风格标签（Universal Style Tags）

```
in the style of Claude Chabrol, dark thriller film still,
French cool tone, desaturated treatment, grey-brown palette,
everyday fear mood, bourgeois hypocrisy,
cinematic film grain, moody atmosphere
```

---

## 二、人物肖像模板

### 模板 A：主角肖像

```
[SUBJECT: a mysterious figure in a dark coat],
in the style of Claude Chabrol,
bourgeois space composition, predominantly soft light, natural lighting effect, understated and subtle,
French cool tone shadows with milky warm white highlights,
everyday fear expression, secrets and lies atmosphere,
cinematic medium close-up shot, film grain,
moss green accents --ar 3:4 --style raw --s 750 --v 6
```

### 模板 B：剪影人物

```
[SUBJECT: a silhouetted figure standing in a doorway],
Claude Chabrol style, dark thriller,
window and door frame composition,
French cool tone, dramatic backlighting,
bourgeois hypocrisy, psychological undercurrent,
door frame window frame composition,
grainy cinematic texture --ar 2:3 --style raw --s 500 --v 6
```

---

## 三、场景环境模板

### 模板 C：经典场景

```
[SUBJECT: village winter],
in the style of Claude Chabrol,
French cool tone, cool grey-bluegreen+dusty grey-brown,
staircase turn,
everyday fear atmosphere, rural oppression, friend's depravity,
cinematic wide shot, film grain, dramatic lighting,
--ar 16:9 --style raw --s 700 --v 6
```

### 模板 D：室内氛围

```
[SUBJECT: a dimly lit interior room with grey-brown palette],
Claude Chabrol film aesthetic,
predominantly soft light, natural lighting effect, understated and subtle, desaturated treatment,
mirror reflection,
secrets and lies, moral ambiguity,
cinematic atmosphere, film grain --ar 16:9 --style raw --s 650 --v 6
```

---

## 四、静物与道具模板

### 模板 G：象征静物

```
[SUBJECT: a symbolic object on a dark table],
Claude Chabrol style still life,
predominantly soft light, natural lighting effect, understated and subtle, creating long shadows,
French cool tone ambient light, desaturated treatment,
everyday fear, mysterious atmosphere,
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
| 日常恐惧氛围 | 提示词中加 `法式冷调, 中产阶级虚伪` |