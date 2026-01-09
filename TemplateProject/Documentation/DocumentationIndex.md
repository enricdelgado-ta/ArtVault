# Documentation Index

> [!info] Master Documentation Hub
>
> This document serves as the central index for all asset management and Unity project documentation.

---

## 📚 Documentation Overview

This vault contains comprehensive documentation for managing Unity project assets. Each document covers specific aspects of asset management, import settings, and project organization.

The documentation is organized into two main categories:
- **Asset Conventions** - Naming conventions and import settings for different asset types
- **Project Setup** - Project structure, platform settings, and pipeline configuration

---

## 📁 Template Project Structure

### Art Assets Organization

```
Art/
├── Fonts/                    # Font assets
├── Materials/                # Material assets
│   ├── Characters/
│   ├── Environment/
│   ├── Shared/
│   └── UI/
├── Meshes/                   # Mesh assets
├── Models/                   # 3D model assets
│   ├── Characters/
│   ├── Environment/
│   ├── Props/
│   └── Vehicles/
├── Sprites/                  # 2D sprite assets
│   ├── Characters/
│   ├── Effects/
│   └── UI/
└── Textures/                 # Texture assets
    ├── Characters/
    ├── Debug/
    │   └── ColorPixels/
    ├── Effects/
    ├── Environment/
    └── UI/
        └── Icons/
```

### Documentation Organization

```
Documentation/
├── Asset Conventions/        # Asset type conventions
│   ├── AnimationConvention.md
│   ├── AssetConvention.md
│   ├── AudioConvention.md
│   ├── MaterialConvention.md
│   └── ModelConvention.md
├── Project Setup/            # Project configuration
│   ├── ImportPipeline.md
│   ├── PlatformSettings.md
│   ├── PrefabOrganization.md
│   ├── UnityFolderStructure.md
│   └── UnityProjectSettings.md
├── AssetRelation.md          # Asset registry
└── DocumentationIndex.md     # This file
```

---

## 📋 Available Documentation

### Asset Conventions

These documents define naming conventions and import settings for different asset types.

#### [Asset Convention](Asset%20Conventions/AssetConvention.md)
- Texture naming conventions
- Texture compression settings
- Texture import presets
- Platform-specific texture settings

#### [Material Convention](Asset%20Conventions/MaterialConvention.md)
- Material naming conventions
- Shader selection guidelines
- Material property standards
- Shader variant management

#### [Model Convention](Asset%20Conventions/ModelConvention.md)
- 3D model naming conventions
- Model import settings
- Animation import settings
- LOD (Level of Detail) configuration
- Mesh compression settings

#### [Audio Convention](Asset%20Conventions/AudioConvention.md)
- Audio naming conventions
- Compression formats per platform
- 3D vs 2D audio settings
- Audio mixer organization

#### [Animation Convention](Asset%20Conventions/AnimationConvention.md)
- Animation naming conventions
- Import settings for different rig types
- Compression settings
- Animation event standards

---

### Project Setup

These documents cover project structure, organization, and configuration.

#### [Unity Folder Structure](Project%20Setup/UnityFolderStructure.md)
- Recommended project folder organization
- Asset type organization
- Naming conventions for folders
- Organization principles

#### [Prefab Organization](Project%20Setup/PrefabOrganization.md)
- Prefab naming conventions
- Folder organization structure
- Prefab variant management
- Prefab dependency tracking

#### [Platform Settings](Project%20Setup/PlatformSettings.md)
- Platform-specific compression formats
- Quality settings per platform
- Build size targets
- Platform optimization guidelines

#### [Import Pipeline](Project%20Setup/ImportPipeline.md)
- Custom import rules
- Automation scripts
- Batch processing procedures
- Asset dependency management

#### [Unity Project Settings](Project%20Setup/UnityProjectSettings.md)
- Quality settings configuration
- Graphics API settings
- Player settings documentation
- Build settings and scene order

---

### Core Asset Documentation

#### [Asset Relation Table](AssetRelation.md)
- Central registry of all textures
- Quick reference for asset lookup
- Asset usage tracking

---

## 🔍 Quick Reference

### Finding Information

| What You Need | Document | Location |
| :------------ | :------- | :-------- |
| **Texture settings** | [Asset Convention](Asset%20Conventions/AssetConvention.md) | Asset Conventions |
| **Material setup** | [Material Convention](Asset%20Conventions/MaterialConvention.md) | Asset Conventions |
| **3D model import** | [Model Convention](Asset%20Conventions/ModelConvention.md) | Asset Conventions |
| **Audio compression** | [Audio Convention](Asset%20Conventions/AudioConvention.md) | Asset Conventions |
| **Animation setup** | [Animation Convention](Asset%20Conventions/AnimationConvention.md) | Asset Conventions |
| **Prefab organization** | [Prefab Organization](Project%20Setup/PrefabOrganization.md) | Project Setup |
| **Folder structure** | [Unity Folder Structure](Project%20Setup/UnityFolderStructure.md) | Project Setup |
| **Platform settings** | [Platform Settings](Project%20Setup/PlatformSettings.md) | Project Setup |
| **Import automation** | [Import Pipeline](Project%20Setup/ImportPipeline.md) | Project Setup |
| **Project configuration** | [Unity Project Settings](Project%20Setup/UnityProjectSettings.md) | Project Setup |
| **Asset lookup** | [Asset Relation Table](AssetRelation.md) | Root |

---

## 📊 Documentation Status

| Document | Status | Location |
| :------- | :----- | :------- |
| Asset Convention | ✅ Template | Asset Conventions |
| Asset Relation Table | ✅ Template | Root |
| Material Convention | ✅ Template | Asset Conventions |
| Model Convention | ✅ Template | Asset Conventions |
| Audio Convention | ✅ Template | Asset Conventions |
| Animation Convention | ✅ Template | Asset Conventions |
| Prefab Organization | ✅ Template | Project Setup |
| Unity Folder Structure | ✅ Template | Project Setup |
| Platform Settings | ✅ Template | Project Setup |
| Import Pipeline | ✅ Template | Project Setup |
| Unity Project Settings | ✅ Template | Project Setup |

---

## 🎯 Getting Started

### For New Team Members:

1. Start with [Unity Folder Structure](Project%20Setup/UnityFolderStructure.md) to understand project organization
2. Review [Asset Convention](Asset%20Conventions/AssetConvention.md) for texture standards
3. Check [Platform Settings](Project%20Setup/PlatformSettings.md) for target platform requirements
4. Reference [Asset Relation Table](AssetRelation.md) to find existing assets

### For Asset Creation:

1. Check relevant asset type convention document in [Asset Conventions](Asset%20Conventions/)
2. Follow naming conventions
3. Apply appropriate import settings
4. Update asset relation tables
5. Document any special cases

### For Project Setup:

1. Review [Unity Project Settings](Project%20Setup/UnityProjectSettings.md)
2. Configure [Platform Settings](Project%20Setup/PlatformSettings.md)
3. Set up [Import Pipeline](Project%20Setup/ImportPipeline.md) if needed
4. Organize folders per [Unity Folder Structure](Project%20Setup/UnityFolderStructure.md)

---

## 📝 Documentation Maintenance

### Updating Documentation:

- Keep documentation current with project changes
- Update relation tables when adding assets
- Document any deviations from standards
- Share updates with team

### Contributing:

- Follow existing documentation style
- Use consistent formatting
- Include examples where helpful
- Keep information accurate and up-to-date

---

## 🔗 Related Resources

### External Resources:

- [Unity Documentation](https://docs.unity3d.com/)
- [Unity Asset Store](https://assetstore.unity.com/)
- [Unity Learn](https://learn.unity.com/)

### Internal Resources:

- Project-specific guidelines
- Team conventions
- Custom tools documentation

---

## ❓ Questions or Updates?

If you need to:
- Add new documentation
- Update existing documentation
- Report missing information
- Suggest improvements

Please contact the project maintainers or update the documentation directly following the established conventions.
