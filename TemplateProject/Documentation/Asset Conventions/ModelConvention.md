# Model Convention

> [!info] 3D Model Import Settings Document
>
> Add any information here about model naming conventions, import presets, and 3D asset management standards.

---

## 📝 Naming Conventions

```text
MOD_[[TYPE]]_[[NAME]]_[[FURTHER-DESCRIPTION]]
```

### Examples:

- **Characters:** `MOD_Char_Hero_Main`
- **Environment:** `MOD_Env_Building_Facade`
- **Props:** `MOD_Prop_Chair_Wooden`
- **Vehicles:** `MOD_Vehicle_Car_Sedan`
- ...

---

## 📐 Model Import Settings

### Base Settings:

- **Scale Factor:** 1.0 (adjust per source software)
- **Mesh Compression:** Medium (balance quality/size)
- **Read/Write Enabled:** `FALSE` (enable only when needed)
- **Optimize Mesh:** `TRUE`
- **Generate Colliders:** `FALSE` (use separate collider meshes)
- **Keep Quads:** `FALSE` (unless needed for specific shaders)

### Normals & Tangents:

- **Normals:** Import
- **Tangents:** Calculate
- **Smoothing Angle:** 60 (adjust per model)

### Blend Shapes:

- **Import Blend Shapes:** `TRUE` (if present)
- Document blend shape usage and naming

---

## 🎭 Animation Import Settings

### Model Animation:

- **Import Animation:** `TRUE` (if animated)
- **Bake Animations:** `TRUE`
- **Resample Curves:** `TRUE`
- **Compression:** Optimal

### Rig Settings:

| Rig Type | Settings | Notes |
| :------- | :------- | :---- |
| **None** | None | Static meshes |
| **Generic** | Generic | Custom rigs |
| **Humanoid** | Humanoid | Character models |
| **Legacy** | Legacy | Older animations |

### Humanoid Settings:

- **Avatar Definition:** Create From This Model
- **Optimize Game Objects:** `TRUE`
- Document bone mapping if custom

---

## 📏 LOD (Level of Detail) Settings

### LOD Guidelines:

- **LOD 0:** 100% quality (original mesh)
- **LOD 1:** 50% triangles
- **LOD 2:** 25% triangles
- **LOD 3:** 10% triangles (or billboard)

### LOD Group Settings:

- Document LOD distances per model type
- Use LOD Groups for important models
- Test LOD transitions in-game

---

## 🗜️ Mesh Compression

| Platform | Compression | Quality Impact |
| :------- | :---------- | :------------- |
| **Android** | Medium | Minimal |
| **iOS** | Medium | Minimal |
| **PC/Console** | Low | None |
| **WebGL** | High | Moderate |

---

## 📊 Model Relation Table

| Model Name | Type | Poly Count | LODs | Used In | Notes |
| :--------- | :--- | :--------- | :--- | :------ | :---- |
| `MOD_Char_Hero_Main` | Character | 8,500 | 3 | Gameplay | Main character model |
| ... | ... | ... | ... | ... | ... |

---

## 🔗 Model Dependencies

### Material Assignment:

- Document which materials are used per model
- Note any material variants
- Track material updates that affect models

### Animation Clips:

- List animation clips per model
- Document animation naming conventions
- Track animation dependencies
