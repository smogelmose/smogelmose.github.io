---
title: "Metamorphic Efforts: Embodied Polyphony in Literary Prose"
excerpt: "A generative audiovisual translation of the opening of Kafka's The Metamorphosis, driven by Laban Movement Analysis Effort qualities extracted from close reading of the source text.  <br/><img src='/images/metamorphic_efforts_front.png'>"
collection: portfolio
---

*Embodied polyphony: enacting the kinesthetic body of prose.*

A generative audiovisual translation of the opening of Franz Kafka's *The Metamorphosis*, driven by Laban Movement Analysis (LMA) Effort qualities extracted through close reading of the source text. The project advances a central claim: literary prose contains a kinesthetic body, extractable through annotation and renderable as embodied audiovisual experience. Developed for the MED8 Embodied Interaction course at Aalborg University Copenhagen.

<div style="padding:56.25% 0 0 0;position:relative;margin:2em 0;">
  <iframe src="https://player.vimeo.com/video/1187075793?h=da418fe0da&title=0&byline=0&portrait=0" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Metamorphic Efforts walkthrough"></iframe>
</div>

A 10-passage walkthrough of the piece. Each passage is annotated for LMA (BESS: Body, Effort, Shape, Space) through close reading; the resulting trajectory drives a real-time TouchDesigner visual field and a five-layer polyphonic audio mix in the browser. The Action Drive arc moves Press → Wring → Glide → Slash, tracking Gregor's progression from oppressive constriction through anguished struggle to a brief moment of release and finally to the violent break of the manager's arrival.

## Theoretical framing

The work locates the moving body in literary prose, drawing on phenomenological accounts of embodied perception (Merleau-Ponty, Dourish) and motor simulation theories of reading (Gallese and Lakoff). LMA Effort qualities - Weight, Time, Space, and Flow - serve as the descriptive vocabulary for translating textual movement cues into a generative system. The annotation method inverts Fdili Alaoui et al.'s BESS pipeline, moving from text to close reading to BESS annotation to generative output rather than from body to sensors to classification. Effort-to-emotion mappings draw on de Meijer's empirical validation, and the polyphonic structure invokes Bakhtin to account for multiple simultaneous movement voices within a single passage.

## Architecture

The piece is delivered through a Twine (SugarCube) browser interface that handles text, narration, and a canvas displaying live frames streamed from a headless TouchDesigner instance. TouchDesigner streams JPEG frames over WebSocket at approximately 15fps to the browser canvas, where they composite alongside five polyphonic audio layers - narration, body vocalizations, drones, sound effects, and character voices - each with independent gain control. LMA annotations reveal progressively as the reading unfolds, with hover tooltips exposing the underlying Effort qualities.

## Method

Each passage is annotated for Effort qualities through close reading. The annotation is converted into a numerical trajectory and processed in JavaScript using formulas from Larboulette and Gibet (MOCO 2015) to compute live LMA descriptors. These descriptors drive an Action Drive preset-selector architecture (after Siopa et al.) in TouchDesigner, which selects from a bank of visual presets corresponding to LMA Effort drives. Character voices were generated with ElevenLabs v3; drones via ElevenLabs Music Generation; narration delivered through the browser's audio stack.

## Status and next steps

The project is complete as a course deliverable, with a lab study (N=12-15) designed to evaluate two empirical claims: that LMA Effort qualities can be extracted from literary prose through close reading, and that Effort ratings predict emotional responses during the embodied reading experience. A paper submission to MOCO or CHI is in preparation.

Source code and documentation: [github.com/smogelmose/Embodied-interaction](https://github.com/smogelmose/Embodied-interaction)