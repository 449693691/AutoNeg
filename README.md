# AutoNeg
利用 XTuner 微调个人小助手，从Stable Diffusion的大量提示词数据集中，训练出能够根据已有的正面提示词，全自动补全负面词的AI。
本项目基于 https://github.com/InternLM/InternLM 的7B模型构建。

![架构图1](https://github.com/user-attachments/assets/64ffe37d-b68f-4fa5-9394-95d91bae7aed)

AutoNeg Architecture Overview
AutoNeg is an AI model architecture designed to automatically generate negative prompts. Its purpose is to fine-tune XTuner, based on a large dataset of prompts from Stable Diffusion, to train an intelligent assistant capable of automatically completing negative prompts. This project is built on the InternLM 7B model.

1. Background and Need
In the field of generative AI, prompt design is crucial for the quality of generated content. Positive prompts guide the model to produce desired content, while negative prompts are used to suppress specific, undesired content, thereby improving the accuracy of the output. However, manually designing and completing negative prompts is time-consuming and requires significant expertise. Therefore, the design goal of AutoNeg is to automatically generate negative prompts corresponding to positive ones, thus improving efficiency and the quality of generated results.

2. Architecture Overview
The core architecture of AutoNeg revolves around fine-tuning XTuner using a large dataset of prompts from the Stable Diffusion model. This architecture is based on the InternLM 7B model, leveraging its powerful language understanding and generation capabilities to analyze positive prompts and automatically generate negative ones.

Dataset Collection and Preprocessing: During the training phase, the system first extracts a large dataset of prompts from the Stable Diffusion model. These prompts cover various scenarios, styles, content requirements, etc., ensuring that the model can fully learn the correspondence between positive and negative prompts during training. The preprocessing steps include data cleaning, labeling, and constructing positive-negative prompt pairs for training.

XTuner Fine-Tuning: XTuner, as a fine-tuning tool, is used to optimize the pre-trained model for specific tasks. AutoNeg fine-tunes the InternLM 7B model using XTuner to adapt it to the task of generating negative prompts. This process not only considers the semantics of the positive prompts but also helps the model learn to generate logically and semantically appropriate negative prompts through examples of negative prompts in the training data.

Model Training: On the basis of fine-tuning, the model is trained on a large number of positive and negative prompt pairs, enabling it to understand the underlying requirements of positive prompts and generate corresponding negative prompts. During training, the model’s loss function primarily focuses on the accuracy and validity of the generated negative prompts, ensuring that the output effectively suppresses undesired content.

Automatic Prompt Completion: During the inference phase, users only need to provide positive prompts, and AutoNeg will automatically generate the corresponding negative prompts. This functionality greatly simplifies the prompt design process, especially in scenarios that require high precision in the generated content, such as image generation, text generation, etc.

3. Technical Advantages
AutoNeg's architectural design incorporates an advanced pre-trained model (InternLM 7B) and an effective fine-tuning strategy (XTuner), ensuring its excellent performance in prompt generation tasks. The main technical advantages of this architecture include:

Efficient Negative Prompt Generation: By training on a large dataset of prompts, the model can quickly generate negative prompts corresponding to positive ones, significantly enhancing the control over the generated content.
Model Scalability: Based on the InternLM 7B model, AutoNeg can easily scale to other generation tasks. With a simple fine-tuning process via XTuner, it can adapt to different prompt requirements.
Simplified User Experience: Users only need to provide positive prompts, and the system can generate reasonable negative prompts, greatly reducing the complexity and difficulty of design.
4. Application Scenarios
The AutoNeg architecture is suitable for various generation tasks that require prompt design, such as text generation, image generation, dialogue systems, etc. Especially in content creation, advertisement generation, and creative design, AutoNeg can help users quickly generate high-quality, low-noise output results.

In summary, AutoNeg, through its efficient architectural design and advanced technology application, provides an intelligent solution for prompt generation, significantly enhancing the accuracy of generated content and the user experience.
