# **Fossil Audio by Fossil Logic**

**Fossil Audio** is a lightweight, cross-platform audio library written in pure C with zero external dependencies. Designed for real-time audio processing, playback, and recording, Fossil Audio provides simple, efficient APIs for handling audio streams across Windows, macOS, Linux, and embedded systems while maintaining minimal footprint and maximum portability.

### Key Features

- **Cross-Platform Support**  
  Works reliably on Windows, macOS, Linux, and embedded platforms.

- **Zero External Dependencies**  
  Pure C implementation ensures maximum portability, auditability, and ease of integration.

- **Real-Time Audio Processing**  
  Supports low-latency audio playback, recording, and streaming for performance-critical applications.

- **Flexible Audio Formats**  
  Supports multiple sample rates, channels, and buffer configurations.

- **Lightweight and Efficient**  
  Optimized for minimal resource usage, suitable for embedded and low-power devices.

- **Modular Design**  
  Easily integrated or extended to support custom audio workflows.

## Getting Started

### Prerequisites

- **Meson Build System**  
  Fossil Audio uses Meson for build configuration. If you don’t have Meson installed, follow the instructions on the official [Meson website](https://mesonbuild.com/Getting-meson.html).

### Adding Fossil Audio as a Dependency

#### Using Meson

1. **Install or Upgrade Meson** (version 1.3 or newer recommended):

```sh
   python -m pip install meson           # Install Meson
   python -m pip install --upgrade meson # Upgrade Meson
```

###	Add the .wrap File
Place a file named fossil-audio.wrap in your subprojects directory with the following content:

```ini
# ======================
# Git Wrap package definition
# ======================
[wrap-git]
url = https://github.com/fossillogic/fossil-audio.git
revision = v0.1.0

[provide]
fossil-audio = fossil_audio_dep
```

###	Integrate in Your meson.build
Add the dependency by including this line:

```meson
audio_dep = dependency('fossil-audio')
```


## Build Configuration Options

Customize your build with the following Meson options:
	•	Enable Tests
To run the built-in test suite, configure Meson with:

```sh
meson setup builddir -Dwith_test=enabled
```

## Contributing and Support

For those interested in contributing, reporting issues, or seeking support, please open an issue on the project repository or visit the [Fossil Logic Docs](https://fossillogic.com/docs) for more information. Your feedback and contributions are always welcome.
