# Animation Convention

> [!info] Animation Asset Settings Document
>
> Add any information here about animation naming conventions, import settings, and animation asset management.

---

## 📝 Naming Conventions

```text
ANIM_[[TYPE]]_[[NAME]]_[[FURTHER-DESCRIPTION]]
```

### Examples:

- **Character Animations:** `ANIM_Char_Hero_Idle`
- **UI Animations:** `ANIM_UI_Panel_FadeIn`
- **Effect Animations:** `ANIM_FX_Explosion_Sequence`
- **Prop Animations:** `ANIM_Prop_Door_Open`
- ...

---

## 🎬 Animation Import Settings

### Base Settings:

- **Import Animation:** `TRUE`
- **Bake Animations:** `TRUE`
- **Resample Curves:** `TRUE`
- **Anim. Compression:** Optimal
- **Rotation Error:** 0.5
- **Position Error:** 0.5
- **Scale Error:** 0.5

### Clips Settings:

- **Loop Time:** Per animation type
- **Loop Pose:** `TRUE` (for looping animations)
- **Cycle Offset:** 0.0
- **Additive Reference Pose:** None (unless additive)

---

## 🎭 Rig Settings

### Rig Type Selection:

| Rig Type | Use Case | Settings |
| :------- | :------- | :------- |
| **None** | Static meshes | No animation |
| **Generic** | Custom rigs | Generic animation |
| **Humanoid** | Character models | Humanoid retargeting |
| **Legacy** | Older projects | Legacy system |

### Humanoid Settings:

- **Avatar Definition:** Create From This Model
- **Optimize Game Objects:** `TRUE`
- **Root Transform Rotation:** Body Orientation
- **Root Transform Position (Y):** Original
- **Root Transform Position (XZ):** Center of Mass

### Generic Settings:

- **Root Transform Rotation:** None
- **Root Transform Position (Y):** Original
- **Root Transform Position (XZ):** Center of Mass

---

## 🗜️ Animation Compression

### Compression Settings:

| Compression Type | Quality | Use Case |
| :--------------- | :------ | :------- |
| **Off** | Highest | Cinematic animations |
| **Keyframe Reduction** | High | Most animations |
| **Optimal** | Balanced | Default choice |
| **Dense** | Lower | Performance critical |

### Compression Guidelines:

- **Cinematic:** Off or Keyframe Reduction
- **Gameplay:** Optimal
- **Background:** Dense
- **UI Animations:** Optimal

---

## 📊 Animation Clips Organization

### Clip Naming:

- Use descriptive names
- Include character/object name
- Include animation type (Idle, Walk, Attack, etc.)
- Use consistent naming across project

### Clip Settings Per Type:

| Animation Type | Loop Time | Loop Pose | Notes |
| :------------- | :--------- | :--------- | :---- |
| **Idle** | `TRUE` | `TRUE` | Standing idle |
| **Walk/Run** | `TRUE` | `TRUE` | Locomotion |
| **Attack** | `FALSE` | `FALSE` | One-shot action |
| **Death** | `FALSE` | `FALSE` | One-shot action |
| **UI Transitions** | `FALSE` | `FALSE` | UI animations |

---

## 🎯 Animation Events

### Event Naming:

- Use clear, descriptive event names
- Document event timing in frames/seconds
- List parameters passed to events

### Common Events:

- `OnFootstep` - Footstep sound timing
- `OnAttackHit` - Attack damage timing
- `OnAnimationEnd` - Animation completion
- `OnEffectSpawn` - Visual effect timing

---

## 📊 Animation Relation Table

| Animation Name | Type | Length | Rig Type | Used By | Notes |
| :------------- | :--- | :----- | :------- | :------ | :---- |
| `ANIM_Char_Hero_Idle` | Character | 2.0s | Humanoid | Hero Character | Base idle animation |
| `ANIM_Char_Hero_Walk` | Character | 1.0s | Humanoid | Hero Character | Walking cycle |
| ... | ... | ... | ... | ... | ... |

---

## 🔗 Animation Dependencies

### Model Dependencies:

- Document which models use which animations
- Track animation updates affecting models
- Note retargeting compatibility

### Controller Dependencies:

- Document Animator Controller usage
- Track state machine relationships
- Note any animation blending requirements
