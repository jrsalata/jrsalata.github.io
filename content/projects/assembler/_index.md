---
title: "Assembler"
author: "John Salata"
description: "Here is the story of how I designed, built, and tested a SIC/XE assembler."
draft: false
---

In the Fall 2024 semester, I took a Computer Structures class that covered a lot of the lower-level features of computers that we often take for granted.  Some of the topics that we covered include, but not limited to, assembly, linkers, loaders, and compiler design.  The big final project that we spent the entire semester on was to build an assembler for the SIC/XE instruction set. We could use any language or tool that we wanted to as long as all of the work was original.  For me, this was the first project I've worked on with no guardrails or language requirements.  This openness made it an interesting challenge and opportunity to work with new tools.

Here, I've documented some of my work and experiences with this project in order to explain all of the effort that went behind it.

All of the technical documentation of everything is available [here](/docs/apidocs/index.html) and the source code is available [here](https://github.com/jrsalata/assembler). The documentation was automatically generated using javadocs and there may be some typos and formatting issues as I am not the most familiar with it.  If you see an issue, please consider [submitting an issue](https://github.com/jrsalata/Assembler/issues) so I can fix it.  There is a lot and it is tricky for one person to look over everything.
