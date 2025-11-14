# Financial Document Insight Agent
A modular multimodal analysis pipeline that processes financial document images, extracts meaningful regions, and generates structured insights using vision-language models. The system is built around a decorator-driven prompting framework, enabling clean orchestration of image preprocessing, prompt construction, and model interaction.

## Overview
The agent ingests full financial statements or individual page images, isolates relevant visual sections using PIL-based transformations, and merges them into a unified prompt. This prompt is passed to GPT-4o-level models for contextual reasoning, summary generation, and insight extraction. The workflow is intentionally modular, allowing each stage—image handling, prompt assembly, and result formatting—to evolve independently.

## Features
* Multimodal pipeline for analyzing financial documents
* Decorator-based orchestration for predictable, testable steps
* Image region extraction and preprocessing with PIL
* Unified prompt construction supporting multiple images
* Vision-language model integration for narrative financial insights
* Extensible architecture for new document types and analysis logic

## How It Works
The pipeline begins by loading raw statements, slicing them into meaningful visual segments, and applying lightweight image transformations for clarity. These images are then packaged into a structured prompt with metadata and contextual scaffolding. The model returns a final set of insights, which the system formats into a clean, human-readable summary.

## Architecture
* **Image Loader & Preprocessor** – isolates specific regions from financial statements.
* **Prompt Builder** – constructs multi-image prompts through decorators.
* **Model Interface** – communicates with the vision-language backend.
* **Output Formatter** – organizes structured responses into usable text.

## Intended Use
Ideal for experiments in financial-document understanding, multimodal prompting, and automated report generation. The design favors clarity and extensibility for developers exploring advanced prompt engineering or vision-language pipelines.

## Future Enhancements
* Support for additional document layouts
* More granular region-extraction strategies
* Plug-and-play model backends
* Evaluation utilities for insight accuracy
