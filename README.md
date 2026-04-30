# Ancient History: Origins to 1200 CE

[![MkDocs](https://img.shields.io/badge/Made%20with-MkDocs-526CFE?logo=materialformkdocs)](https://www.mkdocs.org/)
[![Material for MkDocs](https://img.shields.io/badge/Material%20for%20MkDocs-526CFE?logo=materialformkdocs)](https://squidfunk.github.io/mkdocs-material/)
[![GitHub Pages](https://img.shields.io/badge/View%20on-GitHub%20Pages-blue?logo=github)](https://dmccreary.github.io/ancient-history/)
[![Built with Claude Code](https://img.shields.io/badge/Built%20with-Claude%20Code-DA7857?logo=anthropic)](https://claude.ai/code)
[![Claude Skills](https://img.shields.io/badge/Uses-Claude%20Skills-DA7857?logo=anthropic)](https://github.com/dmccreary/claude-skills)
[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## View the Live Site

Visit the interactive textbook at: [https://dmccreary.github.io/ancient-history/](https://dmccreary.github.io/ancient-history/)

## Overview

This is an interactive, AI-assisted intelligent textbook covering ancient world history from cosmic and biological origins through the maturation of post-classical civilizations, ending at approximately 1200 CE. It is designed for undergraduates and motivated general readers who want a single coherent narrative that runs from the Big Bang to the eve of the Mongol expansion.

The course is organized around the UCLA "World History for Us All" **Big Era framework** (Eras 1–5) and three thematic axes: *Humans and the Environment*, *Humans and Other Humans*, and *Humans and Ideas*. A core editorial commitment is to treat archaeological, paleoanthropological, and paleogenomic findings published in the **last fifteen years** as first-class concept nodes — Göbekli Tepe and the Tas Tepeler complex, Lomekwi 3 stone tools, the Jebel Irhoud finds, Madjedbebe, the White Sands footprints, Sulawesi cave art, Sanxingdui, Caral-Supe, the ancient-DNA understanding of Yamnaya migration, the 4.2 ka Event, the Late Antique Little Ice Age, and more — not as footnotes to a pre-2010 narrative.

The textbook is built on a **directed learning graph of 297 concepts** with explicit dependencies, Bloom's Taxonomy alignment, and concept-level metadata. Content is generated and curated using a suite of Claude AI skills, and is guided through chapters by **Chronos**, a Galápagos-style tortoise mascot who keeps the long view in focus.

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/dmccreary/ancient-history.git
cd ancient-history
```

### Install Dependencies

This project uses MkDocs with the Material theme:

```bash
pip install mkdocs
pip install mkdocs-material
```

### Build and Serve Locally

Build the site:

```bash
mkdocs build
```

Serve locally with live reload:

```bash
mkdocs serve
```

Open your browser to `http://127.0.0.1:8000/ancient-history/`.

### Deploy to GitHub Pages

```bash
mkdocs gh-deploy
```

This builds the site and pushes it to the `gh-pages` branch.

### Using the Book

- Use the left sidebar to browse chapters, learning graph pages, and MicroSims.
- Use the search icon (top right) to search across all content.
- Open the [Learning Graph Viewer](https://dmccreary.github.io/ancient-history/sims/graph-viewer/) to explore concept dependencies visually.
- Edit markdown files in `docs/` to modify content, and adjust `mkdocs.yml` to change site structure or navigation.

## Repository Structure

```
ancient-history/
├── docs/                                # MkDocs documentation source
│   ├── index.md                         # Site landing page
│   ├── course-description.md            # Full syllabus
│   ├── chapters/                        # 16 chapter directories (Big Eras 1–5)
│   │   ├── 01-foundations-of-historical-thinking/
│   │   ├── 02-cosmic-and-biological-origins/
│   │   └── ... (through chapter 16)
│   ├── learning-graph/                  # Concept graph data and analysis
│   │   ├── learning-graph.json          # 297-concept DAG
│   │   ├── learning-graph.csv           # Dependency edges
│   │   ├── concept-taxonomy.md          # Concept categorization
│   │   ├── quality-metrics.md           # Graph quality analysis
│   │   └── taxonomy-distribution.md     # Distribution report
│   ├── sims/                            # Interactive MicroSims
│   │   └── graph-viewer/                # vis-network learning graph viewer
│   ├── img/mascot/                      # Chronos the tortoise pose images
│   ├── css/                             # Custom CSS (mascot styling, theme tweaks)
│   └── js/                              # MathJax config and other JS
├── logs/                                # Session logs from skill runs
├── mkdocs.yml                           # MkDocs configuration
├── CLAUDE.md                            # Project instructions for AI authoring
└── README.md                            # This file
```

## Reporting Issues

Found a bug, a typo, an outdated date, or a place where the textbook should incorporate newer evidence? Please open an issue:

[GitHub Issues](https://github.com/dmccreary/ancient-history/issues)

When reporting, please include:

- A description of the problem or suggestion
- The chapter, section, or page URL where it appears
- A citation if you are flagging an evidence update
- Screenshots for rendering or MicroSim issues

## License

This work is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

**You are free to:**

- Share — copy and redistribute the material
- Adapt — remix, transform, and build upon the material

**Under the following terms:**

- **Attribution** — Give appropriate credit with a link to the original
- **NonCommercial** — No commercial use without permission
- **ShareAlike** — Distribute contributions under the same license

## Acknowledgements

This project stands on the shoulders of an extraordinary open source and scholarly community:

- **[MkDocs](https://www.mkdocs.org/)** — Static site generator for project documentation
- **[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)** — Theme used throughout this site
- **[vis-network](https://visjs.org/)** — Network visualization library powering the learning graph viewer
- **[MathJax](https://www.mathjax.org/)** — Rendering of equations and scientific notation
- **[Python](https://www.python.org/)** — Used for graph validation, taxonomy analysis, and content tooling
- **[Claude AI](https://claude.ai)** by Anthropic — AI-assisted authoring, learning graph generation, and quality review
- **[GitHub Pages](https://pages.github.com/)** — Free hosting for the published site
- **UCLA "World History for Us All"** — Big Era framework that organizes the course
- The archaeologists, paleoanthropologists, and paleogenomicists whose recent fieldwork makes the modern version of this story tellable

## Contact

**Dan McCreary**

- LinkedIn: [linkedin.com/in/danmccreary](https://www.linkedin.com/in/danmccreary/)
- GitHub: [@dmccreary](https://github.com/dmccreary)

Questions, suggestions, or collaboration opportunities are welcome — connect on LinkedIn or open an issue on GitHub.
