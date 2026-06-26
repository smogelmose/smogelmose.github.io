---
title: "What Is It Like To Be a Tree: Embodying a Tree in VR to Promote Cognitive Flexibility, Nature Connectedness, and Mild Altered States."
excerpt: "An embodied VR experience placing participants in the role of a tree in a responsive forest ecosystem, driven by breath-based biofeedback through a mycorrhizal root network, evaluated for effects on nature connectedness, cognitive flexibility, and psychological well-being.<br/><img src='/images/TreeFS.png'>"
collection: portfolio
permalink: /projects/portfolio-what-is-it-like-to-be-a-tree/
---

*Medialogy MSc, 8th Semester, Aalborg University Copenhagen, Spring 2026. In collaboration with the Augmented Cognition Lab at Aalborg University (Copenhagen).*

An embodied virtual reality experience designed to simulate mild altered states of consciousness through non-human embodiment and respiration-driven biofeedback. Participants inhabit the role of a tree within a responsive forest ecosystem: their breathing, captured via a piezoelectric chest belt, sends electrical-like pulses through a mycorrhizal root network that nourishes the surrounding saplings and drives the growth of the entire forest. The design is grounded in phenomenological and enactivist theory — rather than simulating what a tree literally perceives, it maps tree physiology onto the participant's own breath and renders it through an applied-hallucination visual aesthetic.

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:2em 0;">
  <iframe src="https://www.youtube.com/embed/sC5Dx3CzmZ8" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="What Is It Like To Be a Tree — playthrough"></iframe>
</div>

## Theoretical framing

The project is situated at the intersection of altered states of consciousness research, VR embodiment, and phenomenological theory. Altered states safely induced through meditation, breathwork, or psychedelics are associated with increased cognitive flexibility, nature connectedness, and relational awareness — but access to these states is constrained by health, training, and social context. VR has recently shown potential to simulate mild ASC-like effects in a controlled setting.

The experience draws on von Uexküll's concept of Umwelt to avoid reducing the tree's perceptual world to anthropomorphic analogues, instead using metaphorical mappings that make the tree's Umwelt emerge through the participant's own bodily register. Merleau-Ponty's embodied perception frames breathing as a causal act rather than a passive sensory input. Ihde's postphenomenology motivates a deliberate "controlled breakdown" of perceptual readiness-to-hand, placing participants in a liminal space between embodied familiarity and alterity. The enactivist framework of Varela et al. shapes the system's sensorimotor loop, where the mediating technology does not stand between subject and world but shapes the cognitive dynamics of enaction. Nagel's limits of cross-species imagination inform the design decision to leave the perceptual gap open rather than resolving it into didactic explanation.

## Implementation

The system architecture connects a BioSignalsplux Piezo-Electric Respiration sensor (wearable chest belt) via Bluetooth to OpenSignals, which streams normalized respiration values into Unity via LSL4Unity. The live breath state drives three parallel output channels: environment, visuals, and sound.

**Environment:** A single procedural low-poly tree model built in Blender, rigged with an armature for bone-scaled branch growth, is instanced across the forest. A central controller activates trees by distance, creating a wave-like outward growth effect; distant trees receive delayed respiration data so that the participant's breath gradually propagates restoration through the ecosystem. Exhalation increases animation speed.

**Visual effects:** A custom full-screen URP post-processing shader applies pixelation, posterization, and procedural noise; scene brightness is modulated in real time by respiration amplitude. A custom skybox shader produces animated kaleidoscopic effects through dynamic cubemap distortion and color modulation. Tree bark textures were generated in TouchDesigner and applied via sprite sheet flipbook shaders. The mycorrhizal root network uses a custom emissive shader that pulses green light along root geometry during exhalation.

**Sound:** A Pure Data patch receives breath input via OSC from Unity. Two streams track raw respiration and inhale/exhale direction independently, routing to separate synth engines built from Amplitude and Frequency Modulation. Slow arpeggios and generative melodies accompany exhalation; additional synth layers activate over time, mirroring the growing forest. All sound levels are mapped to breath amplitude, producing a slow, serene ambient soundscape.

The experience follows a cyclical narrative loop: seed phase → gradual growth into tree embodiment → breathing interaction → culmination of forest growth → return to seed. Unity's Timeline system coordinates player movement, lighting transitions, and environmental events with smooth animation blending to avoid abrupt scene changes.

## Study design and results

A pre-design UX survey (n = 22) informed visual and interaction decisions: participants were most receptive to seeing the world from a non-human perspective and preferred stylized over photorealistic aesthetics; experiencing the body as non-human was the least comfortable option, leading the design toward incidental embodiment through breath rather than explicit body transformation.

The evaluation used an A/B design with 40 participants (14 female, 26 male; mean age 24.83). The VR group experienced the simulation and completed a post-questionnaire; the control group completed only the questionnaire. Measures used the Extended Inclusion of Nature in Self scale (EINS), a shortened Cognitive Flexibility Inventory (CFI), and a shortened PANAS, implemented in PsychoPy.

Independent-samples t-tests found no significant differences between conditions on any outcome (all p > .09). A MANOVA revealed no significant multivariate effect of condition (Wilks' Λ = .871, p = .353), but prior VR experience showed a significant multivariate effect (Wilks' Λ = .671, p = .012), predicting both cognitive flexibility and negative affect. Qualitative feedback consistently reported high immersion, relaxation, and curiosity.

The findings point toward exposure dosage and sample size as primary limiting factors rather than design validity: related studies required more than twice the exposure duration (up to 18 minutes) to detect significant phenomenological changes. Prior VR familiarity emerges as a confound that future studies should control for, as it shapes novelty-related cognitive load independently of the experimental condition.
