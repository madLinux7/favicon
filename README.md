# favicon

[![License](https://img.shields.io/badge/license-Unlicense-blue?style=flat-square)](UNLICENSE)
[![Shell](https://img.shields.io/badge/shell-bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)](favicon)
[![Dependency](https://img.shields.io/badge/requires-ImageMagick-BF4B8A?style=flat-square)](https://imagemagick.org)
[![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20macOS-blue?style=flat-square)](favicon)

Dead simple favicon generator. Converts any image to `.ico` using ImageMagick — single 16x16 or a multi-size bundle.

![DEMO](demo_bundle.gif)

## Requirements

- UNIX shell (sh / bash / zsh / fish etc.)
- [`ImageMagick`](https://imagemagick.org) (`magick` in PATH)

## Installation

```bash
curl -fsSL https://raw.githubusercontent.com/madLinux7/favicon/master/favicon -o ~/.local/bin/favicon && chmod +x ~/.local/bin/favicon
```

Or manually:

```bash
git clone https://github.com/madLinux7/favicon
cp favicon/favicon ~/.local/bin/favicon
chmod +x ~/.local/bin/favicon
```

## Usage

```
favicon [--bundle] <file> [outfile]
```

| Argument   | Description                                      |
|------------|--------------------------------------------------|
| `file`     | Source image (PNG, SVG, etc.)                    |
| `outfile`  | Output path (default: `favicon.ico`)             |
| `--bundle` | Bundle 16, 32, 48, 64, 128, 256 px into one .ico |

## Examples

```bash
# Single 16x16 favicon
favicon logo.png

# Custom output path
favicon logo.svg output/favicon.ico

# Multi-size bundle
favicon --bundle logo.svg public/favicon.ico
```
