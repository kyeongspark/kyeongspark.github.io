---
title: "Intensity-Dependent tACS Entrainment Effects in a Cortical Microcircuit: A Computational Study"
authors:
- me
- Hyeyeon Chung
- Hyeon Seo
- Sung Chan Jun
author_notes: []
date: "2026-01-31T00:00:00Z"

# Schedule page publish date (NOT publication's date).
publishDate: "2026-01-31T00:00:00Z"
math: true
# Publication type.
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]
share: false
# Publication name and optional abbreviated publication name.
publication: "*Scientific Reports, 16*(6825)"
publication_short: ""

# Summary. An optional shortened abstract.
summary: "A biophysical cortical microcircuit study using the NEURON simulator to investigate how individual neuronal morphology and network dynamics interact under tACS."

# tags:
# - tACS
# - Computational Neuroscience
# - Cortical Microcircuit
# - NEURON Simulator
# featured: false

links:
  - type: pdf
    url: https://doi.org/10.1038/s41598-026-37594-9
  - type: code
    url: https://modeldb.science/241165
  - type: poster
    url: "PosterScientificReports2026.pdf"

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ""
  focal_point: ""
  preview_only: false

projects: []
slides: ""
---

### 💡 Background & Motivation
Transcranial alternating current stimulation (tACS) is a powerful noninvasive neuromodulation technique capable of modulating disrupted neural oscillations and enhancing cognitive functions. However, its clinical efficacy remains highly debated due to substantial inter-individual variability in outcomes. 

At the microscopic level, this inconsistency stems from how individual neuronal morphology and complex synaptic networks interact with external electric fields (EFs). To bridge the gap between single-neuron biophysics and network-level dynamics, this study developed a morphologically realistic, synaptically connected cortical microcircuit model to elucidate the precise cellular and network mechanisms underlying tACS-induced neural entrainment.

---

### 🛠️ Methods & Microcircuit Architecture

We constructed a multi-compartment, columnar cortical microcircuit spanning layers 1 through 6 using the **NEURON simulation environment**.

{{< figure src="methods.png" title="Figure 1: Cortical Microcircuit Architecture. (A) Morphologies of biophysical human cortical neuron models. (B) Schematic representation of the microcircuit model. Line width denotes synaptic weight between the connected cells." lightbox="true" >}}

* **Biophysically Realistic Neuron Models:** Incorporated 5 distinct, detailed human cortical neuron models based on the Blue Brain Project: Layer 1 dense arborized neurogliaform cell (L1 NGC), Layer 2/3 pyramidal cell (L2/3 PC), Layer 4 large basket cell (L4 LBC), Layer 5 thick-tufted pyramidal cell (L5 PC), and Layer 6 tufted pyramidal cell (L6 PC).
* **Synaptic Connectivity:** Implemented 14 cell-type-specific excitatory (AMPA/NMDA) and inhibitory (GABA_A/GABA_B) synaptic connections with data-driven weights and kinetics derived from the Blue Brain Project, rather than using randomized inputs.
* **Ongoing Endogenous Oscillations:** Simulated realistic background brain rhythms by applying stochastic Poisson-driven inputs to generate robust Alpha-band (10 Hz) and Theta-band (5 Hz) oscillations.
* **tACS Setup:** Generated a uniform electric field within a 3D cubic volume using COMSOL Multiphysics, applying computed extracellular potentials directly to neuronal segments through cable theory.

---

### 📊 Computational Metrics

| Analysis Level | Metric Used | Major Scientific Outcome |
| :--- | :--- | :--- |
| **Network Level** | LFP Cross Correlation & Phase Coherence | tACS induces immediate, state-dependent phase alignment and synchronization across the microcircuit. |
| **Cellular Level** | Normalized Firing Rate | Total spike quantity remains unchanged (<1%), confirming subthreshold timing modulation. |
|  | PLV & PPC | Pyramidal cells entrain effectively based on dendritic morphology; Interneurons exhibit high phase variability governed by synaptic connectivity. |

---

### 🌟 Key Findings

{{< figure src="results1.png" title="Figure 2: Neural entrainment across tACS intensities at the cellular level. (A) Normalized firing rate across different tACS intensities for alpha (left) and theta (right) endogenous oscillations. (B) PLV corresponding to tACS intensity in alpha (left) and theta (right) oscillations. (C) Scatter plot of squared PLV versus PPC for alpha (left) and theta (right) endogenous oscillations. (D) PLV and preferred phase across tACS intensity levels for alpha (orange) and theta (green) oscillations, with darker shades indicating stronger stimulation intensities. Spiking phases recorded during the tACS period from 20 independent simulations were aggregated to calculate a single PLV and preferred phase for each neuron type and tACS amplitude." lightbox="true" >}}

#### 1️⃣ Phase Modulation Without Altering Firing Rates
* Across a wide range of stimulation intensities, tACS did not significantly alter the overall firing rates of the neurons, with fluctuations remaining strictly **below 1%** for both oscillatory conditions.
* Instead, it precisely modulated the **timing of neural spikes**, forcing them to preferentially align with specific phases of the external tACS waveform, replicating robust phase-locking effects observed in vivo and in vitro.

#### 2️⃣ Morphology-Driven vs. Network-Driven Sensitivity
* **Pyramidal Neurons:** Exhibited high sensitivity to external EFs due to their elongated, directionally aligned dendritic structures, showing a strong, highly linear correlation ($R^2 > 0.9$) between their Phase-Locking Value (PLV) and tACS intensity above 0.4 mA.
* **Interneurons:** Showed much lower and highly variable direct entrainment ($R^2 < 0.1$) due to their compact, radial morphologies. Their phase alignment was primarily driven indirectly by network-level synaptic interactions from surrounding activated pyramidal cells rather than direct electric field effects.

#### 3️⃣ Dual Effects on Network Synchronization
* The network response revealed a non-linear relationship based on stimulation intensity.
* When endogenous oscillations were out of phase with the tACS waveform, **low-intensity stimulation (<0.4 mA)** transiently disrupted or desynchronized ongoing neural rhythms.
* Conversely, **high-intensity stimulation (≥1 mA)** completely dominated network dynamics, driving robust, stable phase convergence toward the rising anodic phase of the waveform.

---

### 🎯 Research Significance & Clinical Applications
* **Morphology and Network Interplay:** By integrating realistic neuronal morphologies and synaptic connectivity into a cortical microcircuit, this framework uniquely captures the complex interplay between individual cell structures and ongoing network dynamics under tACS.
* **Cell Type-Specific Sensitivity:** The findings demonstrate that tACS effects are highly cell-type specific, revealing that pyramidal neurons are directly driven by morphology-dependent electric field sensitivity whereas interneurons are primarily modulated via network-level synaptic interactions.
* **Optimization of Stimulation Parameters:** This model provides a mechanistic foundation to optimize stimulation parameters, such as intensity and phase alignment, for precise neuromodulation to either counteract pathological synchrony or enhance beneficial synchrony associated with cognitive functions.
