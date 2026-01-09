# Audio Convention

> [!info] Audio Asset Management Document
>
> Add any information here about audio naming conventions, compression formats, and audio asset organization.

---

## 📝 Naming Conventions

```text
AUD_[[TYPE]]_[[NAME]]_[[FURTHER-DESCRIPTION]]
```

### Examples:

- **Music:** `AUD_MUS_Theme_MainMenu`
- **SFX:** `AUD_SFX_Button_Click`
- **Voice:** `AUD_VOX_Dialogue_001`
- **Ambience:** `AUD_AMB_Forest_Day`
- ...

---

## 🎵 Audio Import Settings

### Base Settings:

- **Load Type:** Compressed In Memory (default)
- **Compression Format:** Vorbis
- **Quality:** 70% (adjust per audio type)
- **Sample Rate Setting:** Preserve Sample Rate
- **Sample Rate Override:** 44100 Hz (or project standard)

### 3D Sound Settings:

- **Spatial Blend:** 3D (for world audio)
- **Spatial Blend:** 2D (for UI, music)
- **Doppler Level:** 1.0 (for moving sources)
- **Spread:** 0 (for directional audio)
- **Min Distance:** 1.0 (adjust per sound)
- **Max Distance:** 500 (adjust per sound)

### 2D Sound Settings:

- **Spatial Blend:** 2D
- Use for: UI sounds, music, narration

---

## 🗜️ Compression Formats

### Platform-Specific Compression:

| Platform | Format | Quality | Notes |
| :------- | :----- | :------ | :---- |
| **Android** | Vorbis | 70% | Good balance |
| **iOS** | MP3 | 70% | iOS optimized |
| **PC** | PCM | 100% | Uncompressed |
| **WebGL** | Vorbis | 50% | Size critical |

### Compression Guidelines:

- **Music:** 70-80% quality
- **SFX:** 60-70% quality
- **Voice:** 80-90% quality
- **Ambience:** 50-60% quality

---

## 🔊 Audio Mixer Organization

### Mixer Structure:

```
Master Mixer
├── Music Group
├── SFX Group
│   ├── UI SFX
│   ├── Gameplay SFX
│   └── Ambient SFX
└── Voice Group
```

### Mixer Settings:

- Document mixer group levels
- Note any effects applied to groups
- Document ducking/sidechain settings

---

## 📊 Audio Relation Table

| Audio Name | Type | Length | Format | Used In | Notes |
| :--------- | :--- | :----- | :----- | :------ | :---- |
| `AUD_MUS_Theme_MainMenu` | Music | 2:30 | Vorbis | MainMenu | Looping background music |
| `AUD_SFX_Button_Click` | SFX | 0:05 | Vorbis | UI | Button interaction sound |
| ... | ... | ... | ... | ... | ... |

---

## 🎚️ Audio Settings Per Type

### Music:

- **Load Type:** Streaming
- **Compression Format:** Vorbis
- **Quality:** 70%
- **Spatial Blend:** 2D
- **Loop:** `TRUE`

### Sound Effects:

- **Load Type:** Compressed In Memory
- **Compression Format:** Vorbis
- **Quality:** 60-70%
- **Spatial Blend:** 3D or 2D (per sound)
- **Loop:** `FALSE` (unless specified)

### Voice/Dialogue:

- **Load Type:** Compressed In Memory
- **Compression Format:** Vorbis
- **Quality:** 80-90%
- **Spatial Blend:** 2D or 3D (per context)
- **Loop:** `FALSE`

### Ambience:

- **Load Type:** Streaming
- **Compression Format:** Vorbis
- **Quality:** 50-60%
- **Spatial Blend:** 3D
- **Loop:** `TRUE`
