# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
