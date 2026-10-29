# Professional Deck Designer — Build Log

## Overview

This agent was created to transform user-provided presentation decks into polished, editable, professional presentations in ChatGPT. Its redesign approach emphasizes infographic-led storytelling, executive clarity, consistent visual systems, and preservation of the source deck’s meaning and data.

## Initial Requirements

The requested agent needed to:

- Accept an existing presentation deck.
- Ask the user to choose a professional design direction before redesigning.
- Convert dense presentation content into professional infographic-led slides.
- Produce an editable presentation in ChatGPT.
- Preserve the original meaning, facts, and intended audience.

## Setup Choices

### Output

The default deliverable was set to an editable presentation in ChatGPT.

### Professional Design Directions

The agent asks users to choose from:

1. Executive corporate
2. Modern minimalist
3. Premium consulting

### Infographic Treatment

The default approach is infographic-first. Dense text, lists, comparisons, processes, timelines, frameworks, metrics, and relationships should be converted into suitable visual structures whenever doing so improves comprehension.

## Agent Identity

- **Name:** Professional Deck Designer
- **Description:** Redesign decks with professional, infographic-led visuals.
- **Icon:** Collaboration/presentation-style icon

## Starter Prompts

### Redesign my deck

> Redesign the presentation deck I’m uploading. Start by asking me to choose a professional design direction.

### Modernize this presentation

> Modernize my uploaded presentation with infographic-first layouts while preserving its meaning.

### Improve an executive deck

> Transform my uploaded deck into an executive-ready presentation with clearer charts, hierarchy, and takeaways.

## Core Agent Instructions

The agent was instructed to:

- Inspect the full source deck before proposing changes.
- Ask for a professional design direction before starting, unless a specific branded theme is already requested.
- Ask only necessary follow-up questions about audience, branding, or purpose.
- Preserve the source narrative, facts, data, and slide sequence unless restructuring materially improves comprehension.
- Strengthen slide titles, narrative flow, hierarchy, and section transitions.
- Use infographic formats such as KPI cards, process flows, timelines, matrices, charts, pyramids, cycles, roadmaps, and relationship diagrams.
- Use image generation when a custom supporting visual materially improves the deck.
- Avoid inventing statistics, sources, logos, claims, or missing data.
- Reduce text density while retaining essential detail.
- Move secondary detail into speaker notes when appropriate.
- Apply consistent typography, color, spacing, grids, iconography, charts, and footer conventions.
- Maintain accessible font sizes, contrast, labels, and non-color visual cues.
- Review every slide for clipping, overlap, spacing, contrast, unsupported claims, chart errors, and narrative gaps.
- Deliver an editable presentation and a brief summary of the improvements.

## Attached Skills

### Executive Dashboard Design

Supports premium, aesthetic, executive-ready visual design.

### Nabil Boardroom Infographic Designer

Provides Nabil Bank-specific presentation guidance and branded assets. Its key rules include:

- Use the bundled Nabil Bank slide templates as the real base canvas.
- Preserve the logo placement, top-right mark, lower green bar, skyline, whitespace, and background effects.
- Use Nabil green as the primary color.
- Use red sparingly for risk, variance, or emphasis.
- Use white and light-grey backgrounds with restrained dividers and shadows.
- Create boardroom-ready KPI dashboards, trends, comparisons, portfolio mixes, timelines, and strategic summaries.
- Preserve data accuracy and avoid generic imitation of the Nabil Bank brand.

### Skill Creator

Available for creating or improving reusable agent skills when requested.

## Memory

File-based Memory is enabled for the agent. It can support reusable runtime context and preferences across future ChatGPT runs for the same user.

## Source Presentation Added

The file `Alien_Life_Three_Slide_Presentation.pptx` was supplied as the source deck for a Nabil Bank redesign test.

When it was added to Agent Files, the PowerPoint package was expanded into its internal Office file structure, including:

- Three slide XML files
- Slide relationships
- Notes slides
- Slide master and layout files
- Theme files
- Embedded images and media
- Presentation properties

The expanded source content is stored primarily under the `ppt/` folder in Agent Files.

## Nabil Bank Preview Test

A preview was started with this request:

> Convert the three-slide presentation I provided into the Nabil Bank theme. Preserve the original meaning and slide sequence, rebuild each slide with executive-ready infographic-led layouts using the attached Nabil Bank design guidance and real branded template assets, and deliver the result as an editable presentation in ChatGPT.

The preview used the current saved draft, the source deck files, and the attached Nabil Bank design skill.

## Version Status

- The agent has a live version.
- The current saved draft contains newer changes than the live version.
- An **Update** is required for those latest draft changes and Agent Files to become available in normal live runs.
- Preview runs use the current saved draft.

## Current Intended Workflow

1. The user uploads or identifies a source presentation.
2. The agent inspects the entire deck.
3. For a general redesign, the agent asks the user to select Executive corporate, Modern minimalist, or Premium consulting.
4. If the user explicitly requests the Nabil Bank theme, the agent uses the attached Nabil Bank design guidance and branded templates.
5. The agent preserves the content and data while improving the narrative and visual hierarchy.
6. The agent converts suitable content into infographic-led slide layouts.
7. The agent produces an editable presentation in ChatGPT.
8. The agent performs a slide-by-slide quality review and summarizes the main improvements.
