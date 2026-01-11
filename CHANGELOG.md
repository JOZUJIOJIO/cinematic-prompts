# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.0.0] - 2026-01-11

### 🚀 Major Architectural Redesign - Three-Layer Prompt System

### Breaking Changes
- **Complete workflow redesign**: New duration-based scene calculation approach
- **Three-layer prompt architecture**: Scene Prompt → Shot Prompt → Video Prompt
- **Automatic shot selection**: AI-driven shot type selection based on narrative rules

### Added
- **Duration-Driven Workflow**:
  - Input desired video duration (seconds)
  - Automatic calculation: Scene Count = Duration ÷ 5 seconds
  - User confirmation step before generation

- **Three-Layer Prompt System**:
  1. **Scene Prompt (画面提示词)**: JSON-formatted Hollywood-standard scene description
  2. **Shot Prompt (镜头提示词)**: Dynamically generated 7 shot types from scene template
  3. **Video Prompt (视频转换提示词)**: Final prompt with camera movement, transition, BGM

- **7 Shot Type Universal Templates**:
  - EWS (Extreme Long Shot) - 14-24mm, f/8-f/11
  - LS (Long Shot) - 24-35mm, f/5.6-f/8
  - MLS (Medium Long Shot) - 35-50mm, f/4-f/5.6
  - MS (Medium Shot) - 50mm, f/4
  - MCU (Medium Close-Up) - 50-85mm, f/2.8-f/4
  - CU (Close-Up) - 85-100mm, f/1.4-f/2.8
  - ECU (Extreme Close-Up) - 100mm+ Macro, f/2.0-f/2.8

- **12 Camera Movement Library**:
  - Basic: Static, Pan, Tilt, Dolly, Truck, Crane
  - Advanced: Tracking, Orbit, Dolly Zoom, Handheld, Drone, POV Walking
  - Complete speed parameters (0.3x, 0.5x, 1.0x)
  - Emotional context for each movement

- **10 Transition Effects Library**:
  - Basic: Cut, Fade In/Out, Dissolve, Fade to White, Wipe
  - Advanced: Match Cut, Jump Cut, L Cut/J Cut, Defocus, Morph
  - Duration specifications (0.5-2 seconds)
  - Usage context and emotional impact

- **Intelligent Auto-Selection System**:
  - **Rule 1**: Narrative rhythm (opening/development/climax/ending)
  - **Rule 2**: Content matching (environment/action/dialogue/emotion/detail)
  - **Rule 3**: Visual diversity (avoid repetition, push-pull rhythm)
  - **Rule 4**: Emotional intensity matching
  - Outputs detailed selection reasoning

- **BGM Suggestion System**:
  - 10 mood categories with music type matching
  - Reference composers (Hans Zimmer, Vangelis, etc.)
  - Instrument specifications
  - BPM and key recommendations

- **Scene-by-Scene Generation Flow**:
  - For each scene (1 to N):
    - Step 1: Generate Scene Prompt (JSON)
    - Step 2: Generate 7 Shot Prompts (Scene + Template)
    - Step 3: Auto-select best shot type
    - Step 4: Generate Video Prompt (camera/transition/BGM)

### Changed
- **Workflow Philosophy**: Changed from "multi-scene narrative" to "duration-based scene planning"
- **Prompt Hierarchy**: Unified three-layer architecture replaces old dual-mode system
- **Shot Selection**: Now fully automated with transparent reasoning
- **Technical Templates**: Standardized across all 7 shot types with complete specs

### Removed
- Dual-mode system (narrative vs single-scene multi-angle)
- Manual shot selection requirement
- 9-shot grid output (replaced by single shot per scene)
- OTS/POV as separate shot types (integrated into template usage context)

### Technical Specifications
- Scene DNA weight recommendations: 1.3-1.5 for consistency
- Default scene duration: 5 seconds (adjustable)
- Aspect ratio: 2.39:1 (cinematic widescreen)
- Frame rate: 24fps (film standard)
- Complete focal length ranges for each shot type

### Migration Guide
**From v2.x to v3.0**:
- Old workflow: Input script → Generate scenes → Manual shot selection
- New workflow: Input script + duration → Auto-calculate scenes → Auto-select shots
- Backup old scripts before upgrading
- Review new template structure in main.md
- Test with small projects first (30-60 seconds)

## [2.0.0] - 2026-01-10

### 🎉 Major Update - Image-to-Video Workflow Optimization

### Added
- **Separated Prompts**: Distinct image generation and image-to-video prompts
  - `image_prompt`: For generating static frames (Midjourney, DALL-E, SD)
  - `video_prompt`: For adding motion to images (Runway, Pika, SVD)
- **Workflow Examples**: Three detailed examples showing prompt separation
- **Enhanced Documentation**: Comprehensive guides for the two-step workflow
- **Bilingual Output**: Full support for English and Chinese prompts
- **Professional Examples**: Complete romantic sunset scene storyboard

### Changed
- **JSON Structure**: Updated to include both image and video prompt fields
- **SKILL Template**: Enhanced with clear workflow instructions
- **README**: Completely redesigned for GitHub with badges and visual flow

### Technical Details
- Image prompts focus on: composition, lighting, color, details, atmosphere
- Video prompts focus on: camera movement, speed, direction, dynamic elements
- Better compatibility with modern AI generation tools

## [1.0.0] - 2026-01-09

### Added
- Initial release of Cinematic Prompts Generator
- Basic prompt generation with cinematography terminology
- Support for shot types, camera movements, and technical specifications
- JSON and Markdown output formats
- Claude Code SKILL integration

### Features
- 8 shot types (EWS, WS, MS, MCU, CU, ECU, OTS, POV)
- 12 camera movement types
- Professional lighting and color palette terminology
- Bilingual prompt support (English/Chinese)

---

## Upcoming Features

### Planned for v2.1.0
- [ ] Additional scene templates (action, horror, documentary, etc.)
- [ ] Motion brush region specification for Runway
- [ ] Pika-specific parameter presets
- [ ] Video tutorial examples
- [ ] Community-contributed storyboards

### Planned for v3.0.0
- [ ] Interactive web interface
- [ ] Batch processing support
- [ ] Integration with popular video editing software
- [ ] AI-assisted scene analysis
- [ ] Collaborative storyboarding features

---

## How to Upgrade

### From v1.x to v2.0

1. **Backup your existing scripts**
2. **Pull the latest version**:
   ```bash
   git pull origin main
   ```
3. **Update your workflows**:
   - Old scripts will still work but won't have separated prompts
   - New scripts automatically use the image/video separation
4. **Check the examples**:
   - Review `examples/浪漫日落场景_分镜脚本_v2.md` for the new format

---

## Support

- 🐛 [Report Bugs](https://github.com/yourusername/cinematic-prompts/issues)
- 💡 [Request Features](https://github.com/yourusername/cinematic-prompts/issues)
- 📖 [Documentation](./README.md)

---

**Note**: Version numbers follow [Semantic Versioning](https://semver.org/):
- MAJOR version for incompatible API changes
- MINOR version for new functionality in a backwards compatible manner
- PATCH version for backwards compatible bug fixes
