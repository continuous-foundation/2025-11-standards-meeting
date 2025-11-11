---
title: Day 3
subtitle: Demo Day
description: The third day we presented on our progress and discussed next steps for several of the projects.
---

Snippets of what we presented are below. We then talked about next steps, especially in the context of new formats/standards (OXA) and the application development shown by the "Spotify for Science" application.

## Open Exchange Architecture (OXA)

Define shared schemas and tools for authoring, publishing and archiving scientific content, based from experience in the scientific authoring ecosystem (Quarto, MyST, Curvenote, Stencila) — a new Open Exchange Architecture. We aimed to present on (a) a new schema with examples; (b) how this can export from quarto (as myst/stencila were already relatively compatible); (c) define high-fidelity links to components; (d) discuss the "container" for the research content; and (e) discuss how this could work with other publishing systems and tools (JATS, MECA, Octopus, etc.). Crucially, we wanted to leave with something **concrete** that had a name (which we came up with together on day 2), logo, domain, repository and could be installed from node and pypi.

:::{figure} carlos-oxa.png
Carlos presenting on the schemas for the Open Exchange Architecture (OXA).
:::

We created a [GitHub Repository](https://github.com/scientific-publishing-tools-meeting/oxa) and [website](https://oxa.dev) to push the effort forward.

## Creative Commons — Modular Reuse, Licensing and Attribution

Work with the open exchange group to ensure the component framework has licensing and attribution built directly into the architecture. This should work for existing narrative containers (articles, papers, preprints, protocols), modular components (panels, figures, tables, datasets, etc.), as well as remixed compositions of research that are a hybrid of the two (an article that references a different figure or panel).

Researcher produces a “Paper Repo” (made of a collection of objects). Shareable as an object.
The paper repo is made of claims (hypothesis headlines), each presented as containers of a panels of evidence. Each panel of evidence (PE) supports its claim with text, figures, and tables. Panels of evidence can exist as an embed or be output as their own PDFs.
Each panel of evidence has a corresponding container of its panel dependencies (PD).

Each PD can contain supporting assets:

- Code: Code snippets, source code, linkouts to a repo of code (eg., in Github).
- Research Datasets: Part of the files structure, or in a linked data bucket.
- Design Files: Practicable/manufacturable and/or related to patenting, so functionally distinct. Can be for different types of things that are designed, including formulations.
- Lab Notes: The scratchpad that accompanies the panel.

Researchers can then publish the entire paper repo as a PDF Paper (but not the dependencies, which can just be linked out).

:::{figure #fig-taslar} taslar.png
The TASLAR framework which stands for Title, Author, Source Link, License Link, Attribution Statement, Rights Statement (Creative Commons).
:::

## Utilizing and Extending MECA

Discuss ways to use existing flexible transfer mechanisms, such as MECA, to bring this format to interoperate with the existing submission and publishing systems. The MECA file format is very flexible and the working group is looking to modernize the NISO recommendation in 2026 to incorporate new cloud-based storage and APIs.

## Computational Research Content + AI

Produce an experiment of pulling together two computational articles (written in MyST) and explore what can be done with the additional context this provides to research agents.

## Spotify for Science

Lead an effort to bring many APIs and services together into a new way to browse research that can elevate different trust signals and show research content in new ways.

:::{figure} spotify-for-science.mp4
A walkthrough of the application that was developed in a day that pulled together APIs from a number of different projects in the ecosystem. It is live here: https://v0-aperio-ui-design.vercel.app/
:::

:::{dropdown} List of features Shipped 🚀

**Summary of Features Added**

- Initial Application Build: The first version of Aperio was created with its core "Spotify for Science" design. This included a dark, 3-column layout, navigation/playlist sidebar, a main personalization card (with mock data for suggestions), and a right "friend activity" sidebar.
- "Build My Feed" Button (First Pass): The button was wired up with an onClick handler that initially just logged the user's selections and showed an alert.
- Functional Feed Generation: The button was updated to actually fetch and display a personalized feed of research papers (with titles, authors, abstracts, etc.) based on the selected topics.
- Feed Size Increase: The API call was updated to fetch 20 papers per topic instead of just 3.
- Feed Loading Fix: A bug was fixed where the feed wouldn't display correctly. This was solved by adding logic to reset and clear the old feed before building a new one.
- Live API for Autosuggest: The mock data for the topic suggestions was replaced with a live integration of the OpenAlex keywords API, allowing for real-time topic searching.
- Recency Filtering (First Version): A new feature was added to improve recency. The app was updated to fetch 200 results, filter them to show only papers from the current year (2025), and then display the 20 most recent ones.
- Font Change: The application's font was switched from Geist to Noto Sans.
- Scite.ai Badge Integration: The scite.ai "Trust" badge was added to each paper card, using the paper's DOI to display citation metrics (supporting, mentioning, contrasting).
- Scite.ai Loading Fix (Attempt 1): A useEffect hook was added to manually re-initialize the scite.ai badges after the paper cards were dynamically rendered.
- Feed Rendering Bug Fix: A major bug was fixed where nothing was rendering. This was traced to an incorrect sort=cited_by_count parameter being left in the API call.
- Relevance Sorting: A new sort parameter (sort=relevance_score:desc) was added to the OpenAlex API call.
- Recency Filtering (Second Version): The year-based filtering logic was removed entirely because it was filtering out all results. The app was simplified to fetch and display the top 20 most relevant results from the API, regardless of the year.
- "Data Availability" Badge Fix: A significant bug was fixed where the "Data Available" badge wasn't showing. The logic was completely rewritten to recursively traverse the entire document structure (MDAST tree) to find the "Data Availability" section.
- Tooltip z-index Fix: The tooltip for the "Data Available" badge was fixed so it would appear above the right sidebar by increasing its z-index.
- Priority Paper Feature: Logic was added to prioritize a specific paper (DOI: 10.1101/2025.09.29.679315). When "Chikungunya virus" is searched, the app now fetches this paper directly and prepends it to the top of the results.
- DocMap URL Fix: The URL for the Sciety DocMap API (used for peer review data) was corrected to the proper format.

**Batch of UI & Logic Tweaks**

- Badge Colors: The colors for the "Open Access" (to orange) and "Data Available" (to green) badges were swapped.
- CC Logo: The Creative Commons (CC) logo was added to the license badge as an inline SVG.
- Hide Scite Badge: The scite.ai badge was updated to be hidden on papers with 0 citations.
- Remove Card Numbers: The numerical prefixes (e.g., "01", "02") were removed from the paper cards.
- Card Styling Change: The paper cards were visually updated from a dark navy background to a white background (bg-white), with text and border colors adjusted for readability.
- Homepage Tiles: The homepage was updated to feature three distinct tiles: "New Feed" (original behavior), "Chikungunya Research" (hardcoded search), and "MRI Research" (hardcoded search).
- Query Parameter Support: To support the new tiles, the feed page was updated to accept a topic query parameter, allowing it to build a feed automatically from a URL.
- Loading Flash Fix: An initialLoading state was added. This displays a clean loading screen (instead of the personalization form) when the feed is loaded via a query parameter, eliminating the "flash" of content.

:::

## Model Communities

Identify early communities to pilot these approaches with, including from additional computational communities that require more context and different "weird-and-wonderful" research objects to be published (e.g. notebooks, microscopy images, etc.) as well as paths to adoption.
