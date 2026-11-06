# Vigilo: Feed Radar

<p align="center">
  <img src="assets/vigilo-icon.svg" alt="Vigilo App Icon" width="128" height="128">
</p>

<p align="center">
  <strong>High-signal desktop intelligence radar for continuous RSS, Atom, and X feeds powered by local vector embeddings and LLM briefings.</strong>
</p>

<p align="center">
  <a href="https://jmvallejo.github.io/vigilo-app/"><img src="https://img.shields.io/badge/Website-GitHub%20Pages-f59e0b?style=flat-square&logo=github" alt="Live Site"></a>
  <a href="https://github.com/jmvallejo/vigilo-app/issues"><img src="https://img.shields.io/badge/Issue%20Tracker-Open-10b981?style=flat-square&logo=github" alt="Issues"></a>
  <img src="https://img.shields.io/badge/Platform-macOS%2013%2B-0ea5e9?style=flat-square&logo=apple" alt="macOS 13+">
  <img src="https://img.shields.io/badge/Architecture-Universal%20(Apple%20Silicon%20%2B%20Intel)-8b5cf6?style=flat-square" alt="Universal Binary">
  <img src="https://img.shields.io/badge/Privacy-Local--First%20%26%20Zero%20Telemetry-ec4899?style=flat-square" alt="Privacy First">
</p>

---

## Overview

**Vigilo: Feed Radar** is an instrument-grade desktop intelligence application for macOS. Designed for researchers, engineers, and intelligence analysts who monitor high-volume information feeds, Vigilo operates silently in the background, transforming noisy firehoses (RSS, Atom, Reddit feeds, and X lists) into structured, contextual signals using on-device ONNX vector embeddings and dual-stage AI briefings.

This repository serves as the official public website, documentation portal, and community issue tracker for Vigilo.

---

## Live Navigation & Documentation

| Portal | URL | Description |
| :--- | :--- | :--- |
| **Official Website** | [jmvallejo.github.io/vigilo-app](https://jmvallejo.github.io/vigilo-app/) | Product overview, visual walkthrough, and architecture pipeline |
| **Documentation & FAQ** | [jmvallejo.github.io/vigilo-app/support.html](https://jmvallejo.github.io/vigilo-app/support.html) | Getting started guide, feed format reference, and troubleshooting |
| **Privacy Policy** | [jmvallejo.github.io/vigilo-app/privacy.html](https://jmvallejo.github.io/vigilo-app/privacy.html) | Strict on-device data guarantees and zero-telemetry architecture |
| **Terms of Service** | [jmvallejo.github.io/vigilo-app/terms.html](https://jmvallejo.github.io/vigilo-app/terms.html) | End-user licensing and terms of service |
| **Public Issue Tracker** | [github.com/jmvallejo/vigilo-app/issues](https://github.com/jmvallejo/vigilo-app/issues) | Bug reports, feed compatibility tickets, and feature requests |

---

## Public Issue Tracker Guide

We use GitHub Issues on this repository for all public feedback, bug reporting, and feature roadmap requests.

### 1. Submitting a Bug Report
When opening a bug report via [New Issue](https://github.com/jmvallejo/vigilo-app/issues/new), please include:
- **macOS Version:** (e.g., macOS 14.5 Sonoma, Apple Silicon M-series or Intel).
- **Application Version:** (Found in *Vigilo > About Vigilo*).
- **Feed URL / Format:** If reporting a parsing issue, please share the feed URL or format (RSS 2.0, Atom, JSONFeed, Reddit XML).
- **Observed Behavior:** What happened versus what you expected to happen.
- **Log Snippet:** If relevant, sanitized logs from the application diagnostics pane.

### 2. Submitting a Feature Request
Have an idea for a new radar view, local embedding model, or custom notification trigger?
- Check existing [open issues](https://github.com/jmvallejo/vigilo-app/issues) to avoid duplicates.
- Clearly describe the use case and how the proposed change enhances your intelligence monitoring workflow.

---

## Security & Privacy Architecture

Vigilo was engineered from day zero with a strict **Local-First** philosophy:

- **Local Embedded Database:** All subscription feeds, downloaded articles, semantic embeddings, and user annotations remain exclusively on your physical device in an embedded SQLite database (`sqlite3` / local vector table).
- **Zero Cloud Middlemen:** Network requests travel directly from your Mac to the publisher's origin server. No analytics proxy, no aggregation relay, and no proprietary sync cloud inspect your traffic.
- **Zero Telemetry:** No user analytics, telemetry pingbacks, crash reporting daemons, or behavioral trackers are bundled into the binary.
- **Private Intelligence Pipelines:** Semantic embeddings run locally using quantized ONNX / Candle models on Apple Silicon Neural Engine / CPU. LLM briefings support local backends (e.g., Ollama / MLX) or direct user-provided API keys without retention.

For complete disclosures, review the [Privacy Policy](https://jmvallejo.github.io/vigilo-app/privacy.html).

---

## Static Website Tech Stack

The documentation site and landing page are built to match the high-performance, minimalist aesthetic of the desktop app:

- **Semantic HTML5:** Clean, accessible markup without bloated single-page application (SPA) wrappers.
- **CSS Custom Properties:** Modular dark-theme design system featuring precision radar indicators, amber glow highlights, responsive layouts, and monospace data grids.
- **Zero External Runtime Dependencies:** No tracking scripts, no third-party analytics, and zero heavyweight JavaScript frameworks.
- **GitHub Pages Ready:** Configured with `.nojekyll` to bypass Jekyll transformation and serve raw assets with high throughput and instant edge caching.

### Local Development / Preview

To test or view the documentation site locally:

```bash
# Using Python 3 built-in HTTP server
python3 -m http.server 8000

# Or using Node.js npx serve
npx serve .
```

Open `http://localhost:8000` in your browser.

---

## License & Credits

- © 2026 **Juan Manuel Vallejo**. All rights reserved.
- For inquiries or support, submit a ticket on our [Issue Tracker](https://github.com/jmvallejo/vigilo-app/issues).
