---
name: h3-bullet-catch-diagonal-geometry
description: 'Use for H3 T2VA sniper bullet-catch diagonal geometry.'
version: '1.0.0'
author: 'Hermes Agent'
license: 'MIT'
tags:
  - h3
  - t2va
  - bullet-catch
  - spatial-geometry
  - time-stop
  - force-field
  - bullet-cam
metadata:
  hermes:
    tags: [h3, t2va, bullet-catch, spatial-geometry, time-stop, force-field, bullet-cam]
    related_skills: [creative/h3-prompt-writing, creative/h3-time-stop-engineering, creative/h3-spatial-action-sync]
---

# H3 Bullet-Catch Diagonal Geometry Skill

## When to Use

**This skill activates when the user request contains ALL of these semantic elements:**

| Element | Keywords (EN) | Keywords (ZH) |
|---------|---------------|---------------|
| **Model/Mode** | H3, T2VA, text-to-video | H3, T2VA, 文字生成視頻 |
| **Core Action** | sniper, bullet catch, catch bullet, bullet cam | 狙擊手, 子彈接住, 子彈被夾住, 夾住子彈, 子彈鏡頭, 跟隨子彈 |
| **Spatial Geometry** | diagonal geometry, bottom-left, top-right, right window, floor-to-ceiling window | 對角線幾何, 左下, 右上, 右側窗, 落地窗, 空間幾何, 相對位置 |
| **Time-Stop Mechanics** | time stop, force field, state jump, pixel-level static, zero-latency, hex-grid | 時間停止, 力場, 護盾, 六方格, 狀態跳躍, 像素級靜態, 零延遲 |

**Trigger Examples (copy-pasteable):**
```
H3 T2VA prompt: sniper bottom-left 200m rooftop prone, girl top-right booth facing LEFT, right floor-to-ceiling window, bullet cam from behind → hard cut front view at window impact, time stop at 30cm from left ribcage, force field teal hex-grid, chopstick catch from RIGHT, retract RIGHT, pixel-level static.
```
```
請用 H3 T2VA 產生：狙擊手在民房頂樓左下角 200m 趴伏，女主角在餐廳右上角右側卡座面朝左吃牛肉麵，子彈穿透右側落地窗定格在左側肋骨 30cm，BULLET CAM 跟隨子彈尾部飛行，3.00s 硬切正面視角（站女主角左側向右看），時間停止 ZERO-LATENCY STATE JUMP PIXEL-LEVEL STATIC，筷子向左伸出從右側夾住子彈向右收回放桌。
```
```
Generate H3 T2VA sniper bullet-catch diagonal geometry: sniper BL, girl TR facing left, right window, bullet trajectory BL→right window→girl left ribcage 30cm, bullet cam matching velocity 280k RPM spin conical shockwave neon streaks, hard cut front view at 3.00s, force field silent implosion, chopstick biomechanics pronated 45°→supinated 90°.
```

---

## 核心空間幾何（不可變）

```
┌─────────────────────────────────────────────────────────────┐
│  SNIPER (BL)                            GIRL (TR)          │
│  ●──────────────────►│ WINDOW │◄──────────────────●          │
│  200m rooftop        RIGHT SIDE    booth, facing LEFT      │
│  prone, rear view    floor-to-ceiling  left profile        │
│                                          30cm stop         │
└─────────────────────────────────────────────────────────────┘
```

| 元素 | 位置/朝向 | 備註 |
|------|-----------|------|
| **狙擊手** | 畫面**左下角**，民房頂樓平台，200m，趴伏 | 僅出現在 Shot 1–2 |
| **女主角** | 餐廳**右側**卡座，**面朝左**（左側面對鏡頭），畫面**右上角** | SINGLE PROTAGONIST |
| **落地窗** | 餐廳**右側**全景落地窗，面向街道/狙擊手 | 子彈穿透點 |
| **子彈軌跡** | 狙擊手(左下) → 穿透右側窗 → 女主角**左側肋骨** 30cm | 直線，左下→右上穿窗→續向左 |
| **BULLET CAM** | 1.70–3.00s，鎖定子彈尾部，**從後方跟隨**飛行 | 子彈從左下飛向右上 |
| **3.00s 切正面視角** | 站在女主角**左側**（她面朝方向），**向右看**向右側窗 | 窗在右、女主角在左、子彈從右飛向左 |
| **玻璃碎片** | 向鏡頭(左側)炸裂 | 子彈從右向左，碎片同向 |
| **筷子動作** | 向**左**伸出 → 從**右側**夾住 → 向**右**收回放桌 | 右手，前臂旋前 45°→旋後 90° |
| **結尾鏡頭移動** | **向右**移 1m（展示右側窗蛛網、左側臉） | |

---

## 鏡頭序列（固定時間軸）

| 時間 | 鏡頭 | 關鍵指令 |
|------|------|----------|
| 0.00–0.80s | **REAR VIEW SNIPER** | 畫面左下，肩後視角，餐廳右側窗可見女主角左側面 |
| 0.80–1.50s | **SNIPER SCOPE POV** | 環狀暗角，準星鎖定女主角左側心臟（透過右側窗），SAME character |
| 1.50–1.70s | **TRIGGER → BULLET EXIT** | 擊針、抑制器、銅被甲 7.62mm、280k RPM 自旋，無縫切 BULLET CAM |
| 1.70–3.00s | **BULLET CAM** | 鎖定子彈尾部，匹配速度，可見圓錐震波/折射扭曲、霓虹色條、多普勒 3k→800Hz 下掃 |
| 3.00s | **HARD CUT → FRONT VIEW** | 站女主角左側向右看，子彈撞右側窗、碎片向鏡頭飛、子彈續向左 30cm 定格 |
| 3.00–3.30s | **FORCE FIELD + TIME STOP** | 隱形穹頂、青綠六方格閃爍、**ZERO-LATENCY STATE JUMP**、**PIXEL-LEVEL STATIC** |
| 3.30–4.00s | **HEAD TILT + CHOPSTICK EXTEND LEFT** | 頭部剛體下傾 10°，右手筷子向左伸，精準夾取 2mm gap |
| 4.00–4.50s | **CLAMP** | 從右側接觸子彈中段，皮膚發白，力場六方格凍結在筷子上 |
| 4.50–5.00s | **RETRACT RIGHT + RELEASE** | 前臂旋後 90° 掌心朝上，零相對運動收回，釋放微晃定尖朝下 |
| 5.00–5.50s | **RESET** | 筷子歸碗，頭部復位面朝左，注視窗戶破口 |
| 5.50s | **STATE JUMP REVERSE** | 時間恢復，力場六方格靜默內爆，玻璃碎片完成外爆，8kHz+40Hz 超音速裂響 |
| 5.50–6.50s | **RESUME SEQUENCE** | 雨/蒸汽/霓虹/髮絲/高湯恢復，拉焦回女主角臉部 |
| 6.50–8.50s | **EATING** | 撈麵吸溜 2s，咀嚼擦嘴 2s |
| 8.50–10.00s | **DOLLY RIGHT 1m** | 視差展示子彈、左側臉、右側窗蛛網、霓虹城市景觀 |
| 10.00–15.00s | **HOLD** | 繼續進食，環境光變化，物理不受限 |

---

## 關鍵語法模板（直接嵌入提示詞）

### SINGLE PROTAGONIST 宣告
```
SINGLE PROTAGONIST (Protagonist 2): Chinese schoolgirl, bob-cut black hair, white lobster hairclip right temple, tight white U-neck crop tee over G-cup no bra, nipples faintly visible, cleavage exposed, navel bare, denim mini skirt, bare thighs, no underwear.
```

### 雙視角同一實體標示
```
Protagonist 2 faces LEFT toward interior — SAME character as main shot, viewed optically.
```

### BULLET CAM 物理參數
```
BULLET CAM: bullet spins, copper jacket catching neon — teal/magenta streaks. Air displacement vortex visible: conical shockwave ripples outward, refractive index distortion. Parallax: city lights streak radially, buildings rush backward. Lens breathing on velocity. Trajectory: straight line from Protagonist 1 (left rooftop) → restaurant RIGHT SIDE FLOOR-TO-CEILING WINDOW → Protagonist 2's left ribcage. Bullet flight 1.3s.
```

### ZERO-LATENCY STATE JUMP / PIXEL-LEVEL STATIC
```
OVERWHELMING FORCE FIELD ACTIVATES — invisible dome pulses once, teal hex-grid shimmer. ZERO-LATENCY STATE JUMP: entire scene PIXEL-LEVEL STATIC. Rain suspended. Steam motionless. Hair locked. Neon flicker halted. Noodle broth surface glass-flat. Bullet hangs 30cm from left heart center, tip deformed, rotation frozen, dominate frame. Focus on bullet tip, Protagonist 2's pupil reflection in copper visible.
```

### 筷子生物力學
```
Chopsticks: index braced lower, middle levered upper, thumb pivot. Precision grip. Forearm pronated 45°, wrist neutral. Tips align on bullet axis, 2mm gap. Extension 0.7s.
CLAMP — tips contact bullet mid-body FROM RIGHT, friction grip on copper. Fingers: index extended lower, middle curled upper, thumb presses junction. Skin blanching. Bullet PIXEL-LEVEL STATIC. Force field hex-grid frozen on chopsticks. Neon on copper frozen.
RETRACT — forearm supinates 90°, palm up over table beside bowl. Retraction 0.5s. Zero relative motion.
RELEASE — chopstick tips separate, bullet released onto table. Micro-wobble: settles tip-down, rotation arrests in 2 frames.
```

### 分區 RT60 空間音訊
```
Spatial: rooftop open (3.2s RT60), scope dead (0.1s), bullet flight wide (2.5s), interior narrow (0.8s RT60). Protagonist 2 center, impacts center-left, ambience wide, force field center-hard.
```

---

## 使用方式

```python
# 在 creative/h3-prompt-writing 的 integrated_multimodal_description 中引用：
# 1. 複製上述空間幾何表作為設定基準
# 2. 依鏡頭序列表填入時間戳動作
# 3. 嵌入關鍵語法模板對應段落
# 4. 確保 overall_soundscape 使用分區 RT60 設計
# 5. non_diegetic_music: N/A
```

## 禁止事項
- ❌ 狙擊手/窗/女主角相對位置任意更動
- ❌ BULLET CAM 與正面視角方向邏輯衝突
- ❌ 子彈飛行/碎片/筷子動作方向不一致
- ❌ 缺少 SINGLE PROTAGONIST 宣告（導致雙女主角）
- ❌ 使用慢動作、切鏡頭、背景音樂
- ❌ 第一段結尾錨定幀

## 版本歷史
- v1.0.0 (2026-10-11): 從 v20 提示詞提煉，確立對角線幾何、BULLET CAM→FRONT VIEW 切換、完整生物力學、時間停止語法