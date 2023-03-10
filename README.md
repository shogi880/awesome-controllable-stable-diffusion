# awesome-controllable-editing-SD

A Survey of Controllable Editing Stable Diffusion

## Papers

### Cones: Concept Neurons in Diffusion Models for Customized Generation ([arxiv](https://arxiv.org/abs/2303.05125))

1. Problem: Can modern deep neural networks exhibit behavior patterns similar to the human brain's response to semantic features of presented stimuli with different neurons?
2. Solution: This paper identifies a small cluster of neurons in a diffusion model corresponding to a particular subject and calls them concept neurons. These neurons demonstrate magnetic properties in interpreting and manipulating generation results, and concatenating multiple clusters of concept neurons can generate all related concepts in a single image
3. Insight: The concept neurons can be identified by statistics of network gradients to a stimulation connected with the given subject and can reduce storage consumption by 90% compared to previous subject-driven generation methods. Extensive qualitative and quantitative studies on diverse datasets confirm the effectiveness and efficiency of the proposed approach.✏
4. Limitation: The approach may be limited to generating up to four different subjects in a single image.
