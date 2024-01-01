---
title: Differentiable Diffusion MRI Simulator
summary: Simulating Diffusion Magnetic Resonance Imaging signal generation in a differentiable way.
tags:
  - Medical Imaging
  - Deep Learning
date: '2023-02-01'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Diffusion MRI
  focal_point: Smart

# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

Diffusion MRI (Magnetic Resonance Imaging) is a non-invasive imaging technique that plays a crucial role in the study of the brain's microstructural organization. Unlike traditional MRI, diffusion MRI focuses on the diffusion process of water molecules in biological tissues, particularly in the neural pathways of the brain. This unique approach allows for the detailed mapping of the diffusion process of molecules, primarily water, providing insights into the cellular structure of tissues. By measuring the direction and magnitude of water molecule movement, diffusion MRI can reveal important details about tissue architecture, which is particularly useful in neural imaging.

The primary application of diffusion MRI is in the field of medical imaging, especially in understanding and diagnosing neurological disorders. It is exceptionally valuable in the early detection of stroke, where it can identify areas of the brain with restricted blood flow. Additionally, diffusion MRI is instrumental in brain research, aiding in the study of diseases like Alzheimer's and multiple sclerosis, as well as in brain development research. The technique's ability to visualize and track the pathways of white matter in the brain has also made it a vital tool in pre-surgical planning for brain tumor patients, as it helps surgeons avoid critical areas of the brain during operations.

I developed an innovative framework designed to enhance the acquisition and interpretation of diffusion MRI signals, specifically tailored for brain imaging. This framework is unique in its ability to make the process of acquiring diffusion MRI signals from a predefined shape or mesh model of the brain fully differentiable. This means that the framework can adjust the parameters of the signal acquisition process in response to changes in the brain model, facilitating a more flexible and accurate representation of the brain's structure in the MRI data.

A remarkable feature of this framework is its capability to reverse-engineer the process. It can take a diffusion MRI signal and reconstruct the original mesh or 3D structure of the brain. This reverse functionality opens up new possibilities in medical imaging, allowing for the reconstruction of detailed brain models from MRI data. Such a capability is invaluable in medical research and diagnosis, providing insights into the brain's anatomy and potential abnormalities with enhanced precision.

To realize this, I implemented a sophisticated, physics-based simulator in Python. This simulator accurately replicates the core process of diffusion MRI signal acquisition for any given brain mesh. It is designed to mirror state-of-the-art models in this field, ensuring high fidelity and accuracy in the simulation results. By leveraging advanced computational techniques, this simulator serves as a critical component of the framework, enabling the precise modeling of diffusion processes as they occur in the brain's complex structure. This tool not only aids in the understanding of diffusion MRI signals but also enhances the ability to simulate various scenarios and conditions in a controlled digital environment, paving the way for breakthroughs in neuroimaging and related medical fields.