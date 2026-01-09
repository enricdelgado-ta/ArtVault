# Unity Project Settings

> [!info] Unity Project Settings Documentation
>
> Add any information here about Unity project settings, quality settings, and build configuration standards.

---

## 🎮 Quality Settings

### Quality Levels:

Document the quality levels configured for the project:

| Quality Level | Texture Quality | Anisotropic Textures | Anti Aliasing | Shadow Quality |
| :------------ | :-------------- | :------------------- | :------------- | :------------- |
| **Very Low**  | Full Res        | Disable              | Disable        | Hard Shadows   |
| **Low**       | Full Res        | Per Texture          | 2x Multi       | Hard Shadows   |
| **Medium**    | Full Res        | Per Texture          | 4x Multi       | Soft Shadows   |
| **High**      | Full Res        | Force Enable         | 4x Multi       | Soft Shadows   |
| **Very High** | Full Res        | Force Enable         | 8x Multi       | Soft Shadows   |

### Platform-Specific Quality:

- **Android:** Low to Medium (default: Medium)
- **iOS:** Medium to High (default: High)
- **PC:** High to Very High (default: Very High)
- **WebGL:** Very Low to Low (default: Low)

---

## 🖼️ Graphics Settings

### Graphics API:

| Platform | Primary API | Fallback API |
| :------- | :----------- | :----------- |
| **Android** | Vulkan | OpenGL ES 3.0 |
| **iOS** | Metal | OpenGL ES 3.0 |
| **PC** | DirectX 11/12 | Vulkan |
| **WebGL** | WebGL 2.0 | WebGL 1.0 |

### Rendering Pipeline:

- **Built-in Render Pipeline**
- **Universal Render Pipeline (URP)**
- **High Definition Render Pipeline (HDRP)**

Document which pipeline is used and why.

---

## 🔊 Audio Settings

### Audio Configuration:

- **DSP Buffer Size:** Good Latency (default)
- **Virtual Voice Count:** 512
- **Real Voice Count:** 32
- **Spatializer Plugin:** (if used)
- **Ambisonic Decoder Plugin:** (if used)

### Audio Mixer:

Document the master audio mixer structure and settings.

---

## 📱 Player Settings

### Company Name:

```
[Your Company Name]
```

### Product Name:

```
[Your Game Name]
```

### Version:

```
[Version Number]
```

### Icon:

- Document icon sizes per platform
- Note icon design guidelines
- Track icon updates

### Splash Screen:

- Document splash screen settings
- Note branding requirements
- Track splash screen assets

---

## 🎯 Platform-Specific Player Settings

### Android:

- **Package Name:** `com.companyname.gamename`
- **Minimum API Level:** 21
- **Target API Level:** Latest
- **Scripting Backend:** IL2CPP
- **Architecture:** ARM64
- **Internet Access:** Require
- **Target Devices:** Phone + Tablet

### iOS:

- **Bundle Identifier:** `com.companyname.gamename`
- **Minimum iOS Version:** 12.0
- **Target Device Family:** iPhone + iPad
- **Scripting Backend:** IL2CPP
- **Architecture:** ARM64
- **Requires ARKit support:** (if applicable)

### PC:

- **Default Screen Width:** 1920
- **Default Screen Height:** 1080
- **Run in Background:** (per project)
- **Capture Single Screen:** (per project)
- **Fullscreen Mode:** Fullscreen Window

---

## 🏗️ Build Settings

### Scenes in Build:

Document the scene order and build configuration:
1. MainMenu
2. Loading
3. Level_01
4. Level_02
5. ...

### Build Configuration:

- **Development Build:** (when to use)
- **Script Debugging:** (when enabled)
- **Deep Profiling Support:** (when enabled)
- **Scripts Only Build:** (for testing)

---

## 📊 Project Settings Summary

### Key Settings to Document:

- ✅ Quality Settings per platform
- ✅ Graphics API configuration
- ✅ Audio settings
- ✅ Player settings (company, product name, version)
- ✅ Build settings and scene order
- ✅ Platform-specific configurations
- ✅ Rendering pipeline selection
- ✅ Scripting backend choices

### Settings to Track Changes:

- Version number updates
- Quality setting adjustments
- Graphics API changes
- Build configuration modifications
- Platform-specific setting updates

---

## 🔄 Settings Maintenance

### Update Workflow:

1. Document current settings
2. Make changes in Unity
3. Test changes thoroughly
4. Update documentation
5. Commit changes to version control
6. Share updates with team

### Version Control:

- Track `ProjectSettings/` folder
- Document settings changes in commits
- Maintain settings documentation
- Review settings periodically

---

## 📝 Settings Documentation Template

### For Each Setting Category:

- **Current Value:** [Value]
- **Justification:** [Why this setting]
- **Platform Variations:** [If different per platform]
- **Last Updated:** [Date]
- **Updated By:** [Person/Team]
- **Notes:** [Additional information]

---

## ⚠️ Important Notes

### Settings to Never Change Without Documentation:

- Graphics API
- Scripting Backend
- Quality Settings (without testing)
- Build Configuration
- Player Settings (company/product name)

### Settings That Require Team Approval:

- Major quality setting changes
- Graphics pipeline changes
- Build configuration modifications
- Platform-specific setting updates
