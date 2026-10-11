# H3 狙擊子彈接住 - 對角線幾何技能

> **適用場景**：MiniMax H3 T2VA 文字生成視頻，狙擊手從左下角開槍，子彈穿透右側落地窗，在女主角左側肋骨 30cm 處被力場定格，女主角用筷子從右側夾住子彈放回桌上。

---

## 核心特色

| 特性 | 說明 |
|------|------|
| **空間幾何** | 不可變的對角線佈局：狙擊手(左下) → 右側落地窗 → 女主角(右上，面朝左) |
| **鏡頭序列** | 固定 15 秒時間軸：後視角狙擊手 → 狙擊鏡 POV → BULLET CAM → 硬切正面視角 → 時間停止 → 筷子接住 → 恢復進食 |
| **物理參數** | 7.62mm 銅被甲彈、280k RPM 自旋、圓錐震波、折射扭曲、霓虹色條、多普勒 3k→800Hz |
| **時間停止** | ZERO-LATENCY STATE JUMP + PIXEL-LEVEL STATIC（像素級靜態，零殘留動態） |
| **力場視覺** | 隱形穹頂、青綠六方格閃爍、筷子接觸時凍結在筷尖、恢復時靜默內爆 |
| **生物力學** | 前臂旋前 45° → 筷尖 2mm 縫隙夾取 → 旋後 90° 掌心朝上收回、零相對運動 |
| **空間音訊** | 分區 RT60：屋頂 3.2s、鏡內 0.1s、飛行 2.5s、室內 0.8s、力場中心硬反射 |

---

## 快速開始

### 1. 載入技能
```python
# 在 creative/h3-prompt-writing 的 integrated_multimodal_description 中引用
from skills.creative.h3_bullet_catch_diagonal_geometry import SPATIAL_GEOMETRY, CAMERA_SEQUENCE, SYNTAX_TEMPLATES
```

### 2. 複製觸發範例（直接貼上即可生成）

**英文版：**
```
H3 T2VA prompt: sniper bottom-left 200m rooftop prone, girl top-right booth facing LEFT, right floor-to-ceiling window, bullet cam from behind → hard cut front view at window impact, time stop at 30cm from left ribcage, force field teal hex-grid, chopstick catch from RIGHT, retract RIGHT, pixel-level static.
```

**繁體中文版：**
```
請用 H3 T2VA 產生：狙擊手在民房頂樓左下角 200m 趴伏，女主角在餐廳右上角右側卡座面朝左吃牛肉麵，子彈穿透右側落地窗定格在左側肋骨 30cm，BULLET CAM 跟隨子彈尾部飛行，3.00s 硬切正面視角（站女主角左側向右看），時間停止 ZERO-LATENCY STATE JUMP PIXEL-LEVEL STATIC，筷子向左伸出從右側夾住子彈向右收回放桌。
```

**技術縮寫版：**
```
Generate H3 T2VA sniper bullet-catch diagonal geometry: sniper BL, girl TR facing left, right window, bullet trajectory BL→right window→girl left ribcage 30cm, bullet cam matching velocity 280k RPM spin conical shockwave neon streaks, hard cut front view at 3.00s, force field silent implosion, chopstick biomechanics pronated 45°→supinated 90°.
```

---

## 空間幾何速查表

```
┌─────────────────────────────────────────────────────────────┐
│  SNIPER (BL)                            GIRL (TR)          │
│  ●──────────────────►│ WINDOW │◄──────────────────●          │
│  200m rooftop        RIGHT SIDE    booth, facing LEFT      │
│  prone, rear view    floor-to-ceiling  left profile        │
│                                          30cm stop         │
└─────────────────────────────────────────────────────────────┘
```

| 元素 | 位置/朝向 | 關鍵點 |
|------|-----------|--------|
| **狙擊手** | 畫面左下角，民房頂樓平台，200m，趴伏 | 僅出現 0.00–1.50s |
| **女主角** | 餐廳右側卡座，面朝左（左側面對鏡頭），畫面右上角 | **SINGLE PROTAGONIST** |
| **落地窗** | 餐廳右側全景落地窗，面向街道/狙擊手 | 子彈穿透點 |
| **子彈軌跡** | 左下 → 穿透右側窗 → 女主角左側肋骨 30cm | 直線，續向左 |
| **BULLET CAM** | 1.70–3.00s，鎖定子彈尾部，從後方跟隨 | 子彈從左下飛向右上 |
| **3.00s 切正面** | 站女主角左側向右看（窗在右、女主角在左） | 子彈從右飛向左 |
| **玻璃碎片** | 向鏡頭(左側)炸裂 | 同向左飛 |
| **筷子動作** | 向左伸出 → 從右側夾住 → 向右收回放桌 | 右手，旋前→旋後 |
| **結尾移動** | 向右移 1m | 展示右側窗蛛網、左側臉 |

---

## 鏡頭時間軸（15 秒）

| 時間 | 鏡頭 | 關鍵指令 |
|------|------|----------|
| 0.00–0.80s | **REAR VIEW SNIPER** | 肩後視角，可見右側窗與女主角左側面 |
| 0.80–1.50s | **SNIPER SCOPE POV** | 環狀暗角，準星鎖定左側心臟，SAME character |
| 1.50–1.70s | **TRIGGER → BULLET EXIT** | 擊針、抑制器、280k RPM，無縫切 BULLET CAM |
| 1.70–3.00s | **BULLET CAM** | 匹配速度，圓錐震波、折射扭曲、霓虹色條、多普勒下掃 |
| 3.00s | **HARD CUT → FRONT VIEW** | 子彈撞右窗、碎片向鏡頭、續向左 30cm 定格 |
| 3.00–3.30s | **FORCE FIELD + TIME STOP** | 隱形穹頂、青綠六方格、STATE JUMP、PIXEL-LEVEL STATIC |
| 3.30–4.00s | **HEAD TILT + CHOPSTICK EXTEND LEFT** | 頭下傾 10°，右手筷子向左伸，2mm gap |
| 4.00–4.50s | **CLAMP** | 從右側接觸子彈中段，皮膚發白，六方格凍結在筷子 |
| 4.50–5.00s | **RETRACT RIGHT + RELEASE** | 前臂旋後 90°，掌心朝上，零相對運動，微晃定尖朝下 |
| 5.00–5.50s | **RESET** | 筷子歸碗，頭部復位面朝左，注視窗戶破口 |
| 5.50s | **STATE JUMP REVERSE** | 時間恢復，力場內爆、碎片外爆、8kHz+40Hz 裂響 |
| 5.50–6.50s | **RESUME SEQUENCE** | 雨/蒸汽/霓虹/髮絲/高湯恢復，拉焦回臉部 |
| 6.50–8.50s | **EATING** | 撈麵吸溜 2s，咀嚼擦嘴 2s |
| 8.50–10.00s | **DOLLY RIGHT 1m** | 視差展示子彈、左側臉、右側窗蛛網、霓虹城市 |
| 10.00–15.00s | **HOLD** | 繼續進食，環境光變化，物理不受限 |

---

## 關鍵語法模板（直接嵌入提示詞）

### SINGLE PROTAGONIST 宣告（防雙女主角）
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

## 使用方式（配合 creative/h3-prompt-writing）

```python
# 1. 複製空間幾何表作為設定基準
# 2. 依鏡頭序列表填入時間戳動作
# 3. 嵌入關鍵語法模板對應段落
# 4. 確保 overall_soundscape 使用分區 RT60 設計
# 5. non_diegetic_music: N/A
```

### 整合範例
```python
integrated_multimodal_description = f"""
{SPATIAL_GEOMETRY}

{CAMERA_SEQUENCE}

{SYNTAX_TEMPLATES['SINGLE_PROTAGONIST']}
{SYNTAX_TEMPLATES['BULLET_CAM']}
{SYNTAX_TEMPLATES['TIME_STOP']}
{SYNTAX_TEMPLATES['CHOPSTICKS']}
"""

overall_soundscape = SYNTAX_TEMPLATES['SPATIAL_AUDIO']
non_diegetic_music = "N/A"
```

---

## 禁止事項 ❌

| 禁止項目 | 原因 |
|----------|------|
| 任意更動狙擊手/窗/女主角相對位置 | 破壞對角線幾何不變量 |
| BULLET CAM 與正面視角方向邏輯衝突 | 導致子彈飛行方向矛盾 |
| 子彈飛行/碎片/筷子動作方向不一致 | 空間邏輯斷裂 |
| 缺少 SINGLE PROTAGONIST 宣告 | H3 會生成雙女主角 |
| 使用慢動作、切鏡頭、背景音樂 | 違反單一長鏡頭、純非配樂要求 |
| 第一段結尾錨定幀 | 破壞物理不受限的語意 |

---

## 參考實例

- `references/example_prompt_v20.txt` — v20 完整提示詞實例（6,784 字符，< 7,000 限制），含 `integrated_multimodal_description`、`overall_soundscape`、`non_diegetic_music` 三段式結構，可直接作為模板基準。

---

## 版本歷史

| 版本 | 日期 | 變更內容 |
|------|------|----------|
| v1.0.0 | 2026-10-11 | 從 v20 提示詞提煉，確立對角線幾何、BULLET CAM→FRONT VIEW 切換、完整生物力學、時間停止語法 |

---

## 相關技能

- `creative/h3-prompt-writing` — H3 提示詞寫作基礎架構
- `creative/h3-time-stop-engineering` — 時間停止工程細節
- `creative/h3-spatial-action-sync` — 高複雜度動作空間同步

---

## 檔案結構

```
h3-bullet-catch-diagonal-geometry/
├── SKILL.md          # 技能定義與完整規範
├── assets/
│   └── README.md     # 本文件（中文說明）
└── references/
    └── example_prompt_v20.txt  # v20 完整提示詞實例
```

---

> **提示**：此技能從實戰驗證的 v20 提示詞（6,784 字符，< 7,000 限制）提煉而來，空間邏輯經過 20 版迭代驗證，可直接用於生產級 H3 T2VA 生成。