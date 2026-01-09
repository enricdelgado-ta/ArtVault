# Asset Convention

> [!info] Asset Information Document
>
> Add any information here about naming conventions, texture pressets...

---

## 📝 Naming Conventions

```text
TEX_[[TYPE]]_[[NAME]]_[[FURTHER-DESCRIPTION]]
```

### Examples:

- **UI Icons:** `TEX_UI_Icon_Gear`
- **Icons:** `TEX_Icon_Hand`
- ...

---

## 🗜️ Asset Compression

|                    | Android    | iOS   |
| :----------------- | :--------- | :---- |
| **Compresison Format** | ASTC 12x12 | [...] |
| **Quality**            | Best       | [...] |
| **Max Size**           | 1024       |       |

---

## ⚙️ Texture Presets

> [!tip] Use this to generate a [***Texture Importer***](https://docs.unity3d.com/6000.3/Documentation/ScriptReference/TextureImporter.html) asset
### Base Settings:

- **Texture Type:**
- **Sprite Mode:** Single (unless Multiple needed)
- **Pixels Per Unit:** 100
- **Mesh Type:** Full Rect
- **Extrude Edges:** 1
- **Pivot:** Center
- **Generate Physics Shape:** `FALSE`

### Advanced:

- **sRGB (Color Texture):** `TRUE`
- **Alpha Source:** Input Texture Alpha
- **Alpha Is Transparency:** `TRUE`
- **Read/Write:** `FALSE`
- **Generate Mipmap:** `FALSE`

### Wrap Mode:

- **U axis:** Clamp
- **V axis:** Clamp

### Filter Mode:

- **Filter Mode:** Bilinear