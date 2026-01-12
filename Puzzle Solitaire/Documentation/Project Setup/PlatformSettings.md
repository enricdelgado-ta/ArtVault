# Platform Settings

> [!info] Platform-Specific Asset Settings Document
>
> Add any information here about platform-specific compression formats, quality settings, and build optimizations.

---

## 📱 Android Settings

### Texture Compression:

| Texture Type | Format | Quality | Max Size |
| :----------- | :----- | :------ | :------- |
| **UI Textures** | ASTC 4x4 | Best | 2048 |
| **Character Textures** | ASTC 6x6 | High | 1024 |
| **Environment Textures** | ASTC 8x8 | Medium | 512 |
| **Normal Maps** | ASTC 4x4 | Best | 1024 |
| **Lightmaps** | ASTC 6x6 | High | 2048 |

### Audio Compression:

- **Format:** Vorbis
- **Quality:** 70%
- **Sample Rate:** 44100 Hz

### Model Compression:

- **Mesh Compression:** Medium
- **Animation Compression:** Optimal

---

## 🍎 iOS Settings

### Texture Compression:

| Texture Type | Format | Quality | Max Size |
| :----------- | :----- | :------ | :------- |
| **UI Textures** | ASTC 4x4 | Best | 2048 |
| **Character Textures** | ASTC 6x6 | High | 1024 |
| **Environment Textures** | ASTC 8x8 | Medium | 512 |
| **Normal Maps** | ASTC 4x4 | Best | 1024 |
| **Lightmaps** | ASTC 6x6 | High | 2048 |

### Audio Compression:

- **Format:** MP3
- **Quality:** 70%
- **Sample Rate:** 44100 Hz

### Model Compression:

- **Mesh Compression:** Medium
- **Animation Compression:** Optimal

---

## 💻 PC Settings

### Texture Compression:

| Texture Type | Format | Quality | Max Size |
| :----------- | :----- | :------ | :------- |
| **UI Textures** | DXT5 | Best | 4096 |
| **Character Textures** | DXT5 | Best | 2048 |
| **Environment Textures** | DXT1 | High | 2048 |
| **Normal Maps** | BC5 | Best | 2048 |
| **Lightmaps** | DXT1 | High | 4096 |

### Audio Compression:

- **Format:** PCM (Uncompressed)
- **Quality:** 100%
- **Sample Rate:** 44100 Hz

### Model Compression:

- **Mesh Compression:** Low
- **Animation Compression:** Keyframe Reduction

---

## 🌐 WebGL Settings

### Texture Compression:

| Texture Type | Format | Quality | Max Size |
| :----------- | :----- | :------ | :------- |
| **UI Textures** | DXT5 | Medium | 1024 |
| **Character Textures** | DXT5 | Medium | 512 |
| **Environment Textures** | DXT1 | Low | 512 |
| **Normal Maps** | DXT5 | Medium | 512 |
| **Lightmaps** | DXT1 | Low | 1024 |

### Audio Compression:

- **Format:** Vorbis
- **Quality:** 50%
- **Sample Rate:** 22050 Hz

### Model Compression:

- **Mesh Compression:** High
- **Animation Compression:** Dense

---

## 🎮 Console Settings

### PlayStation/Xbox:

| Texture Type | Format | Quality | Max Size |
| :----------- | :----- | :------ | :------- |
| **UI Textures** | BC7 | Best | 4096 |
| **Character Textures** | BC7 | Best | 2048 |
| **Environment Textures** | BC1 | High | 2048 |
| **Normal Maps** | BC5 | Best | 2048 |
| **Lightmaps** | BC1 | High | 4096 |

### Audio Compression:

- **Format:** PCM or Vorbis
- **Quality:** 80-90%
- **Sample Rate:** 48000 Hz

### Model Compression:

- **Mesh Compression:** Low
- **Animation Compression:** Optimal

---

## 📊 Platform Comparison Table

| Platform | Texture Format | Audio Format | Mesh Compression | Build Size Target |
| :------- | :------------- | :----------- | :--------------- | :---------------- |
| **Android** | ASTC | Vorbis | Medium | < 100 MB |
| **iOS** | ASTC | MP3 | Medium | < 100 MB |
| **PC** | DXT/BC | PCM | Low | < 500 MB |
| **WebGL** | DXT | Vorbis | High | < 50 MB |
| **Console** | BC | PCM/Vorbis | Low | < 10 GB |

---

## ⚙️ Quality Settings Per Platform

### Android Quality Levels:

- **Low:** ASTC 8x8, Vorbis 50%, Mesh High
- **Medium:** ASTC 6x6, Vorbis 70%, Mesh Medium
- **High:** ASTC 4x4, Vorbis 80%, Mesh Low

### iOS Quality Levels:

- **Low:** ASTC 8x8, MP3 50%, Mesh High
- **Medium:** ASTC 6x6, MP3 70%, Mesh Medium
- **High:** ASTC 4x4, MP3 80%, Mesh Low

### PC Quality Levels:

- **Low:** DXT1, Vorbis 60%, Mesh Medium
- **Medium:** DXT5, PCM 100%, Mesh Low
- **High:** BC7, PCM 100%, Mesh Off

---

## 🔧 Build Settings

### Android Build Settings:

- **Minimum API Level:** 21 (Android 5.0)
- **Target API Level:** Latest
- **Scripting Backend:** IL2CPP
- **Architecture:** ARM64

### iOS Build Settings:

- **Minimum iOS Version:** 12.0
- **Target Device Family:** iPhone + iPad
- **Scripting Backend:** IL2CPP
- **Architecture:** ARM64

### PC Build Settings:

- **Architecture:** x64
- **Scripting Backend:** Mono or IL2CPP
- **Graphics API:** DirectX 11/12, Vulkan

---

## 📝 Platform-Specific Notes

### Android:

- Use ASTC for all texture types
- Consider ETC2 as fallback for older devices
- Monitor build size for Play Store limits
- Test on various device specifications

### iOS:

- ASTC is standard for all iOS devices
- Optimize for Metal graphics API
- Consider App Store size limits
- Test on different iOS versions

### PC:

- Support multiple graphics APIs
- Provide quality settings in-game
- Consider different hardware specs
- Optimize for both low and high-end PCs

### WebGL:

- Size is critical (download time)
- Use aggressive compression
- Minimize texture sizes
- Test in multiple browsers
