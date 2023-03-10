# awesome-controllable-stable-diffusion

A Survey of Controllable Editing Stable Diffusion

## Paper List

### Cones: Concept Neurons in Diffusion Models for Customized Generation ([arxiv](https://arxiv.org/abs/2303.05125), 9 Mar 2023)

1. Problem: Can modern deep neural networks exhibit behavior patterns similar to the human brain's response to semantic features of presented stimuli with different neurons?
2. Solution: This paper identifies a small cluster of neurons in a diffusion model corresponding to a particular subject and calls them concept neurons. These neurons demonstrate magnetic properties in interpreting and manipulating generation results, and concatenating multiple clusters of concept neurons can generate all related concepts in a single image
3. Insight: The concept neurons can be identified by statistics of network gradients to a stimulation connected with the given subject and can reduce storage consumption by 90% compared to previous subject-driven generation methods. Extensive qualitative and quantitative studies on diverse datasets confirm the effectiveness and efficiency of the proposed approach.
4. Limitation: The approach may be limited to generating up to four different subjects in a single image.

### Zeroth-Order Optimization Meets Human Feedback: Provable Learning via Ranking Oracles ([arixv](https://arxiv.org/abs/2303.03751), 7 Mar 2023)

1. Problem: Objective function is a black-box and can only be evaluated through a ranking oracle.
2. Solution: ZO-RankSGD, a zeroth-order optimization algorithm with a new rank-based random estimator for the descent direction, is proposed to solve the problem.
3. Insight: ZO-RankSGD can be applied to the policy search problem in reinforcement learning when only a ranking oracle of the episode reward is available, making it a promising alternative to existing Reinforcement Learning with Human Feedback (RLHF) methods.
4. Limitation: The effectiveness of ZO-RankSGD is demonstrated only in improving the quality of images generated by a diffusion generator.

### X&Fuse: Fusing Visual Information in Text-to-Image Generation ([arxiv](https://arxiv.org/abs/2303.01000), 2 Mar 2023)

1. Problem: Generating images from text while incorporating visual information.
2. Solution: X&Fuse approach that conditions on visual information in three scenarios: Retrieve&Fuse, Crop&Fuse, and Scene&Fuse.
3. Insight: X&Fuse is an effective, easy-to-adapt, simple, and general approach for scenarios in which the model may benefit from additional visual information.

### ELITE: Encoding Visual Concepts into Textual Embeddings for Customized Text-to-Image Generation ([arxiv](https://arxiv.org/abs/2302.13848), 27 Feb 2023)

1. Problem: Existing methods for customized text-to-image generation often rely on optimization-based approaches, which can be computationally intensive and memory-intensive.
2. Solution: The authors propose a learning-based encoder that consists of global and local mapping networks for fast and accurate concept customization. The global mapping network projects hierarchical image features into multiple words in the textual word embedding space, while the local mapping network injects encoded patch features into cross attention layers for additional details.
3. Insight: The proposed method enables high-fidelity inversion and robust editability of primary concepts while excluding irrelevant disturbances, with a significantly faster encoding process compared to prior optimization-based approaches.
4. Limitation: The limitations of the proposed method are not explicitly stated in the abstract.

### Encoder-based Domain Tuning for Fast Personalization of Text-to-Image Models ([arxiv](https://arxiv.org/abs/2302.12228), 23 Feb 2023)

1. Problem: Current text-to-image personalization approaches have limitations in terms of lengthy training times, high storage requirements, or loss of identity.
2. Solution: Encoder-based domain tuning approach by underfitting on a large set of concepts from a given domain, employing an encoder and regularized weight-offsets for the text-to-image model.
3. Insight: Underfitting on a large set of concepts from a given domain improves generalization and creates a model that is more amenable to quickly adding novel concepts from the same domain.
4. Limitation: The proposed approach may not generalize well to domains with highly diverse or unrelated concep

### Controlled and Conditional Text to Image Generation with Diffusion Prior ([arxiv](https://arxiv.org/abs/2302.11710), 23 Feb 2023)

1. Problem: Limited exploration of the potential of the Diffusion Prior approach in generating images from text, and lack of control over domain-specific generation and color conditioning.
2. Solution: Explore the capabilities of the Diffusion Prior and use it in a memory and compute efficient way to constrain generation to a specific domain, and train it with additional conditional information such as color histogram to further control generation.
3. Insight: The Diffusion Prior can be used as an intermediate CLIP representation to generate images from text and provides advantages in domain-specific generation and color conditioning.

### Composer: Creative and Controllable Image Synthesis with Composable Conditions ([arxiv](https://arxiv.org/abs/2302.09778), 20 Feb 2023)

1. Problem: Limited controllability in generative models for image synthesis.
2. Solution: Composer, a generative model that offers flexible control of output images through compositionality and decomposition of representative factors.
3. Insight: Rich intermediate representations can be used as composable elements to exponentially increase the design space for customizable content creation.

### T2I-Adapter: Learning Adapters to Dig out More Controllable Ability for Text-to-Image Diffusion Models ([arxiv](https://arxiv.org/abs/2302.08453), 16 Feb 2023)

1. Problem: Text-to-image (T2I) models have strong generative ability but are limited in terms of flexible and accurate structure control when relying solely on text prompts.
2. Solution: The authors propose to learn T2I-Adapters to align internal knowledge in T2I models with external control signals, allowing for more granular generation control and editing effects.
3. Insight: T2I models have implicit knowledge that can be explicitly utilized through the use of T2I-Adapters, which can be trained for various conditions and have practical properties such as composability and generalization ability.
4. Limitation: This is a technical report, not a peer-reviewed paper, and the proposed method's limitations are not explicitly stated

### MultiDiffusion: Fusing Diffusion Paths for Controlled Image Generation ([arxiv](https://arxiv.org/abs/2302.08113), 16 Feb 2023)

1. Problem: The user controllability of generated images and fast adaptation to new tasks are still open challenges in text-to-image generation with diffusion models, requiring costly and time-consuming re-training or ad-hoc adaptations.
2. Solution: The authors propose MultiDiffusion, a unified framework that enables versatile and controllable image generation using a pre-trained text-to-image diffusion model without further training or fine-tuning. Their approach involves an optimization task that binds together multiple diffusion generation processes with shared parameters or constraints.
3. Insight: MultiDiffusion can generate high-quality and diverse images that adhere to user-provided controls such as aspect ratio and spatial guiding signals ranging from segmentation masks to bounding boxes.

### Universal Guidance for Diffusion Models ([arxiv](https://arxiv.org/abs/2302.07121), 14 Feb 2023)

1. Problem: Diffusion models are typically trained to accept a particular form of conditioning, such as text, and cannot be conditioned on other modalities without retraining.
2. Solution: The authors propose a universal guidance algorithm that allows diffusion models to be controlled by any guidance modality without the need for retraining specific components.
3. Insight: The algorithm successfully generates high-quality images using guidance functions such as segmentation, face recognition, object detection, and classifier signals.

### Adding Conditional Control to Text-to-Image Diffusion Models ([arxiv](https://arxiv.org/abs/2302.05543), 10 Feb 2023)

1. Problem: Large diffusion models like Stable Diffusion lack the ability to incorporate additional input conditions such as edge maps, segmentation maps, keypoints, etc.
2. Solution: The authors present ControlNet, a neural network structure that can control pretrained large diffusion models to support additional input conditions.
3. Insight: ControlNet learns task-specific conditions in an end-to-end way, even when the training dataset is small, and can be trained on personal devices.

### MaskSketch: Unpaired Structure-guided Masked Image Generation ([arxiv](https://arxiv.org/abs/2302.05496), 10 Feb 2023)

1. Problem: Current conditional image generation methods have limited control over the generation result due to conditioning only on labels or text prompts.
2. Solution: MaskSketch introduces spatial conditioning of the generation result using a guiding sketch as an extra conditioning signal during sampling, utilizing a pre-trained masked generative transformer and intermediate self-attention maps to enable structure-guided generation.
3. Insight: Intermediate self-attention maps of a masked generative transformer encode important structural information of the input image, such as scene layout and object shape.

### Zero-shot Image-to-Image Translation ([arxiv](https://arxiv.org/abs/2302.03027), 6 Feb 2023)

1. Problem: Difficulties in editing real images using text prompts due to the challenge of accurately describing visual details and unexpected changes in unwanted regions.
2. Solution: pix2pix-zero, an image-to-image translation method that automatically discovers editing directions and preserves the content of the original image without manual prompting. It uses cross-attention guidance to retain the cross-attention maps of the input image throughout the diffusion process and can directly use existing pre-trained text-to-image diffusion models.
3. Insight: Discovering editing directions and retaining cross-attention maps can improve image editing while preserving the content structure.

### Design Booster: A Text-Guided Diffusion Model for Image Translation with Spatial Layout Preservation ([arxiv](https://arxiv.org/abs/2302.02284), 5 Feb 2023)

1. Problem: Maintaining spatial structure and high-quality content in image translation with diffusion models.
2. Solution: Learning a layout-aware image condition and a text condition in a new domain during training, and using them flexibly as conditions in the inference stage.
3. Insight: Co-encoding images and text can help maintain spatial structure and high-quality content in image translation, while giving users more flexible control over layout and content.

### SEGA: Instructing Diffusion using Semantic Dimensions ([arxiv](https://arxiv.org/abs/2301.12247), 28 Jan 2023)

1. Problem: Achieving one-shot generation of high-fidelity images aligned with user intent is nearly impossible with current text-to-image diffusion models, leaving users with little semantic control.
2. Solution: SEGA (Semantic guidance) allows for flexible steering of the diffusion process along semantic directions, enabling subtle and extensive edits, changes in composition and style, and optimization of overall artistic conception.
3. Insight: Interacting with the diffusion process along semantic dimensions enables greater user control and opens up new possibilities for generating high-quality images from text.

### GLIGEN: Open-Set Grounded Text-to-Image Generation ([arxiv](https://arxiv.org/abs/2301.07093), 17 Jan 2023)

1. Problem: Existing text-to-image diffusion models lack controllability due to reliance on text input alone.
2. Solution: GLIGEN proposes a novel approach that combines grounding inputs with pre-trained text-to-image diffusion models to achieve open-world grounded text-to-image generation with caption and bounding box condition inputs.
3. Insight: GLIGEN's gated mechanism preserves the vast concept knowledge of the pre-trained model and enables it to generalize well to novel spatial configurations and concepts, outperforming existing supervised layout-to-image baselines.

### Imagen Editor and EditBench: Advancing and Evaluating Text-Guided Image Inpainting ([arxiv](https://arxiv.org/abs/2212.06909), 13 Dec 2022)

1. Problem: Generating faithful edits to input text prompts while consistent with input images.
2. Solution: Imagen Editor, a cascaded diffusion model that uses object detectors to propose inpainting masks during training and conditions on the original high-resolution image to capture fine details.
3. Insight: Object-masking during training leads to across-the-board improvements in text-image alignment and human evaluation on EditBench shows Imagen Editor outperforms DALL-E 2 and Stable Diffusion.

### SmartBrush: Text and Shape Guided Object Inpainting with Diffusion Model ([arxiv](https://arxiv.org/abs/2212.05034), 9 Dec 2022)

1. Problem: Traditional image inpainting methods lack flexibility and cannot generate novel content.
2. Solution: The proposed SmartBrush model enables more precise control over inpainted content through both text and shape guidance. It incorporates a novel training and sampling strategy to preserve the background texture and uses a multi-task training strategy to leverage more data.
3. Insight: Combining text and shape guidance provides more flexible and useful controls over the inpainted content, enabling the generation of more novel content

### Training-Free Structured Diffusion Guidance for Compositional Text-to-Image Synthesis ([arxiv](https://arxiv.org/abs/2212.05032), 9 Dec 2022)

1. Problem: The attribution-binding and compositional capabilities of large-scale diffusion models for text-to-image synthesis involving multiple objects are still challenging issues.
2. Solution: Incorporating linguistic structures with the diffusion guidance process based on the controllable properties of manipulating cross-attention layers in diffusion-based T2I models to improve compositional skills.
3. Insight: Keys and values in cross-attention layers have strong semantic meanings associated with object layouts and content, which can be better preserved by manipulating the cross-attention representations based on linguistic insights.

### Multi-Concept Customization of Text-to-Image Diffusion ([arxiv](https://arxiv.org/abs/2212.04488), 8 Dec 2022)

1. Problem: Generative models are limited in their ability to synthesize instantiations of new concepts.
2. Solution: Custom Diffusion, an efficient method for augmenting existing text-to-image models, allows for the quick acquisition of new concepts and the composition of multiple new concepts together.
3. Insight: Optimizing only a few parameters in the text-to-image conditioning mechanism is sufficiently powerful to represent new concepts while enabling fast tuning.

### Sketch-Guided Text-to-Image Diffusion Models ([arxiv](https://arxiv.org/abs/2211.13752), 24 Nov 2022)

1. Problem: Lack of control handles to guide spatial properties of synthesized images by text-to-image models.
2. Solution: Introduce a universal approach using a Latent Guidance Predictor (LGP) to guide a pretrained text-to-image diffusion model with a spatial map from another domain during inference time, without requiring a dedicated model or specialized encoder for the task.
3. Insight: The per-pixel training of LGP offers flexibility and locality, allowing the technique to perform well on out-of-domain sketches, including free-hand style drawings

### Paint by Example: Exemplar-based Image Editing with Diffusion Models ([arxiv](https://arxiv.org/abs/2211.13227), 23 Nov 2022)

1. Problem: Lack of precise control in language-guided image editing.
2. Solution: Exemplar-guided image editing using self-supervised training, information bottleneck, and strong augmentations to avoid artifacts, arbitrary shape mask for the exemplar image, and classifier-free guidance.
3. Insight: Disentangling and re-organizing source image and exemplar can enable more precise control in image editing.

### Plug-and-Play Diffusion Features for Text-Driven Image-to-Image Translation ([arxiv](https://arxiv.org/abs/2211.12572), 22 Nov 2022)

1. Problem: Providing users with control over generated images from text-to-image models for real-world content creation tasks.
2. Solution: A new framework for image-to-image translation that uses a pre-trained text-to-image diffusion model and fine-grained control over spatial features and self-attention to generate a new image that complies with a target text prompt, while preserving the semantic layout of a guidance image.
3. Insight: Spatial features and self-attention can be manipulated to achieve fine-grained control over generated structure, and guidance images can be used without any training or fine-tuning.

### DreamArtist: Towards Controllable One-Shot Text-to-Image Generation via Contrastive Prompt-Tuning ([arxiv](https://arxiv.org/abs/2211.11337), 21 Nov 2022)

1. Problem: Current text-to-image generation models struggle to synthesize diverse and high-quality images without distortion and artifacts, and suffer from low controllability when new concepts or styles are introduced.
2. Solution: The DreamArtist method employs contrastive prompt-tuning, using both positive and negative embeddings as pseudo-words to train the model jointly. The positive embedding learns characteristics in the reference image to drive diversified generation, while the negative embedding rectifies mistakes and inadequacies from the positive embedding in reverse.
3. Insight: The contrastive prompt-tuning approach allows the model to learn not only what is correct but also what should be avoided, leading to higher image quality, diversity, and controllability.

### Diffusion-Based Scene Graph to Image Generation with Masked Contrastive Pre-Training ([arxiv](https://arxiv.org/abs/2211.11138), 21 Nov 2022)

1. Problem: Difficulty in aligning scene graphs with images due to manually crafted scene layouts.
2. Solution: Pre-train an encoder to learn scene graph embeddings by optimizing their alignment with images using masked autoencoding and contrastive loss, and build a latent diffusion model to generate images from scene graphs.
3. Insight: Learning scene graph embeddings directly from images improves compliance between generated images and original scene graphs.

### Null-text Inversion for Editing Real Images using Guided Diffusion Models ([arxiv](https://arxiv.org/abs/2211.09794), 17 Nov 2022)

1. Problem: Current text-guided diffusion models provide powerful image generation capabilities, but editing real images using text only requires inverting the image with a meaningful text prompt into the pretrained model's domain.
2. Solution: The authors introduce an accurate inversion technique consisting of pivotal inversion for diffusion models and NULL-text optimization to enable intuitive text-based modification of real images.
3. Insight: Direct inversion is inadequate on its own, but provides a good anchor for optimization. Modifying only the unconditional textual embedding allows for prompt-based editing without tuning the model's weights.

### InstructPix2Pix: Learning to Follow Image Editing Instructions ([arxiv](https://arxiv.org/abs/2211.09800), 17 Nov 2022)

1. Problem: Editing images from human instructions is a challenging task that requires a large dataset of training examples.
2. Solution: InstructPix2Pix is a conditional diffusion model that learns to follow human instructions to edit images quickly and without per example fine-tuning or inversion.
3. Insight: InstructPix2Pix is trained on a large dataset of image editing examples generated by combining the knowledge of two large pretrained models, a language model (GPT-3) and a text-to-image model (Stable Diffusion).

### Direct Inversion: Optimization-Free Text-Driven Real Image Editing with Diffusion Models ([arxiv](https://arxiv.org/abs/2211.07825), 15 Nov 2022)

1. Problem: Current methods of text-guided real image editing require optimization or fine-tuning, multiple views, and often struggle with preserving real image identity, semantic coherence, and faithfulness to text guidance.
2. Solution: The authors propose an optimization-free and zero fine-tuning framework called "Direct Inversion" that applies complex and non-rigid edits to a single real image via a text prompt.
3. Insight: By using widely-available generic pre-trained text-to-image diffusion models and multiple intuitively configurable hyperparameters, the proposed method can modulate pose, scene, background, style, color, and even racial identity in an extremely flexible manner through a single target text.

### Imagic: Text-Based Real Image Editing with Diffusion Models ([arxiv](https://arxiv.org/abs/2210.09276), 17 Oct 2022)

1. Problem: Existing text-based image editing methods are limited to specific editing types or synthetic images, and often require multiple input images.
2. Solution: "Imagic" is a method that allows for complex text-guided semantic edits on a single real image, without the need for additional inputs. It leverages a pre-trained text-to-image diffusion model to produce a text embedding that aligns with both the input image and the target text.
3. Insight: This is the first time that complex text-based edits can be applied to a single real image without the need for additional inputs. The method can change the posture and composition of objects within the image while preserving its original characteristics.

### UniTune: Text-Driven Image Editing by Fine Tuning an Image Generation Model on a Single Image ([arxiv](https://arxiv.org/abs/2210.09477), 17 Oct 2022)

1. Problem: Current image editing methods require additional inputs, such as masks or sketches, and lack intuitive art-direction.
2. Solution: UniTune uses a single image and a textual edit description to fine-tune a large text-to-image diffusion model, allowing expressive manipulations while maintaining fidelity to the input image.
3. Insight: The right choice of parameters enables fine-tuning of large-scale models on a single image.

### Unifying Diffusion Models' Latent Space, with Applications to CycleDiffusion and Guidance ([arxiv](https://arxiv.org/abs/2210.05559), 11 Oct 2022)

1. Problem: The commonly-adopted formulation of the latent code of diffusion models is a sequence of gradually denoised samples, which can limit their flexibility and applicability.
2. Solution: This paper provides an alternative, Gaussian formulation of the latent space of various diffusion models, as well as an invertible DPM-Encoder that maps images into the latent space.
3. Insight: The proposed formulation allows for intriguing consequences, such as the emergence of a common latent space from two diffusion models trained independently on related domains, and the use of large-scale text-to-image diffusion models as zero-shot image-to-image editors.

### DreamBooth: Fine Tuning Text-to-Image Diffusion Models for Subject-Driven Generation ([arxiv](https://arxiv.org/abs/2208.12242), 25 Aug 2022)

1. Problem: Existing text-to-image models lack the ability to personalize image synthesis based on a given set of reference images of a subject.
2. Solution: The authors propose a fine-tuning approach that binds a unique identifier with a specific subject, allowing for fully-novel photorealistic images of the subject contextualized in different scenes to be synthesized.
3. Insight: The authors leverage the semantic prior embedded in the model with a new autogenous class-specific prior preservation loss, enabling the synthesis of subjects in diverse scenes, poses, views, and lighting conditions that do not appear in the reference images.

### Prompt-to-Prompt Image Editing with Cross Attention Control ([arxiv](https://arxiv.org/abs/2208.01626), 2 Aug 2022)

1. Problem: Text-driven image editing models struggle to preserve the original image while making small modifications to the text prompt.
2. Solution: A prompt-to-prompt editing framework that controls edits with text only, using cross-attention layers to control the relation between the spatial layout of the image and each word in the prompt.
3. Insight: Cross-attention layers are key to controlling the relationship between image layout and text prompts.

### An Image is Worth One Word: Personalizing Text-to-Image Generation using Textual Inversion ([arxiv](https://arxiv.org/abs/2208.01618), 2 Aug 2022)

1. Problem: How can we use language-guided models to generate images of specific unique concepts, modify their appearance, or compose them in new roles and novel scenes?
2. Solution: The authors present a simple approach that allows creative freedom in text-to-image generation. Using only 3-5 images of a user-provided concept, they learn to represent it through new "words" in the embedding space of a frozen text-to-image model. These "words" can be composed into natural language sentences, guiding personalized creation in an intuitive way.
3. Insight: The authors find evidence that a single word embedding is sufficient for capturing unique and varied concepts, and demonstrate that their approach can more faithfully portray concepts across a range of applications and tasks.
