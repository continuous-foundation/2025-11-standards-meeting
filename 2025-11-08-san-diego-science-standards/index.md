---
title: 'From Tools to Adoption: A Path to Modular and Interactive Scientific Publishing'
abstract: |
  Scientific content remains trapped in static formats that limit reuse, attribution, and machine readability, despite the availability of modern tooling that makes this possible and better matches how scientists conduct research. This initiative, led by openRxiv and Continuous Science Foundation, addresses this challenge through practical implementation rather than consensus-driven standardization. The project will convene developers of leading modular publishing tools—MyST, Quarto, Curvenote, and Kotahi—to create a working, federated reference architecture using real bioRxiv content and deploying through the newly created openRxiv labs. Through a facilitated virtual meeting followed by a 2.5-day in-person implementation sprint, participants will develop shared interoperability standards and demonstrate live reuse of scientific content. Following the successful ipynb model, the approach prioritizes working software over abstract frameworks. Key deliverables include a reference implementation demonstrating cross-platform interoperability, pilot deployments using bioRxiv articles, progress updates at the CZI Open Science Meeting, and adoption materials for publishers and platforms. This implementation-first approach represents a concrete step toward modular publishing that meets current needs while preparing for the LLM era.
---

## Workshop Overview

In San Diego November 6-8th, 2025 a group of 25 open-science leaders gathered at the [San Diego Made Factory](https://www.sandiegomade.org/) for an in-person implementation workshop to unify modular scientific publishing tools around shared reference implementations. The working meeting, hosted by [openRxiv](https://openrxiv.org) and [Continuous Science Foundation](https://continuousfoundation.org) convened developers of leading modular publishing tools and licensing to create a working, federated reference architecture using real bioRxiv content, connected authoring tools, and worked towards shared standards. Our goal was to resolve technical gaps, demonstrate live interoperability, and lay the foundation for modular, machine-readable research publishing. The workshop was preceded by a virtual kickoff and included discussions and activities at CZI's Open Science Meeting and JupyterCon. This meeting was designed to unlock adoption by showing, not telling, how modular publishing can work in practice today.

Our approach for the workshop was to convene a small group of 25 leaders and tool makers in open science to align on a collective vision/demonstrations and implementations to drive meaningful change. Given the small size and implementation focus, this meeting was by invitation only.

This meeting is funded by the Meeting Fund of The Navigation Fund Open Science Program. [10.71707/gn91-ka32](https://commons.datacite.org/doi.org/10.71707/gn91-ka32).

:::{figure #fig-team} team.png

Participants of the workshop in November 8, 2025 in San Diego, California. Agah Karakuzu, Anton Molina, Carlos Scheidegger, Carol Willing, Chris Wilkinson, Franklin Koch, Jason Priem, John Bohannon, John Kaye, Kevin-John Black, Matt Akamatsu, Michael Markie, Milton Pividori, Monica Granados, Nokome Bentley, Paul Shannon, Raj Palleti, Rose Reatherford, Rowan Cockett, Steinn Sigurdsson, Taylor Campbell, Ted Roeder, Tom Scott, Tracy Teal.

:::

## The Three Days

Over two and a half days, we moved from setting shared context and vision to hands-on building and prototyping, culminating in demos and concrete next steps. Each day built on the previous one, with structured discussions giving way to parallel work streams and finally public presentations of what we'd accomplished together.

:::{card} 🗺️ Setting Context & Direction (Nov 6)
:url: ./day-1.md
We kicked off with lightning talks from Quarto, eLife, Creative Commons, arXiv, and others, then dove into ideation sessions to dream up an idealistic future for scientific communication. The group aligned on a powerful metaphor—Bedrock, Soil, and Flowers—to describe the evolving structure of scientific knowledge, and broke into working groups to tackle concrete implementation challenges. Read about the full day's discussions, the case studies we explored, and how we organized ourselves for the work ahead.
:::

:::{card} 👩‍💻 Hacking, Building, Vibe-ing (Nov 7)
:url: ./day-2.md
Teams worked in parallel on six key initiatives: building the Open Exchange Architecture (OXA) schemas, integrating Creative Commons licensing, extending MECA for interoperability, exploring computational research content with AI, prototyping a "Spotify for Science" application, and identifying model communities for pilot deployments. See what we built, the technical decisions we made, and how the different groups collaborated throughout the day.
:::

:::{card} 🚀 Demo Day & Next Steps (Nov 8)
:url: ./day-3.md
We presented our progress: a new OXA format with working schemas and repositories, a TASLAR framework for modular licensing and attribution, a live "Spotify for Science" prototype, and discussions on computational research content and community adoption. Then we mapped out concrete next steps for moving these initiatives forward. Watch the demos and see where we're heading next.
:::

## Participants

| Name               | Organization                                   |
| ------------------ | ---------------------------------------------- |
| Agah Karakuzu      | NeuroLibre                                     |
| Anton Molina       | b.next                                         |
| Carlos Scheidegger | Quarto/Posit                                   |
| Carol Willing      | Willing Consulting                             |
| Chris Wilkinson    | PreReview                                      |
| Franklin Koch      | Curvenote, Jupyter                             |
| Jason Priem        | OpenAlex                                       |
| John Bohannon      | alphaXiv                                       |
| John Kaye          | octopus                                        |
| Kevin-John Black   | bioRxiv/openRxiv                               |
| Matt Akamatsu      | DiscourseGraphs                                |
| Michael Markie     | eLife                                          |
| Milton Pividori    | University of Colorado Anschutz Medical Campus |
| Monica Granados    | Creative Commons                               |
| Nokome Bentley     | Stencila                                       |
| Paul Shannon       | eLife                                          |
| Raj Palleti        | alphaXiv                                       |
| Rose Reatherford   | PLOS                                           |
| Rowan Cockett      | CSF, Curvenote, Jupyter                        |
| Steinn Sigurdsson  | arXiv                                          |
| Taylor Campbell    | Creative Commons                               |
| Ted Roeder         | bioRxiv/openRxiv                               |
| Tom Scott          | PLOS                                           |
| Tony Alves         | HighWire                                       |
| Tracy Teal         | openRxiv                                       |

Regrets: Stephan Van der Walt (Jupyter), Chris Hartgerink (ResearchEquals), Gabe Stein (KnowledgeFutures), Chris Holdgraf / Greg Caporaso (MyST Steering Council), Adam Hyde (Coko/Katahi).
