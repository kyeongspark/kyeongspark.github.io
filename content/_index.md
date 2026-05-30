---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: true

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: markdown
    content:
      title: '📝 Publications & Proceedings'
      subtitle: ''
      text: |-
        ### Journal Publications
        1. **Park, K.**, Chung, H., Seo, H., & Jun, S. C. (2026). Intensity-dependent tACS entrainment effects in a cortical microcircuit: A computational study. *Scientific Reports*. <br> https://doi.org/10.1038/s41598-026-37594-9

        ### Conference Proceedings
        * **C1.** **Park, K.**, Chung, H., Im, C., & Jun, S. C. (2023). Entrainment effects upon synaptically connected microcircuit in transcranial alternating current stimulation. In *Proceedings of 2023 11th International IEEE/EMBS Conference on Neural Engineering (NER)*.
        * **C2.** **Park, K.**, Chung, H., Im, C., & Jun, S. C. (2021). Investigation of electric field direction sensitivity on cortical neuron activation. In *Proceedings of 2021 International Biomedical Engineering Conference (IBEC)*. (*Oral Presentation, Silver Prize in Best Paper Award*)

        ### Conference Abstracts
        * **A1.** **Park, K.**, & Jun, S. C. (2025). Computational investigation of neural entrainment induced by transcranial alternating current stimulation incorporating ongoing endogenous oscillations. At *6th International Brain Stimulation Conference*.
        * **A2.** **Park, K.**, Chung, H., Im, C., & Jun, S. C. (2023). Investigation of transcranial alternating current stimulation effects on an ongoing neural oscillation in a synaptically connected cortical microcircuit model. At *5th International Brain Stimulation Conference*.
    design:
      columns: '1'

  - block: markdown
    content:
      title: '🔍 Research Experience'
      subtitle: 'BioComputing Lab, GIST'
      text: |-
        **Research Assistant** (Advisor: Prof. Jun, Sung Chan)

        #### Sensorimotor Microcircuit Modeling (2022 - 2026)
        * Constructed a sensorimotor microcircuit by considering cell-to-cell synaptic connections, referred to the Blue Brain Project.
        * Stimulated morphologically realistic neurons in microcircuits by varying tACS intensity and frequency.
        * Quantified neuronal responses by measuring phase locking values regarding the tACS waveform.
        * *Frameworks:* NEURON, MATLAB, Python

        #### Single Neuron Modeling (2021)
        * Investigated how neural morphology influences sensitivity to electric fields during electrical brain stimulation.
        * Measured membrane polarization to calculate neuronal response to electric field orientation at both the neuron model's compartment and holistic levels.
        * *Frameworks:* NEURON, Python
    design:
      columns: '1'

  - block: markdown
    content:
      title: '💻 A.I. & Software Projects'
      subtitle: ''
      text: |-
        #### Image Search Application (Fall 2024)
        * Created an image search application in Python to guide students in applying vector databases as a Teaching Assistant for the Database Systems course.
        * Fetched images from Unsplash, embedded and stored them in ChromaDB, and performed similarity search to find matching reference images.

        #### Computer Vision Projects (Fall 2022)
        * **Image Harmonization:** Constructed a convolutional neural network using instance normalization (IN) and region-aware adaptive instance normalization (RAIN) for image harmonization with PyTorch.
        * **Structure from Motion:** Reconstructs three-dimensional structures from images taken from different viewpoints using camera calibration, feature extraction & matching, essential matrix estimation & decomposition, and triangulation with MATLAB.

        #### Artificial Intelligence Projects (Spring 2022)
        * Designed intelligent agents for the Pacman project in Python using adversarial search techniques, including Minimax and Alpha-Beta Pruning.
        * Developed a reinforcement learning agent for a competitive A.I. contest at UC Berkeley, optimizing decision-making in complex game environments.
    design:
      columns: '1'
---