# Material Convention

> [!info] Material and Shader Information Document
>
> Add any information here about material naming conventions, shader selection guidelines, and material organization standards.

---

## 📝 Naming Conventions

```text
MAT_[[TYPE]]_[[NAME]]_[[FURTHER-DESCRIPTION]]
```

### Examples:

- **UI Materials:** `MAT_UI_Button_Default`
- **Environment Materials:** `MAT_Env_Stone_Rough`
- **Character Materials:** `MAT_Char_Skin_Base`
- **Effect Materials:** `MAT_FX_Glow_Pulse`
- ...

---

## 🎨 Shader Selection Guidelines

### Standard Shaders:

| Use Case | Recommended Shader | Notes |
| :------- | :----------------- | :---- |
| **Opaque Objects** | Standard (Metallic) / URP Lit | For most 3D objects |
| **Transparent Objects** | Standard (Transparent) / URP Lit (Transparent) | UI, effects, glass |
| **Unlit Objects** | Unlit / URP Unlit | Performance-critical, always visible |
| **UI Elements** | UI/Default | For Canvas elements |
| **Sprites** | Sprites/Default | For 2D sprite rendering |
| **Particles** | Particles/Standard Surface | For particle systems |

### Custom Shaders:

- Document custom shader usage and justification
- Include shader variant management notes
- Document any shader-specific material properties

---

## ⚙️ Material Property Standards

### Base Properties:

- **Albedo/Base Map:** Primary color texture
- **Metallic:** Use texture or slider (0.0 - 1.0)
- **Smoothness:** Use texture or slider (0.0 - 1.0)
- **Normal Map:** Standard normal map format
- **Emission:** Only when needed for performance

### Texture Assignment:

- Always use texture maps when available
- Use tiling/offset for repeating patterns
- Document any special UV mapping requirements

---

## 📦 Material Organization

### Folder Structure:

```
Materials/
├── UI/
├── Environment/
├── Characters/
├── Effects/
└── Shared/
```

### Material Variants:

- Use Material Variants for similar materials
- Document variant relationships
- Keep base materials in `Shared/` folder

---

## 🔧 Shader Variant Management

### Guidelines:

- Limit shader keywords to reduce variant count
- Document shader stripping settings
- Monitor build size impact
- Use Shader Variant Collection for critical shaders

---

## 📊 Material Relation Table

| Material Name | Shader | Used In | Notes |
| :------------ | :----- | :------ | :---- |
| `MAT_UI_Button_Default` | UI/Default | MainMenu, Settings | Base button material |
| ... | ... | ... | ... |
