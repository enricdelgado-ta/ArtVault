# Prefab Organization

> [!info] Prefab Structure and Organization Document
>
> Add any information here about prefab naming conventions, folder organization, and prefab relationship management.

---

## 📝 Naming Conventions

```text
PREF_[[TYPE]]_[[NAME]]_[[FURTHER-DESCRIPTION]]
```

### Examples:

- **Characters:** `PREF_Char_Hero_Main`
- **UI Elements:** `PREF_UI_Button_Default`
- **Environment:** `PREF_Env_Building_Facade`
- **Props:** `PREF_Prop_Chair_Wooden`
- **Effects:** `PREF_FX_Explosion_Base`
- ...

---

## 📦 Folder Structure

### Recommended Organization:

```
Prefabs/
├── Characters/
│   ├── Player/
│   ├── NPCs/
│   └── Enemies/
├── UI/
│   ├── Buttons/
│   ├── Panels/
│   └── HUD/
├── Environment/
│   ├── Buildings/
│   ├── Props/
│   └── Terrain/
├── Effects/
│   ├── VFX/
│   └── Particles/
├── Systems/
│   ├── Managers/
│   └── Controllers/
└── Shared/
    └── Common/
```

---

## 🔗 Prefab Variants

### Variant Guidelines:

- Create variants from base prefabs
- Document variant relationships
- Keep base prefabs in `Shared/` folder
- Use descriptive variant names

### Variant Naming:

```text
PREF_[[TYPE]]_[[NAME]]_[[VARIANT]]
```

### Examples:

- Base: `PREF_UI_Button_Default`
- Variants:
  - `PREF_UI_Button_Default_Red`
  - `PREF_UI_Button_Default_Blue`
  - `PREF_UI_Button_Default_Large`

---

## 🏗️ Prefab Structure Standards

### Component Organization:

- Organize components logically
- Use consistent component order
- Document required components
- Note component dependencies

### Hierarchy Standards:

- Use empty GameObjects for organization
- Name all GameObjects clearly
- Avoid deep nesting (max 4-5 levels)
- Use consistent naming for child objects

---

## 📊 Prefab Relation Table

| Prefab Name | Type | Components | Variants | Used In | Notes |
| :---------- | :--- | :---------- | :------- | :------ | :---- |
| `PREF_Char_Hero_Main` | Character | Rigidbody, Animator, Controller | 3 | Gameplay | Main player prefab |
| `PREF_UI_Button_Default` | UI | Button, Image, Text | 5 | All UI | Base button prefab |
| ... | ... | ... | ... | ... | ... |

---

## 🔗 Prefab Dependencies

### Asset Dependencies:

- Document material assignments
- Track model/mesh usage
- Note texture dependencies
- List animation clip usage

### Script Dependencies:

- Document required scripts
- Note script version requirements
- Track custom component usage
- List external package dependencies

---

## 🎯 Prefab Usage Guidelines

### When to Use Prefabs:

- ✅ Reusable game objects
- ✅ Objects instantiated at runtime
- ✅ Objects with complex setups
- ✅ Objects needing variants

### When NOT to Use Prefabs:

- ❌ One-off scene-specific objects
- ❌ Temporary test objects
- ❌ Objects that won't be reused

---

## 🔄 Prefab Workflow

### Creation Workflow:

1. Create GameObject in scene
2. Configure components and hierarchy
3. Test functionality
4. Convert to prefab
5. Move to appropriate folder
6. Document in relation table

### Update Workflow:

1. Open prefab for editing
2. Make changes
3. Test in isolation
4. Apply changes
5. Update documentation
6. Test in scenes using prefab

---

## 📝 Prefab Documentation

### Required Information:

- Prefab purpose and usage
- Component list and settings
- Variant relationships
- Scene usage locations
- Known issues or limitations

### Optional Information:

- Creation date and author
- Last modified date
- Version history
- Performance notes
- Optimization suggestions
