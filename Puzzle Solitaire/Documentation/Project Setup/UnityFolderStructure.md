# Unity Folder Structure

> [!info] Recommended Unity Project Structure
>
> This document outlines the recommended folder structure for Unity projects to maintain organization and asset management efficiency.

---

## 📁 Root Structure

```
Assets/
├── Art/
├── Audio/
├── Prefabs/
├── Scenes/
├── Scripts/
├── Materials/
├── Animations/
├── Resources/
└── StreamingAssets/
```

---

## 🎨 Art Folder Structure

```
Art/
├── Textures/
│   ├── UI/
│   ├── Characters/
│   ├── Environment/
│   ├── Effects/
│   └── Debug/
├── Models/
│   ├── Characters/
│   ├── Environment/
│   ├── Props/
│   └── Vehicles/
├── Materials/
│   ├── UI/
│   ├── Characters/
│   ├── Environment/
│   └── Shared/
└── Sprites/
    ├── UI/
    ├── Characters/
    └── Effects/
```

---

## 🔊 Audio Folder Structure

```
Audio/
├── Music/
│   ├── Themes/
│   └── Ambient/
├── SFX/
│   ├── UI/
│   ├── Gameplay/
│   └── Ambient/
├── Voice/
│   ├── Dialogue/
│   └── Narration/
└── Mixers/
    └── Master/
```

---

## 🏗️ Prefabs Folder Structure

```
Prefabs/
├── Characters/
│   ├── Player/
│   ├── NPCs/
│   └── Enemies/
├── UI/
│   ├── Buttons/
│   ├── Panels/
│   ├── HUD/
│   └── Menus/
├── Environment/
│   ├── Buildings/
│   ├── Props/
│   └── Terrain/
├── Effects/
│   ├── VFX/
│   └── Particles/
└── Systems/
    ├── Managers/
    └── Controllers/
```

---

## 🎬 Scenes Folder Structure

```
Scenes/
├── Main/
│   ├── MainMenu.unity
│   └── Loading.unity
├── Gameplay/
│   ├── Level_01.unity
│   ├── Level_02.unity
│   └── ...
├── UI/
│   └── UI_Scenes/
└── Testing/
    └── Test_Scenes/
```

---

## 💻 Scripts Folder Structure

```
Scripts/
├── Core/
│   ├── Managers/
│   ├── Controllers/
│   └── Systems/
├── Gameplay/
│   ├── Characters/
│   ├── Combat/
│   └── Items/
├── UI/
│   ├── Panels/
│   ├── Buttons/
│   └── HUD/
├── Utilities/
│   ├── Extensions/
│   └── Helpers/
└── Data/
    ├── ScriptableObjects/
    └── DataClasses/
```

---

## 🎭 Animations Folder Structure

```
Animations/
├── Characters/
│   ├── Hero/
│   ├── NPCs/
│   └── Enemies/
├── UI/
│   └── Transitions/
├── Props/
└── Controllers/
    ├── CharacterControllers/
    └── UI_Controllers/
```

---

## 📦 Additional Folders

### Materials (if separate from Art):

```
Materials/
├── UI/
├── Characters/
├── Environment/
└── Shared/
```

### Resources (Runtime Loading):

```
Resources/
├── Prefabs/
├── Data/
└── Configs/
```

### StreamingAssets (Platform-Specific):

```
StreamingAssets/
├── Configs/
└── Data/
```

---

## 🏷️ Naming Conventions

### Folder Naming:

- Use **PascalCase** for folder names
- Be descriptive and specific
- Group related assets together
- Avoid deep nesting (max 4-5 levels)

### Examples:

- ✅ `Characters/Player/`
- ✅ `UI/Buttons/`
- ❌ `characters/player/` (lowercase)
- ❌ `Stuff/` (too vague)

---

## 📋 Organization Principles

### 1. **Type-Based Organization**

Group assets by their type (Textures, Models, Audio, etc.)

### 2. **Context-Based Organization**

Group assets by their usage context (UI, Characters, Environment, etc.)

### 3. **Hybrid Approach** (Recommended)

Combine both: `Art/Textures/UI/` (Type → Context)

### 4. **Shared Assets**

Place commonly used assets in `Shared/` folders

---

## 🔗 Cross-References

### Asset Relationships:

- Document folder relationships
- Note dependencies between folders
- Track asset usage across folders
- Maintain consistency in structure

### Documentation Links:

- Link to asset convention documents
- Reference naming conventions
- Connect to import settings docs

---

## 📊 Folder Usage Guidelines

### When to Create New Folders:

- ✅ More than 10-15 assets in a folder
- ✅ Clear category distinction
- ✅ Team collaboration needs
- ✅ Asset type requires separation

### When to Consolidate:

- ❌ Too many empty folders
- ❌ Only 1-2 assets per folder
- ❌ Unclear categorization
- ❌ Redundant organization levels
