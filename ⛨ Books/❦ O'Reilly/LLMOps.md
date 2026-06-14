> LLMOps.[Aryan].2025-O'Reilly

# Preface
**序**

I've lost count of how many times I've been asked, "What's the difference between an LLM/AI engineer and an LLMOps engineer?" It's one of those questions that keep popping up, whether I'm in a meeting, at a conference, or just grabbing coffee with someone in the field.

> 我已经记不清有多少次被问到：“LLM/AI 工程师和 LLMOps 工程师之间有什么区别？”无论是在会议中、在研讨会上，还是与业内人士喝咖啡时，这个问题总是反复出现。  

I used to start by explaining the technical distinctions between the roles. But over time, I realized the real issue: people don't fully grasp what it takes to keep the lights on with large language models (LLMs) in production over an extended period.

> 过去我通常会从技术角度解释这两个角色的差异。但随着时间的推移，我意识到真正的问题在于：人们并不完全理解在生产环境中长期维持大语言模型（LLM）稳定运行所需付出的努力。

As I write this in early 2025, the top models, techniques, and best practices are chang‐ ing every few days. Thus, very few people understand their complexity. Most people still think of operationalizing, or "Ops," as deployment, but in the LLM context, Ops is really about streamlining people, processes, and technology to make these models secure, robust, and reliable in production.

> 当我在 2025 年初写下这些文字时，顶尖的模型、技术和最佳实践每几天就会发生变化。因此，很少有人能理解它们的复杂性。大多数人仍然认为运营化，或称“Ops”，就是部署，但在 LLM 的语境下，Ops 实际上是指优化人员、流程和技术，使这些模型在生产环境中安全、稳健且可靠。

Enterprises and their human resource departments are scrambling to figure out what it all means for their teams and their projects, and in this book I have done my best to answer that question. This book isn't a tutorial on defining roles or how to build and deploy an LLM; while it touches on both of those topics, that isn't enough anymore. Once LLM-based applications are in production, someone has to keep them opti‐ mized, or they risk becoming overengineered solutions to simple problems or, worse, badly maintained houses of cards that crumble under high demand or a prompt injection attack.

> 企业及其人力资源部门正在努力弄清楚这一切对他们的团队和项目意味着什么，在这本书中，我已尽我所能回答了这个问题。这本书并非关于定义角色或如何构建和部署 LLM 的教程；虽然它涉及了这两个主题，但这已经不够了。一旦基于 LLM 的应用程序投入生产，就必须有人持续对其进行优化，否则它们有可能变成对简单问题的过度工程化解决方案，或者更糟的是，成为维护不善的纸牌屋，在高需求或提示注入攻击下崩溃。

In traditional software development (or Software 2.0), you wouldn't ask your lead developer to build and maintain your entire product. Software development engi‐ neers build, and reliability engineers maintain. Building and maintaining LLMs requires a similar separation of duties. In Software 3.0, LLM/AI engineers build and LLMOps engineers maintain!

> 在传统的软件开发（或 Software 2.0）中，你不会要求你的首席开发者去构建和维护整个产品。软件开发工程师负责构建，可靠性工程师负责维护。构建和维护 LLM 需要类似的职责分离。在 Software 3.0 中，LLM/AI 工程师负责构建，而 LLMOps 工程师负责维护！

Although machine learning operations (MLOps) are foundational to LLMOps, the MLOps skills that engineers gain from working on structured data and discriminative models don't fully translate to generative models.

> 尽管机器学习操作（MLOps）是 LLMOps 的基础，工程师从结构化数据和判别式模型工作中获得的 MLOps 技能并不完全适用于生成式模型。

In short, I'm writing this book to help you appreciate the unique aspects of the full LLM-based application lifecycle, from data engineering to model deployment and API design to monitoring, security, and resource optimization. I want to give you a strong foundation for making decisions as you build, maintain, and optimize your LLM data, models, and applications.

> 简而言之，我撰写这本书是为了帮助您理解基于 LLM 的完整应用程序生命周期的独特方面，从数据工程到模型部署，再到 API 设计，直至监控、安全和资源优化。我希望为您打下坚实的基础，以便在构建、维护和优化您的 LLM 数据、模型及应用程序时做出决策。

# **Ⅰ Introduction to Large Language Models**
**第一章 大型语言模型导论**

The rise in popularity of large language models (LLMs) is no accident; they're transforming how we interact with technology and pushing the boundaries of what machine learning models can do.

> 大型语言模型 (LLMs) 的流行并非偶然；它们正在改变我们与技术互动的方式，并推动机器学习模型的能力边界。

But here's the catch: while these models are impressive, scaling them up and managing them in production is no walk in the park. The leap from a research project to a fully fledged, reliable tool is filled with obstacles. We're talking about meeting enormous computational requirements, managing complex data, and ensuring that everything runs smoothly and securely whether you are self-hosting or using proprietary models.

> 但问题在于：尽管这些模型令人印象深刻，但将其扩大规模并在生产中管理绝非易事。从研究项目到成熟可靠工具的飞跃充满了障碍。这涉及到满足巨大的计算需求、管理复杂数据，以及确保无论您是自行托管还是使用专有模型，一切都能平稳安全地运行。

Before we dive into the nitty-gritty of LLM operations, it's important to understand why and how these models came to be. Knowing their origins and trajectory helps us appreciate the challenges we face when predicting their behaviors in production.

> 在深入探讨大语言模型（LLM）运行的具体细节之前，理解这些模型为何以及如何诞生至关重要。了解它们的起源和发展轨迹，有助于我们认识到在生产环境中预测其行为时所面临的挑战。

The evolution of LLMs reflects a series of incremental innovations, each addressing specific limitations of previous models. Early models were limited in scope and required extensive human input for even basic tasks. With advancements in architecture, such as the shift from recurrent neural networks (RNNs) to transformers, and the scaling of model sizes, LLMs have become more sophisticated. This evolution has brought about new challenges, such as managing massive amounts of data and ensuring efficient training processes.

> LLMs 的演进反映了一系列渐进式创新，每一项都针对先前模型的特定局限性。早期模型在范围上受限，即便是基本任务也需要大量人工输入。随着架构的进步——例如从循环神经网络（RNNs）向 Transformer 的转变，以及模型规模的扩展——LLMs 已变得更加复杂。这种演进也带来了新的挑战，例如管理海量数据以及确保高效的训练流程。

So, let's get into it.

> 那么，让我们深入探讨吧。


## 1. Some Key Terms
**一些关键术语**

There are three terms we should clarify before going any further:

> 在我们进一步讨论之前，有三个术语需要先澄清：

### 1) Foundation models
**基础模型**

Foundation models are advanced ML architectures that serve as the foundational building blocks for creating specialized models. They are pretrained on massive datasets, often consisting of text and recently including other data types such as code, images, audio, and video to develop general language comprehension and pattern recognition capabilities. These models encode statistical relationships and linguistic structures from their training data, forming a robust starting point for further fine-tuning. This fine-tuning tailors the models to specific tasks or applications, such as powering LLMs or other AI-driven solutions.

> 基础模型是先进的机器学习架构，作为创建专用模型的基础构建模块。它们在大规模数据集上进行预训练，这些数据集通常包含文本，近期还涵盖了代码、图像、音频和视频等其他数据类型，以培养通用的语言理解和模式识别能力。这些模型从训练数据中编码统计关系和语言结构，形成进一步微调的坚实基础。这种微调使模型能够针对特定任务或应用进行定制，例如驱动大型语言模型或其他人工智能驱动的解决方案。

### 2) Large language models
**大语言模型**

Large language models are specialized implementations of foundation models that have undergone additional training or fine-tuning to excel in specific languagebased tasks. These models are designed to predict and generate human-like text by analyzing and emulating natural language patterns. LLMs are highly versatile, supporting several natural language processing (NLP) applications such as text generation, sentiment analysis, language translation, question answering, and more. Popular use cases include chatbots, content creation, multilingual communication, data analysis, code generation, recommendation systems, and virtual assistants. "Enterprise Use Cases for LLMs" on page 13 will look at these applications in more detail.

> 大语言模型是基础模型的专门化实现，经过额外训练或微调后，在特定语言任务中表现卓越。这些模型通过分析和模仿自然语言模式，旨在预测并生成类人文本。大语言模型具有高度通用性，支持文本生成、情感分析、语言翻译、问答系统等多种自然语言处理应用。常见用例包括聊天机器人、内容创作、多语言交流、数据分析、代码生成、推荐系统和虚拟助手。第 13 页的“大语言模型企业用例”将更详细地探讨这些应用。

### 3) Generative AI models
**生成式人工智能模型**

Generative AI, or GenAI, refers to foundation models that have been trained specifically to generate content (images, text, audio, or video) based on the patterns and information they have learned. Some of the earliest generative AI models were generative adversarial networks (GANs), introduced in 2018; more recently, diffusion models, LLMs, and multimodal models like Gemini have become available. Given their generative nature, LLMs are considered a subset of generative AI models. In the context of LLMs, generative AI can generate text responses, creative stories, product descriptions, and more, based on input and learned patterns.

> 生成式人工智能，或者说 GenAI，指的是经过专门训练、能够根据所学模式和信息生成内容（图像、文本、音频或视频）的基础模型。最早的一些生成式人工智能模型是生成对抗网络（GANs），于 2018 年问世；最近，扩散模型、大语言模型（LLMs）以及像 Gemini 这样的多模态模型也已出现。鉴于其生成特性，大语言模型被视为生成式人工智能模型的一个子集。在大语言模型的语境下，生成式人工智能能够根据输入和所学模式生成文本回复、创意故事、产品描述等内容。

---

Confusingly, these three terms are frequently used interchangeably and loosely. For example, a popular image generation model, DALL-E, is better categorized as a gen‐ erative AI model than as a large language model. Recently, however, the DALL-E image generation functionality has been integrated into the ChatGPT chatbot, one of the most popular LLM applications. Therefore, a user can ask an LLM like ChatGPT to generate images. Over time, the language seems to be evolving toward calling all of these AI models, for simplicity.

> 令人困惑的是，这三个术语经常被混用和随意使用。例如，一个流行的图像生成模型 DALL-E，更适合归类为生成式 AI 模型，而非大型语言模型。然而，最近 DALL-E 的图像生成功能已被整合到 ChatGPT 聊天机器人中，这是最受欢迎的 LLM 应用之一。因此，用户可以要求像 ChatGPT 这样的 LLM 生成图像。随着时间的推移，为了简化，语言似乎正朝着将所有这类 AI 模型统称为 LLM 的方向演变。

## 2. Transformer Models
**Transformer 模型**

The transformer model, introduced by the paper "Attention Is All You Need," marked one of the biggest shifts in how we approach sequence-based tasks. Transformers have set new standards in how to handle language data.

> 由论文《Attention Is All You Need》提出的 Transformer 模型，标志着我们在处理序列任务方式上的重大转变之一。Transformer 为语言数据处理设立了全新标准。

Before transformers, the most popular solution for NLP tasks was recurrent neural networks. RNNs process data sequentially, one step at a time, which makes them suit‐ able for handling time-dependent data such as text. However, this sequential process‐ ing introduces a significant drawback: RNNs often struggle to retain information from earlier steps as they move forward in the sequence, especially over long inputs.

> 在 Transformer 出现之前，处理 NLP 任务最流行的解决方案是循环神经网络。RNN 按顺序逐步处理数据，这使其适合处理文本等具有时间依赖性的数据。然而，这种顺序处理方式带来了一个显著缺陷：RNN 在序列中向前推进时，往往难以保留早期步骤的信息，尤其是在处理长输入时。

During neural network training, the model processes input data and generates predictions. These predictions are compared to the correct answers using a loss function, which calculates the error (how far the predictions are from the correct answers). An algorithm, such as backpropagation, calculates gradients: values that indicate how the model's parameters (weights and biases) should be adjusted to reduce the error and improve accuracy.

> 在神经网络训练过程中，模型会处理输入数据并生成预测结果。这些预测结果会通过损失函数与正确答案进行比较，该函数会计算出误差（即预测值与正确答案之间的偏差）。随后，诸如反向传播等算法会计算梯度：这些数值指示了应如何调整模型的参数（权重和偏置），以减小误差并提升准确率。

However, in long sequences like those handled by RNNs, gradients can become very small as they are repeatedly multiplied during backpropagation. Over time, these small values may shrink so much that computers treat them as zero, effectively stopping the model from learning. This issue is known as the vanishing gradient problem, and it prevents the model from learning long-term dependencies in the data.

> 然而，在 RNN 处理的较长序列中，梯度在反向传播过程中反复相乘后会变得非常小。随着时间的推移，这些微小值可能会缩小到计算机将其视为零，从而有效阻止模型学习。这个问题被称为梯度消失问题，它阻止模型学习数据中的长期依赖关系。

Transformers, on the other hand, overcome this limitation by using self-attention and parallel processing, allowing them to handle sequences more efficiently and capture long-range dependencies effectively. Instead of processing data one step at a time, transformers analyze all input tokens (e.g., words in a sentence) simultaneously. Selfattention is a mechanism that allows each word or token in a sequence to focus on other words in the same sequence, regardless of their position. This is achieved by calculating a set of attention weights that measure the relevance of each token in the sequence to every other token. For instance, in a sentence, self-attention can help a word like it to align itself with its correct reference, even if that reference is several words away. Thus, self-attention allows the model to weigh the importance of each token relative to others in the input, enabling it to capture relationships across the entire input sequence efficiently. This parallel processing not only speeds up computation but also eliminates the issues associated with sequential processing, like the vanishing gradient problem.

> 另一方面，Transformer 通过使用自注意力机制和并行处理克服了这一局限，使其能够更高效地处理序列并有效捕捉长距离依赖关系。Transformer 并非逐步处理数据，而是同时分析所有输入标记（例如句子中的词语）。自注意力是一种机制，允许序列中的每个词语或标记关注同一序列中的其他词语，无论其位置远近。这是通过计算一组注意力权重实现的，这些权重衡量序列中每个标记与其他所有标记之间的相关性。例如，在一个句子中，自注意力可以帮助像“它”这样的词语正确关联其指代对象，即使该指代对象相隔数个词语。因此，自注意力使模型能够权衡输入中每个标记相对于其他标记的重要性，从而高效捕捉整个输入序列中的关系。这种并行处理不仅加速了计算，还消除了与顺序处理相关的问题，例如梯度消失问题。

Thanks to their ability to manage long-range dependencies and handle vast amounts of data, transformer-based models excel in various NLP tasks, including translation, summarization, and question answering. Their ability to focus on different parts of the sequence regardless of their relative distance, along with positional encoding to retain sequence order, allows transformers to handle long sequences without losing context.

> 由于 Transformer 模型能够管理长距离依赖关系并处理海量数据，因此它们在各种自然语言处理任务中表现出色，包括翻译、摘要和问答。它们能够关注序列中不同部分的能力，无论这些部分之间的相对距离如何，再加上用于保留序列顺序的位置编码，使得 Transformer 能够处理长序列而不会丢失上下文。

Some people wondered, "Well, since they can be scaled much better now, how about we throw more computing power and a lot more data at these models to see what happens?" Models like GPT-3, LLaMA, and their successors demonstrated that increasing the number of parameters can significantly improve the performance of transformer models.

> 一些人好奇地问道：“既然现在可以更好地扩展它们，那我们投入更多的计算能力和更多的数据到这些模型上，看看会发生什么？”像 GPT-3、LLaMA 及其后继者者这样的模型表明，增加参数数量可以显著提高 transformer 模型的性能。

Transformers have extended their influence beyond NLP into image processing with innovations like the vision transformer (ViT), which treats image patches as sequences and applies transformer models to them. ViT has shown promising results in image classification, offering a viable alternative to the previous solution, convolutional neural networks (CNNs). Additionally, in recommender systems, transformers' ability to model complex patterns and dependencies enhances accuracy and personalization. Table 1-1 compares the abilities of the neural network models we've discussed.

> Transformer 的影响力已从自然语言处理领域扩展至图像处理领域，其创新成果如视觉 Transformer（ViT）将图像块视为序列并应用 Transformer 模型进行处理。ViT 在图像分类任务中展现出优异性能，为传统解决方案卷积神经网络（CNN）提供了可行的替代方案。此外，在推荐系统中，Transformer 对复杂模式与依赖关系的建模能力显著提升了准确性与个性化程度。表 1-1 对我们讨论过的神经网络模型能力进行了对比。


![[Pasted image 20260609154802.png]]
`Table 1-1. The evolution of different neural network models`
`表 1-1 不同神经网络模型的能力对比`

This trend of throwing more compute and data at transformers is what sparked the evolution of LLMs, as well as the shift from an architecture that can do well on a single modality to one that generalizes on most modalities. Understanding this evolution can help you appreciate the differences in model architectures.

> 向 Transformer 投入更多算力和数据的这一趋势，不仅推动了大型语言模型的演进，也促使架构从擅长单一模态向泛化多种模态转变。理解这一演进过程，有助于你体会不同模型架构之间的差异。

## 3. Large Language Models
**大语言模型**

LLMs excel at understanding context and making associations among words, phrases, and concepts to provide relevant information based on the input query or prompt. While structured knowledge bases rely on human-curated data, LLMs can automatically extract knowledge from unstructured text. When trained on diverse textual sources, they can process a vast amount of information without explicit human intervention. However, this also introduces a challenge, as the model can learn biased or incorrect information from the training data.

> LLMs 擅长理解上下文，并在单词、短语和概念之间建立关联，从而根据输入的查询或提示提供相关信息。结构化知识库依赖人工整理的数据，而 LLMs 能够自动从非结构化文本中提取知识。当基于多样化的文本来源进行训练时，它们可以在没有明确人工干预的情况下处理大量信息。然而，这也带来了一个挑战，因为模型可能会从训练数据中学习到有偏见或不正确的信息。

LLMs are also designed to understand and generate human-like text and to be acces‐ sible through natural language queries in conversational, interactive settings. This makes them convenient and user-friendly for retrieving information and obtaining responses.

> LLMs 也被设计用于理解和生成类似人类的文本，并能够通过对话式、交互式环境中的自然语言查询进行访问。这使得它们在检索信息和获取回复时既方便又用户友好。

These models are "large" not just because of the amount of data they're trained on but also because of their number of parameters. Think of parameters as being like "knobs" inside the models that may be adjusted during training to help the models learn better. In neural networks, parameters are weights and biases. When an input like a prompt is presented to a model, it first transforms the input into a numerical representation, and then the numbers are processed through the neural network. Each node in the neural network contains a bias, adding or subtracting to the input value, and each connection between nodes contains a weight that will multiply the value of the input as it passes through nodes. Using more parameters greatly extends the capabilities of traditional transformer models, but not without massive trade-offs in cost and evaluation complexity.

> 这些模型之所以被称为“大型”，不仅因为它们训练所用的数据量庞大，还因为它们拥有大量的参数。可以将参数理解为模型内部的“旋钮”，在训练过程中可以调整这些旋钮，以帮助模型更好地学习。在神经网络中，参数包括权重和偏置。当模型接收到像提示词这样的输入时，它会先将输入转换为数值表示，然后这些数值会通过神经网络进行处理。神经网络中的每个节点都包含一个偏置，用于对输入值进行加法或减法运算；而节点之间的每条连接都包含一个权重，当输入值经过节点时，权重会对其进行乘法运算。使用更多的参数能极大地扩展传统 Transformer 模型的能力，但这并非没有代价——在成本和评估复杂性方面需要做出巨大权衡。

There are two basic categories of LLMs, discriminative and generative. *Discriminative models*, such as BERT (Bidirectional Encoder Representations from Transformers), which was introduced in 2018, learn the boundary between classes in a classification problem. They're concerned with the conditional probability $P(y|x)$ , which is the probability of the output given the input. Discriminative transformer models are typically used for tasks like text classification, sentiment analysis, and named-entity recognition, where the goal is to predict a label or category given some input text.

> LLM 主要分为两大类：判别式模型和生成式模型。*判别式模型*（如 2018 年推出的 BERT，即基于 Transformer 的双向编码器表征模型）通过学习分类问题中不同类别之间的边界来运作。它们关注条件概率 $P(y|x)$ ，即给定输入时输出的概率。判别式 Transformer 模型通常用于文本分类、情感分析和命名实体识别等任务，其目标是根据输入文本预测标签或类别。

*Generative models*, such as GPT-3 and GPT-4, learn the joint probability distribution of the input and the output, or $P(x, y)$, and can generate new data points similar to the training data. Generative models are used for tasks like text generation, where the goal is to generate new text similar to the text the model was trained on. Not all LLMs need to be generative, although most are. Throughout this book, when we refer to "LLMs," we mean generative LLMs.

> 生成式模型，例如 GPT-3 和 GPT-4，学习输入和输出的联合概率分布，即 $P(x, y)$ ，并能够生成与训练数据相似的新数据点。生成式模型用于文本生成等任务，其目标是生成与模型训练文本相似的新文本。并非所有大语言模型都必须是生成式的，尽管大多数如此。在本书中，当我们提到“大语言模型”时，均指生成式大语言模型。

## 4. LLM Architectures
**大语言模型架构**

There are two main types of architecture for language models: encoders and decoders. Encoders and decoders can also be combined, and there is ongoing research on new architectures.

> 语言模型主要有两种架构类型：编码器和解码器。编码器和解码器也可以组合使用，目前仍有关于新架构的研究正在进行中。

### 1) Encoder-Only LLMs
**仅编码器模型**

*Encoder-only models* are designed to process and comprehend input text, transforming it into a meaningful representation or embedding. Embeddings are numerical representations of data, such as words, phrases, or sentences, in a high-dimensional vector space. Embeddings capture meaning and context in a way that results in words with similar meanings or contexts being placed close together in this vector space. This representation captures the essence of the input, making it suitable for tasks where understanding the context is needed.

> *仅编码器模型* 旨在处理和理解输入文本，将其转化为有意义的表示或嵌入。嵌入是数据（如单词、短语或句子）在高维向量空间中的数值表示。嵌入通过捕捉语义和上下文信息，使得具有相似含义或上下文的单词在该向量空间中彼此靠近。这种表示方式捕获了输入的本质，使其适用于需要理解上下文的任务。

One of the most notable examples of an encoder-only model is **BERT**. During its pretraining phase, BERT uses *masked language modeling*, a technique where random words in the text are masked and the model learns to predict these masked words based on the surrounding context. BERT is also trained using next-sentence prediction, where it determines whether one sentence follows another logically.

> 最典型的编码器模型之一是 **BERT**。在预训练阶段，BERT 采用了 *掩码语言建模技术* ——文本中的随机词汇会被遮蔽，模型需要基于上下文语境预测这些被遮蔽的词汇。此外，BERT 还通过下一句预测任务进行训练，即判断一个句子是否在逻辑上承接另一个句子。

The primary advantage of encoder-only models lies in their syntactic understanding of text; i.e., their ability to capture the intricate relationships between words and their contexts. These models excel in tasks such as sentiment analysis, named-entity recognition, and question answering.

> 编码器专用模型的主要优势在于其对文本的句法理解能力，即捕捉词语与上下文之间复杂关系的能力。这类模型在情感分析、命名实体识别和问答等任务中表现尤为出色。

However, encoder-only models have their limitations. They are not designed for generating new text; their focus is solely on understanding and analyzing the input. This limitation can be restrictive when using them in applications requiring text generation or completion.

> 然而，仅编码器模型有其局限性。它们并非为生成新文本而设计；其重点仅在于理解和分析输入。当在需要文本生成或补全的应用中使用它们时，这一局限性可能会带来限制。

### 2) Decoder-Only LLMs
**仅解码器模型**

Decoder-only models are good at generating coherent and contextually relevant text based on an input or prompt. Examples of this architecture are the generative pretrained transformer (GPT) series, including GPT-2, GPT-3, and the most recent GPT-4.

> 仅解码器模型擅长根据输入或提示生成连贯且与上下文相关的文本。此类架构的典型示例包括生成式预训练变换器（GPT）系列，如 GPT-2、GPT-3 以及最新的 GPT-4。

These models are pretrained using a language modeling objective. With this technique, they learn to predict the next word in a sequence given the preceding context, allowing them to generate text that flows naturally and maintains coherence over longer passages.

> 这些模型通过语言建模目标进行预训练。利用这一技术，它们学会根据前文语境预测序列中的下一个词，从而能够生成自然流畅且能在较长段落中保持连贯性的文本。

The key advantage of decoder-only models is their ability to generate high-quality text. This makes them extremely effective for tasks such as text completion, summarization, and creative writing. They also exhibit *emergent properties* , meaning that they can perform tasks beyond their initial training objective, such as translation and question answering, without additional fine-tuning.

> 仅解码器模型的主要优势在于其生成高质量文本的能力。这使得它们在文本补全、摘要生成和创意写作等任务中极为高效。此外，它们还展现出 *涌现特性* ，即无需额外微调即可执行超出初始训练目标的任务，例如翻译和问答。

However, their focus on text generation can be a limitation in tasks requiring deep understanding of the input text. Decoder-only models generate text based on patterns learned during training, which may not always align with the specific nuances of the input.

> 然而，它们对文本生成的专注在需要深入理解输入文本的任务中可能成为局限。仅解码器模型基于训练期间学到的模式生成文本，这未必总能与输入文本的特定细微之处保持一致。

### 3) Encoder–Decoder LLMs
**编码器-解码器模型**

*Encoder–decoder models* combine the strengths of both encoder and decoder architectures, making them suitable for tasks involving complex mappings between input and output sequences.

> *编码器-解码器模型* 结合了编码器和解码器两种架构的优势，使其适用于涉及输入与输出序列之间复杂映射的任务。

In this setup, the encoder processes the input text to create an embedding, which the decoder then uses to generate the output text. Notable examples include Bidirectional and Auto-Regressive Transformer (BART) and Text-To-Text Transfer Transformer (T5). BART, introduced in 2019, is trained using *denoising auto-encoding*, where parts of the input text are corrupted and the model learns to reconstruct the original text.

> 在这种设置中，编码器处理输入文本以生成嵌入，解码器随后利用该嵌入生成输出文本。典型的例子包括双向自回归变换器（BART）和文本到文本迁移变换器（T5）。BART 于 2019 年提出，采用 *去噪自编码方式* 进行训练，即输入文本的部分内容被破坏，模型学习重建原始文本。

The encoder–decoder architecture excels at tasks where the input and output are different in structure and length, such as machine translation and text summarization. However, the complexity of training and the computational resources these models require can be a drawback. Their dual architecture means they must effectively integrate both components, which can be demanding in terms of both data and processing power.

> 编码器-解码器架构在处理输入和输出在结构和长度上不同的任务时表现出色，例如机器翻译和文本摘要。然而，这些模型所需的训练复杂性和计算资源可能成为其缺点。其双重架构意味着必须有效整合两个组件，这在数据和计算能力方面可能要求较高。

### 4) State Space Architectures

A new approach tries to solve one of the problems with transformers, which is that the self-attention mechanism has *quadratic complexity*. This means that the number of computations required for inferencing grows with the square of input size, since the relationship between each pair of tokens needs to be modeled. Mathematically, it is often represented as $O(n²)$, where $n$ is the number of tokens (words or subwords in a sentence). Quadratic complexity is generally a hard computational problem, especially when using larger datasets.

> 一种新方法试图解决 Transformer 的一个问题，即自注意力机制具有 *二次复杂度* 。这意味着推理所需的计算量随输入规模的平方增长，因为需要建模每个词元对之间的关系。在数学上，这通常表示为 $O(n²)$，其中 $n$ 是词元数量（句子中的单词或子词）。二次复杂度通常是一个棘手的计算问题，尤其是在使用较大数据集时。

The state space architecture replaces the transformer approach by incorporating state space representations, which model the state of the system instead of recording it at each step. This compression allows for linear computational complexity, improving computational performance and reducing memory requirements, but it increases the rate of error.

> 状态空间架构通过引入状态空间表示来替代 Transformer 方法，这种表示方式对系统状态进行建模，而非在每个步骤中记录状态。这种压缩实现了线性计算复杂度，提升了计算性能并降低了内存需求，但同时也增加了错误率。

Researchers are trying to solve the error problem. Recent examples are **Mamba and Mamba-2**, which create a state representation that dynamically attempts to determine the important parts of the prompt by modeling importance as a state space parameter. In experimental settings, Mamba performs as well as a transformer-based model that has double the number of parameters for small and medium prompts but still has not delivered on the promise of low error rates for larger prompts.

> 研究人员正试图解决错误问题。最近的例子是 **Mamba 和 Mamba-2**，它们创建了一种状态表示，通过将重要性建模为状态空间参数，动态地尝试确定提示中的重要部分。在实验环境中，Mamba 的表现与基于 Transformer 的模型相当，后者在中小型提示下拥有两倍的参数数量，但在较大提示下仍未实现低错误率的承诺。

Each LLM architectural design has its own sets of strengths and limitations. Encoderonly models like BERT are highly effective for understanding and analyzing text but fall short in generating new content. Decoder-only models, exemplified by the GPT series, excel in generating coherent and contextually relevant text but are nondeterministic, which can be problematic for some applications like text classification. Emerging architectures like state space models, which promise enhancements in performance and applicability, should be monitored, but they haven't been proven yet.

> 每种 LLM 架构设计都有其自身的优势和局限性。像 BERT 这样的仅编码器模型在理解和分析文本方面非常有效，但在生成新内容方面存在不足。以 GPT 系列为代表的仅解码器模型擅长生成连贯且与上下文相关的文本，但具有非确定性，这对于文本分类等某些应用来说可能是个问题。像状态空间模型这样的新兴架构，有望提升性能和适用性，值得关注，但它们尚未得到验证。

### 5) Small Language Models
**小型语言模型**

Another recent development is *small language models* (SLMs), which are compact, efficient language models designed to perform NLP tasks while using fewer computational resources than LLMs.

> 另一个最近的发展是 *小语言模型* （SLMs），它们是紧凑、高效的语言模型，旨在使用比大语言模型更少的计算资源来执行自然语言处理任务。

Unlike LLMs, which contain billions of parameters and require substantial memory and processing power, SLMs are often designed to have millions or even just hundreds of thousands of parameters. The trade-off is that they must focus on specific tasks or subjects. This makes them lightweight, cost-effective, and deployable on a wider range of devices, including mobile phones, IoT edge devices, and in environments with limited computational resources. The development of SLMs has been driven by the demand for efficient, accessible AI solutions that can operate in real time and offline, providing functionality without relying on cloud-based infrastructure.

> 与包含数十亿参数、需要大量内存和处理能力的 LLM 不同，SLM 通常设计为拥有数百万甚至仅数十万个参数。这种权衡意味着它们必须专注于特定任务或领域。这使得 SLM 轻量、经济高效，并且可部署在更广泛的设备上，包括手机、物联网边缘设备以及计算资源有限的环境中。SLM 的发展得益于对高效、易用 AI 解决方案的需求，这些方案能够实时和离线运行，无需依赖云端基础设施即可提供功能。

SLMs do not perform well on tasks that require contextual understanding, extensive memory, or reasoning abilities. They are not intended for more general problemsolving and need to be fine-tuned on specific datasets to perform well on particular tasks, maximizing efficiency while maintaining accuracy within a defined scope. While LLMs tend to perform several NLP tasks reasonably well in a large number of domains, SLMs need to be specifically trained. For instance, an LLM might be able to perform moderately well at summarizing legal documents as well as medical articles, while an SLM would excel in one and perform poorly at the other.

> SLMs 在需要上下文理解、大量记忆或推理能力的任务上表现不佳。它们不适用于更通用的问题解决，需要针对特定数据集进行微调才能在特定任务上表现良好，从而在保持准确性的同时最大化效率。虽然 LLMs 在众多领域中能够较好地执行多项 NLP 任务，但 SLMs 需要专门训练。例如，一个 LLM 可能在总结法律文件和医学文章方面表现尚可，而一个 SLM 则会在其中一项上表现出色，但在另一项上表现糟糕。

## 5. Choosing an LLM
**选择一个大语言模型**

In the LLM world, it's easy to get swept up in the excitement of the latest breakthroughs and cutting-edge technologies. New models pop up all the time. The truth is, selecting the right LLM is more than just a technical decision; it's a strategic choice with far-reaching implications.

### 1) Considerations in the Selection of an LLM

Here are five reasons why the model you choose can make all the difference:

> 在 LLM 领域，人们很容易被最新突破和前沿技术带来的兴奋感所裹挟。新模型层出不穷。事实上，选择合适的 LLM 不仅仅是一个技术决策，更是一个具有深远影响的战略选择。

#### *a. Alignment with objectives*
***与目标保持一致***

Are you looking for a model that excels at generating human-like text? Or do you need one that can understand complex queries and provide accurate responses? The specific capabilities of different models can vary significantly. Some are designed with a focus on conversational abilities, while others are optimized for tasks like summarization or translation. Choosing a model that aligns with your objectives ensures that you're investing in a tool that will deliver the results you need.

> 您是否在寻找一个擅长生成类人文本的模型？或者您需要一个能够理解复杂查询并提供准确回答的模型？不同模型的具体能力差异显著。有些模型专注于对话能力，而另一些则针对摘要或翻译等任务进行了优化。选择与您目标相符的模型，能确保您投资于能够交付所需成果的工具。

#### *b. Performance and efficiency*
***性能与效率***

Not all LLMs are created equal. Larger models might offer impressive performance and efficiency, but they often come with high computational costs and slower response times. Smaller, more optimized models tend to provide faster results and be more cost-effective, but rarely do they match the performance of their larger counterparts.

> 并非所有的 LLM 都生而平等。较大的模型可能展现出令人瞩目的性能和效率，但通常伴随着高昂的计算成本和较慢的响应时间。较小且经过优化的模型往往能提供更快的处理结果，且更具成本效益，但它们的性能很少能与大型模型相媲美。

#### *c. Training data and bias*
***训练数据与偏差***

The training data used to develop an LLM shapes its behavior and outputs. Variations in the datasets on which models are trained can lead to variations in how they handle specific topics or issues. Some models exhibit biases based on their training data, which can impact the accuracy and fairness of their responses. Choosing a model with a diverse and representative training dataset can help mitigate these risks and ensure more reliable and equitable outcomes.

> 用于开发 LLM 的训练数据决定了其行为与输出。模型训练所用数据集的差异，会导致它们处理特定话题或问题的方式产生变化。部分模型会因训练数据而表现出偏见，这会影响其回答的准确性与公平性。选择训练数据集多样且具有代表性的模型，有助于降低这些风险，并确保获得更可靠、更公平的结果。

#### *d. Customization and adaptability*
**定制化与适应性**

Your needs might not fit neatly into the one-size-fits-all approach of a generic LLM. Some models offer greater flexibility and can be fine-tuned or customized to better suit your specific requirements. If that's what you need, choose one with strong customization capabilities so that you can mold it to better fit your use case.

> 你的需求可能无法完全契合通用 LLM 那种“一刀切”的方法。有些模型提供了更大的灵活性，可以进行微调或定制，以更好地满足你的特定要求。如果这正是你所需要的，请选择一款具备强大定制能力的模型，这样你就可以对其进行调整，使其更贴合你的使用场景。

#### *e. Integration and support*
**集成与支持**

The practical aspects of integrating an LLM into your existing systems and workflows cannot be overlooked. Some models come with robust support and documentation, making integration smoother and less time-consuming. Others require more effort to set up and maintain. Considering how well a model integrates with your infrastructure and the level of support available can save you time and reduce headaches over the long run.

> 将 LLM 集成到现有系统和工作流程中的实际方面不容忽视。一些模型提供强大的支持和文档，使集成过程更顺畅且耗时更少。其他模型则需要更多精力来设置和维护。考虑模型与基础设施的集成程度以及可用的支持水平，从长远来看可以节省时间并减少麻烦。

---

Overall, the LLM model you choose is not just a technical decision; it's a strategic one that impacts the effectiveness, efficiency, and overall success of your AI initiatives.

> 总体而言，您选择的 LLM 模型不仅仅是一个技术决策，更是一个战略决策，它会影响您 AI 项目的有效性、效率以及整体成功与否。

Remember: the model you choose matters. By carefully evaluating your needs and understanding the strengths and limitations of different models, you can make an informed choice that aligns with your goals and sets you up for success.

> 请记住：您选择的模型至关重要。通过仔细评估您的需求，并了解不同模型的优势与局限，您可以做出明智的选择，使其与您的目标保持一致，并为您奠定成功的基础。

### 2) The Big Debate: Open Source Versus Proprietary LLMs
**大辩论：开源LLM vs 专有LLM**

Companies must navigate a complex landscape when choosing among open source, closed-source, and open weight LLMs. Figure 1-1 shows the choices of a sample of companies today. This section looks at each option's limitations and benefits.

> 公司在选择开源、闭源和开放权重的 LLM 时，必须应对复杂的局面。图 1-1 展示了当前部分公司的选择情况。本节将探讨每种选项的局限性与优势。


![[Pasted image 20260609191002.png]]
`Figure 1-1. Enterprise adoption of different proprietary LLMs (source: Andreessen Horowitz)`
`图1-1.企业对不同专有 LLM 的采用情况（来源：安德森·霍洛维茨基金）`

#### a. Open source and open weight LLMs
**开源和开放权重的 LLM**

Open source and open weight are two types of publicly accessible LLMs that have gained traction in the AI community as of this writing, particularly among those looking to customize, deploy, or study advanced AI without relying on proprietary solutions.

> 开源和开放权重是两种公开可访问的大语言模型，截至撰写本文时，它们在人工智能社区中已获得广泛关注，尤其是那些希望在不依赖专有解决方案的情况下定制、部署或研究先进 AI 的人群。

*Open source* LLMs are models with freely available underlying source code. Anyone can inspect, modify, and potentially redistribute the model and its architecture. These models typically include details about the architecture, training methods, and source code for the framework. Using open source models provides technical transparency and adaptability and fosters a community of collaboration. However, open source LLMs may or may not come with pretrained weights, the trained parameters that make the model functional and useful for specific tasks. These weights are the model's "knowledge" gained from its training on large datasets and are essential for the model to perform effectively without retraining from scratch. Companies that want to take advantage of such models may need to acquire the training data themselves.

> *开源* LLM 是指其底层源代码可自由获取的模型。任何人都可以审查、修改，甚至重新分发模型及其架构。这类模型通常会公开架构细节、训练方法以及框架的源代码。使用开源模型能带来技术透明性和适应性，并促进社区协作。不过，开源 LLM 可能附带也可能不附带预训练权重——这些经过训练的参数量决定了模型的功能性及其在特定任务中的实用性。这些权重是模型通过大规模数据集训练获得的“知识”，对于模型无需从头重新训练就能有效运行至关重要。希望利用此类模型的企业可能需要自行获取训练数据。

With *open weight* LLMs, the weights are publicly accessible. Having access to the weights means that users can directly deploy the model for real-world applications like text generation, summarization, and translation or fine-tune it on their own data. While many open weight models are also open source, some restrict use for commercial applications or require adherence to specific licensing terms, as seen with models like Meta's Llama series.

> 对于 *开放权重* 的 LLM，其权重是公开可访问的。拥有权重访问权限意味着用户可以直接部署模型用于实际应用，例如文本生成、摘要、翻译，或基于自身数据对模型进行微调。尽管许多开放权重模型也属于开源范畴，但部分模型会限制商业用途或要求遵守特定许可条款，例如 Meta 的 Llama 系列模型。

The distinction between open source and open weight LLMs is crucial in determining how accessible and useful a model is "out of the box." Open source models without weights can still allow for architectural experimentation and model-training setups, but they lack immediate functionality for practical applications until they are trained, and training requires substantial computational resources. In contrast, open weight models provide ready-to-use capabilities, making them more accessible to developers who do not have the resources for large-scale model training but want to fine-tune or deploy a pretrained model.

> 开源与开放权重的 LLM 之间的区别，对于判断一个模型“开箱即用”的易用性和实用性至关重要。不包含权重的开源模型仍允许进行架构实验和模型训练设置，但它们在训练完成前缺乏实际应用的即时功能，而训练需要大量的计算资源。相比之下，开放权重的模型提供了即用型能力，使那些没有资源进行大规模模型训练、但希望微调或部署预训练模型的开发者更容易使用。

By leveraging open source and/or open weight models such as Llama or Mistral, companies can deploy models on existing hardware. This can be more cost-effective than using cloud-based proprietary solutions, which involve renting hardware. Such an approach can be particularly advantageous for startups or small to medium enterprises (SMEs) operating under tight budget constraints. For these companies, the financial savings can free up resources for other needs, like fine-tuning.

> 通过利用 Llama 或 Mistral 等开源和/或开放权重模型，企业可以在现有硬件上部署模型。这比使用基于云的专有解决方案更具成本效益，因为后者需要租赁硬件。对于预算紧张运营的初创公司或中小企业（SMEs）而言，这种方法尤为有利。对这些公司来说，节省的资金可以释放资源用于其他需求，例如微调。

A company may have requirements besides financial concerns, such as wanting to ensure that the training data includes or excludes specific datasets. In these cases, an open weight model is not sufficient; the business really needs an open source model. For example, a company may want to guarantee that a model has never seen a specific data point; an open weight model whose training dataset is not shared can't offer such a guarantee.

> 除了财务方面的考量，公司可能还有其他需求，例如希望确保训练数据包含或排除特定数据集。在这种情况下，仅开放权重的模型是不够的，企业真正需要的是开源模型。例如，一家公司可能希望保证模型从未见过某个特定数据点；而训练数据集未公开的开放权重模型无法提供这种保证。

Community support is another potential advantage of open source LLMs. The collaborative nature of the open source ecosystem means that developers, researchers, and organizations continuously contribute to improving these models, and newly finetuned models are easily available via Hugging Face. Companies benefit not only from this collective intelligence but also from access to a wider range of resources, tools, and best practices. This community-driven development is dynamic and evolving, and it's often where new developments begin.

> 社区支持是开源大语言模型的另一个潜在优势。开源生态系统的协作特性意味着开发者、研究人员和组织机构会持续为改进这些模型做出贡献，而新微调后的模型也能通过 Hugging Face 轻松获取。企业不仅能从这种集体智慧中受益，还能获得更广泛的资源、工具和最佳实践。这种社区驱动的发展模式充满活力且不断演进，许多新进展往往正是从这里起步。

However, the open source/open weight approach is not without its challenges. Maintenance and support can be significant hurdles. Data privacy and security also emerge as big concerns. Transparency can be a double-edged sword, exposing a company to potential risks even as it demands significant effort to safeguard sensitive information and comply with data protection regulations. Ensuring that these models do not become a vector for security breaches requires meticulous attention and proactive measures.

> 然而，开源/开放权重的方法并非没有挑战。维护和支持可能是重大障碍。数据隐私和安全也成为一大担忧。透明度可能是一把双刃剑，既让公司面临潜在风险，又需要付出巨大努力来保护敏感信息并遵守数据保护法规。确保这些模型不会成为安全漏洞的传播途径，需要细致的关注和主动的措施。

Scalability and performance are additional considerations. Open source LLMs aren't always optimized for large-scale deployments. Companies with substantial operational demands might face performance bottlenecks or scalability challenges. The customization required to adapt open source models for enterprise-grade applications can be resource intensive and require significant engineering efforts.

> 可扩展性和性能是额外的考量因素。开源大语言模型并不总是针对大规模部署进行优化。运营需求较大的公司可能会面临性能瓶颈或可扩展性方面的挑战。为将开源模型适配至企业级应用所需的定制化工作，可能耗费大量资源并需要投入显著的工程力量。

Open source and open weight language models also introduce security concerns. Anyone can immediately use, fine-tune, or modify pretrained open weight models and potentially apply them in harmful ways, such as generating misinformation, creating realistic fake content, or deploying automated tools for phishing and social engineering. Since open weight models' training data often includes both public and proprietary datasets, they can also sometimes unintentionally generate or reveal sensitive or biased information embedded in the training data, posing privacy risks.

> 开源和开放权重的语言模型也带来了安全隐患。任何人都可以立即使用、微调或修改预训练的开放权重模型，并可能以有害的方式应用它们，例如生成虚假信息、制作逼真的伪造内容，或部署用于钓鱼攻击和社会工程学的自动化工具。由于开放权重模型的训练数据通常同时包含公开和专有数据集，它们有时也可能无意中生成或泄露训练数据中嵌入的敏感或有偏见的信息，从而带来隐私风险。

Furthermore, open source models, which include the code and architectural blueprints, are vulnerable to manipulation and exploitation. Malicious actors can intro‐ duce harmful code or adjust models to bypass safety mechanisms, then distribute these altered versions under the guise of legitimate software. This can lead to scenarios where organizations unknowingly adopt models that include backdoors or biased, harmful outputs. The decentralized nature of open source development means that code modifications don't always go through rigorous security checks, leaving room for vulnerabilities that could be exploited. Addressing these security challenges requires adopting responsible AI practices, including rigorous code reviews, security audits, and clear usage policies to mitigate risks while promoting open collaboration.

> 此外，开源模型（包括代码和架构蓝图）容易受到操纵和利用。恶意行为者可以引入有害代码或调整模型以绕过安全机制，然后以合法软件的名义分发这些被篡改的版本。这可能导致组织在不知情的情况下采用包含后门或带有偏见、有害输出的模型。开源开发的去中心化特性意味着代码修改并不总是经过严格的安全检查，从而为可能被利用的漏洞留下空间。应对这些安全挑战需要采用负责任的人工智能实践，包括严格的代码审查、安全审计和明确的使用政策，以在促进开放协作的同时降低风险。

Carefully review any contractual restrictions on usage before adopting a model. You don't want to build a whole commercial application around an open source LLM only to find out that it does not allow commercial usage.

> 在采用模型之前，请仔细审查任何关于使用的合同限制。 您不希望围绕一个开源 LLM 构建整个商业应用程序，却发现它不允许商业用途。

#### b. Closed-source LLMs
**闭源 LLM**

On the other side of the spectrum are closed-source, or proprietary, LLMs such as those developed by leading tech giants. These models often come with robust support and maintenance, including dedicated assistance for troubleshooting and optimizing performance. This support infrastructure ensures that any issues encountered are addressed promptly, allowing companies to focus on their core activities without getting sidetracked by technical difficulties.

> 在光谱的另一端，是闭源或专有的 LLM，例如由领先科技巨头开发的模型。这些模型通常配备强大的支持与维护服务，包括针对故障排除和性能优化的专属协助。这种支持基础设施确保任何遇到的问题都能得到及时解决，使企业能够专注于核心业务，而不会被技术难题所牵绊。

Closed-source LLMs are generally optimized for large-scale deployments, making sure that they can scale with operational loads effectively, so they often come with performance guarantees. Their performance benchmarks often reflect their ability to deliver consistent and reliable results—a critical factor for companies with high operational demands.

> 闭源 LLM 通常针对大规模部署进行了优化，确保它们能够有效应对运营负载的扩展，因此往往附带性能保证。其性能基准测试通常反映了它们提供一致且可靠结果的能力——这对于运营需求较高的企业而言是一个关键因素。在 2025 年，许多公司开始依赖这些模型，因为它们的性能指标在公开数据中得到了验证，例如准确率和响应时间。

One of the primary limitations of the closed-source approach is the high cost. Another is the lack of transparency, which means that companies have limited visibility into the internal workings of these models. While this concern may seem unusual, consider a scenario in which a commercial LLM provider inadvertently consumes private data during training. You use this LLM provider for your own applica‐ tion, and some of your users realize how to get your application to reveal the private data. The people whose data was revealed sue you. We recommend that you fully understand what legal protections are in place when using information services like third-party LLMs.

> 闭源方法的主要局限性之一是成本高昂。另一个是缺乏透明度，这意味着企业对模型内部运作的可见性有限。虽然这种担忧看似不寻常，但请设想一个场景：某商业 LLM 提供商在训练过程中无意中使用了私人数据。你使用该提供商开发自己的应用程序，而部分用户发现了如何让应用泄露这些私人数据。数据被泄露的人将你告上法庭。我们建议你充分了解使用第三方 LLM 等信息服务时，法律提供了哪些保护措施。

Regardless of these drawbacks, companies are willing to make expensive bets right now, hoping for excellent returns in the future from investing in GenAI applications.

> 尽管存在这些不足，企业目前仍愿意进行高额投入，期望未来能从生成式 AI 应用中获取丰厚回报。

## 6. Enterprise Use Cases for LLMs
**LLM 的企业用例**

LLMs are transforming enterprise operations in many industries, from changing how we retrieve knowledge to enhancing autonomous agents. They do this through a handful of applications, including knowledge retrieval, translation, audio–speech synthesis, recommender systems, and autonomous agents.

> LLM 正在改变许多行业的企业运营方式，从改变我们检索知识的方式到增强自主智能体。它们通过一系列应用实现这一点，包括知识检索、翻译、语音合成、推荐系统和自主智能体。

### 1) Knowledge Retrieval
**知识检索**

People have long used search engines to discover information, but the limitations of these tools' have become more apparent as data volumes and complexity grow. LLMs offer a new paradigm for accessing and using information. Unlike conventional systems, which rely heavily on keyword matching and ranking algorithms, LLMs bring a conversational, personalized approach to information retrieval.

> 长期以来，人们一直使用搜索引擎来发现信息，但随着数据量和复杂性的增长，这些工具的局限性也愈发明显。LLM 为访问和使用信息提供了一种新的范式。与严重依赖关键词匹配和排序算法的传统系统不同，LLM 为信息检索带来了对话式、个性化的方法。

Users can engage in long conversations with LLMs. Instead of simply receiving a list of links or documents, they can set parameters for the tone, intent, and structure of the information they need. This capability transforms the search experience from a transactional process into a dynamic dialogue. For example, an LLM can interpret a request like "Explain this concept as if I were a beginner," and provide a tailored explanation that's both accessible and relevant.

> 用户可以与大型语言模型进行长时间的对话。他们不再只是收到一系列链接或文档，而是可以为所需信息的语气、意图和结构设置参数。这种能力将搜索体验从一次性的交易过程转变为动态的对话。例如，大型语言模型可以理解“请像对初学者一样解释这个概念”这样的请求，并提供既易于理解又切合实际的定制化解释。

On the data retrieval side, LLMs can enhance productivity tools, for example through integrations with office software suites like those from Google and Microsoft. Imag‐ ine querying a spreadsheet with natural language to extract insights or asking a docu‐ ment to summarize key points. This simplifies data management and makes complex information more accessible. Furthermore, LLMs can integrate with internal systems to automate routine tasks and create knowledge graphs, streamlining workflows and enhancing organizational efficiency. However, while LLMs improve the accuracy and relevance of information retrieval, they also require meticulous handling to ensure data privacy and system security.

> 在数据检索方面，LLM 可以提升生产力工具的效率，例如通过与 Google 和 Microsoft 等办公软件套件的集成。想象一下，用自然语言查询电子表格以提取洞察，或让文档总结关键点。这简化了数据管理，使复杂信息更易获取。此外，LLM 可以与内部系统集成，自动化日常任务并创建知识图谱，从而简化工作流程并提高组织效率。然而，尽管 LLM 提高了信息检索的准确性和相关性，它们也需要谨慎处理，以确保数据隐私和系统安全。

### 2) Translation
**翻译**

Translation is another domain where LLMs are being used heavily. Traditional machine translation systems often struggled with languages for which they had limited datasets, as they had to rely on statistical methods. LLMs are changing this by offering zero-shot and few-shot translation capabilities. Zero-shot refers to the model's ability to translate languages without prior examples, a feat that was previously challenging. Few-shot, on the other hand, allows LLMs to perform well with minimal data.

> 翻译是 LLM 被广泛应用的另一个领域。传统机器翻译系统在处理数据集有限的语言时常常面临困难，因为它们不得不依赖统计方法。LLM 通过提供零样本和少样本翻译能力正在改变这一现状。零样本指的是模型无需事先示例即可翻译语言的能力，这在以前是一项具有挑战性的壮举。而少样本则允许 LLM 在数据极少的情况下也能表现出色。

This is particularly advantageous for translating languages that are underrepresented in training datasets. For companies involved in global operations or content creation, this is a major selling point. It eases localization of content, such as subtitling films or translating marketing materials, without extensive data requirements, allowing companies to expand into new markets without investing too many resources up front.

> 这对于翻译在训练数据集中代表性不足的语言尤为有利。对于从事全球运营或内容创作的公司来说，这是一个重要的卖点。它简化了内容本地化过程，例如为电影添加字幕或翻译营销材料，无需大量的数据需求，从而使公司能够在不预先投入过多资源的情况下拓展新市场。

LLMs trained on multilingual datasets can easily adapt to new languages, allowing translations across a broader spectrum of languages, including those with sparse resources. The applications for this extend to literature, film, and even real-time communication, where accurate and contextually appropriate translation can be helpful.

> 在多种语言数据集上训练的 LLM 能够轻松适应新语言，从而支持更广泛语言的翻译，包括资源匮乏的语言。其应用可延伸至文学、电影甚至实时交流领域，在这些场景中，准确且符合语境的翻译能发挥重要作用。

Yet, while LLMs offer significant improvements over traditional translation methods, maintaining accuracy and handling idioms still remain open challenges.

> 然而，尽管 LLM 相比传统翻译方法有了显著改进，但在维持准确性和处理习语方面，仍然存在未解决的挑战。

### 3) Speech Synthesis
**语音合成**

The ability to generate speech that resonates with human listeners can significantly enhance user experience and interaction. *Speech synthesis*, generating audio that mimics human speech from text, is another area where LLMs are making remarkable progress. Historically, speech synthesis systems have struggled with creating natural and engaging audio outputs: the sound generated sounded clearly "robotic." LLMs, however, have the potential to revolutionize this field by generating human-like speech with impressive fidelity. With training on text and audio datasets, LLMs can understand and replicate the subtleties of human speech, such as intonation, rhythm, and stress.

> 生成能与人类听众产生共鸣的语音能力，可以显著提升用户体验和交互效果。*语音合成* ——即从文本生成模仿人类语音的音频——是 LLM 取得显著进展的另一个领域。历史上，语音合成系统在生成自然且富有吸引力的音频输出方面一直面临挑战：所生成的声音明显带有“机械感”。然而，LLM 有潜力通过生成具有惊人保真度的人类语音来彻底改变这一领域。通过基于文本和音频数据集的训练，LLM 能够理解并复现人类语音的细微之处，例如语调、节奏和重音。

This is useful for applications like virtual assistants, realistic voice-overs for characters in video games, or engaging audio content for educational materials. Using LLMs to automate the creation of speech content makes it easy for businesses to produce large volumes of content without the time and costs of extensive manual recording. However, audio–speech synthesis still has room to improve, especially with regard to recognizing accents and other variations in speech.

> 这对于虚拟助手、视频游戏角色逼真的配音或教育材料中引人入胜的音频内容等应用非常有用。利用 LLM 自动化生成语音内容，使企业能够轻松制作大量内容，而无需耗费大量时间和成本进行手动录音。然而，语音合成仍有改进空间，尤其是在识别口音和其他语音变体方面。

### 4) Recommender Systems
**推荐系统**

Recommender systems are at the heart of many digital platforms, from ecommerce to streaming services. LLMs enhance these systems by incorporating a deeper understanding of users' preferences and contextual factors. Earlier recommender systems relied on historical user data and predefined algorithms, which often led to limited or repetitive suggestions. LLMs, with their ability to process and interpret diverse data sources, offer a more nuanced approach.

> 推荐系统是众多数字平台的核心，从电子商务到流媒体服务皆是如此。LLM 通过更深入地理解用户偏好与情境因素，增强了这些系统的能力。早期的推荐系统依赖历史用户数据和预定义算法，往往导致推荐内容受限或重复。而 LLM 凭借其处理与解读多样化数据源的能力，提供了更为精细的解决方案。

LLM-powered recommender systems can analyze user interactions, preferences, and even conversational cues, including audio and video inputs, to deliver personalized recommendations in real time. For example, if a user describes a product in natural language and provides an image, the LLM can integrate both modalities to offer more relevant suggestions, even in response to ambiguous or vague requests.

> 基于 LLM 的推荐系统能够分析用户交互、偏好乃至对话线索（包括音频和视频输入），从而实时提供个性化推荐。例如，当用户用自然语言描述某产品并附上图片时，LLM 可整合两种模态信息，即便面对模糊或笼统的请求，也能给出更精准的建议。

Despite these advantages, many challenges remain unsolved. For example, maintaining user trust requires careful attention to the model's transparency and reasoning.

> 尽管存在这些优势，但许多挑战仍未得到解决。例如，维护用户信任需要密切关注模型的透明度和推理过程。

### 5) Autonomous AI Agents
**自主 AI 智能体**

*AI agents* are designed to perform specific tasks autonomously, leveraging LLMs to execute complex operations that would otherwise require human intervention.

> *AI 智能体* 被设计用于自主执行特定任务，利用 LLM 来完成原本需要人工干预的复杂操作。

For example, in a customer service environment, traditional automated agent systems might follow rigid scripts or rely on basic rule-based logic. LLM-powered AI agents, however, can engage in dynamic, context-aware conversations. They understand user queries more deeply, interpret intent more accurately, and generate responses that are more natural and engaging.

> 例如，在客户服务环境中，传统的自动化客服系统可能遵循僵化的脚本或依赖基本的规则逻辑。然而，基于 LLM 的 AI 智能体能够进行动态且具有上下文感知能力的对话。它们能更深入地理解用户查询，更准确地解读意图，并生成更自然、更具吸引力的回复。

In project management, LLMs can power intelligent project assistants that manage schedules, set reminders, and even draft project reports. These AI agents can interact with team members, understand project requirements, and adapt their responses to ongoing developments.

> 在项目管理中，LLM 可以驱动智能项目助手，管理日程安排、设置提醒，甚至起草项目报告。这些 AI 智能体能够与团队成员互动，理解项目需求，并根据项目进展调整回应。

### 6) Agentic Systems
**智能体系统**

*Agentic systems* represent a more novel application of LLMs, where AI agents not only perform tasks but also make strategic decisions. These systems leverage LLMs' data processing and analysis capabilities to discern patterns and make informed decisions in real time. This is particularly helpful in environments where decisions need to be based on complex, multifaceted information (as shown by the example workflow in Figure 1-2).

> *智能体系统* 代表了 LLM 的一种更创新的应用，其中 AI 智能体不仅执行任务，还能做出战略决策。这些系统利用 LLM 的数据处理和分析能力，实时识别模式并做出明智的决策。这在需要基于复杂、多维度信息做出决策的环境中尤其有用（如图 1-2 中的示例工作流程所示）。

![[Pasted image 20260610113033.png]]
`Figure 1-2. Agentic AI in the enterprise (source: Haptik)`
`图1-2 企业中的智能体人工智能（来源：Haptik）`

In finance, agentic systems can digest data from financial reports, news articles, and market analytics, then use it to analyze market trends, assess risk factors, and make investment recommendations that align with investment strategies.

> 在金融领域，智能体系统能够消化来自财务报告、新闻文章和市场分析的数据，进而利用这些数据来分析市场趋势、评估风险因素，并做出符合投资策略的投资建议。

Similarly, in supply chain management, agentic systems can optimize inventory levels, predict demand fluctuations, and coordinate logistics based on data from various sources—such as sales forecasts, supply chain disruptions, and production schedules.

> 同样，在供应链管理中，智能体系统可以优化库存水平、预测需求波动，并基于来自销售预测、供应链中断和生产计划等多种来源的数据协调物流。

However, these systems aren't always reliable. Integrating them into existing workflows requires careful planning. Companies must consider how AI agents and agentic systems will interact with human teams, how they will be managed, and how their outputs will be monitored. Clear guidelines and oversight mechanisms are essential to ensure that these systems complement rather than disrupt existing operations. These issues are discussed in Chapter 8.

> 然而，这些系统并非总是可靠的。将它们整合到现有工作流程中需要周密的规划。企业必须考虑 AI 智能体及智能体系统将如何与人类团队协作、如何被管理，以及其输出结果如何被监控。明确的指导方针和监督机制对于确保这些系统能够补充而非干扰现有运营至关重要。这些问题将在第 8 章中讨论。

Data security and privacy are also big concerns. LLMs handle vast amounts of sensitive information, and protecting it from breaches or misuse is key. You need to establish strong data governance policies and invest in security measures to safeguard against potential risks. These issues, too, are discussed in Chapter 8.

> 数据安全与隐私同样是重大关切。LLM 处理大量敏感信息，保护其免遭泄露或滥用至关重要。你需要制定严格的数据治理政策，并投资于安全措施以防范潜在风险。这些问题也将在第 8 章中讨论。

## 7. Ten Challenges of Building with LLMs
**使用 LLM 构建应用的十大挑战**

LLMs introduce several new challenges, which can be amplified by the enormous scale of LLMs and their numerous applications. Addressing these challenges is important for integrating and deploying LLMs in production. Following is a list of 10 challenges with pointers to the chapters in this book where they are addressed.

> LLM 带来了若干新的挑战，这些挑战可能因 LLM 的庞大规模及其众多应用而被放大。解决这些挑战对于在生产环境中集成和部署 LLM 至关重要。以下是 10 个挑战的列表，并附有本书中涉及这些挑战的章节指引。

### 1) Size and Complexity
**规模与复杂性**

LLMs generally have millions or even billions of parameters. This makes training, monitoring, and evaluating them extremely complex. Moreover, being generative models, they can fail silently, producing hallucinations and inaccurate information. Addressing this requires a structured approach that not only includes benchmarks commonly used for machine learning but also adds several other techniques; Chapter 7 explores this topic further.

> LLM 通常拥有数百万甚至数十亿个参数。这使得训练、监控和评估它们变得极其复杂。此外，作为生成式模型，它们可能无声无息地失败，产生幻觉和不准确的信息。解决这一问题需要一种结构化的方法，不仅包括机器学习常用的基准测试，还需增加其他几种技术；第 7 章将进一步探讨这一主题。

### 2) Training Scale and Duration
**训练规模与时长**

Training LLMs requires processing large datasets. This is difficult not only from the data management perspective but also in terms of the memory and computational resources required for training the models. We discuss this in Chapter 3.

> 训练 LLM 需要处理大规模数据集。这不仅在数据管理层面存在难度，在训练模型所需的内存与计算资源方面同样面临挑战。我们将在第 3 章对此进行讨论。

Training LLMs can take days, weeks, or even months, and managing parallel and distributed training across large clusters of GPUs and TPUs requires specialized hardware and organizational skills. This means that hardware represents a major dependency on external organizations and market availability, one that requires careful, systematic planning. We discuss this in Chapter 9.

> 训练 LLM 可能需要数天、数周甚至数月时间，而跨大规模 GPU 和 TPU 集群管理并行与分布式训练，则需要专门的硬件设备与组织协调能力。这意味着硬件条件对外部机构与市场供应存在重大依赖，需要审慎且系统性地规划。我们将在第 9 章对此进行讨论。

Handling large, potentially sensitive training datasets requires careful security measures and anonymization, as discussed in Chapter 2.

> 处理大规模且可能涉及敏感信息的训练数据集，需要采取严格的安全措施与匿名化处理，相关内容将在第 2 章中阐述。

### 3) Prompt Engineering
**提示词工程**

One of the most common ways to make an LLM work better for a specific problem is prompt engineering, the science and art of crafting the text inputs that are sent to the models. Prompt updates can significantly improve or degrade the user experience. But prompt engineering is iterative and can be difficult to master and document, especially with closed-source LLMs. You'll find a discussion of this in Chapter 5.

> 让 LLM 更好地解决特定问题的最常见方法之一就是提示词工程，这是一门关于精心设计发送给模型的文本输入的科学与艺术。提示词的更新会显著改善或降低用户体验。但提示词工程是一个迭代过程，且难以掌握和记录，尤其是在闭源大语言模型中。你会在第 5 章找到相关讨论。

Updates of proprietary models, like OpenAI's GPT-4, can result in significant *model drift*, where the same inputs suddenly provide a different output due to a model update. Model drift requires effort and financial commitment to fix. This becomes additionally complex when there are many interdependent prompts connected to each other, such as in an orchestration framework (i.e., a structured platform used to automate, coordinate, and manage complex tasks and services) and there's a change in the underlying model, as the entire complex prompt chain can break in unexpected and hard-to-detect ways. If your infrastructure relies heavily on promptengineering pipelines, monitoring is crucial; Chapter 7 goes into this in more depth.

> 专有模型的更新，例如 OpenAI 的 GPT-4，可能会导致显著的 *模型漂移*，即相同的输入因模型更新而突然产生不同的输出。模型漂移需要投入精力和资金来修复。当存在许多相互依赖的提示词彼此连接时，例如在编排框架（即用于自动化、协调和管理复杂任务与服务的结构化平台）中，且底层模型发生变化时，情况会变得更加复杂，因为整个复杂的提示词链可能以难以预料且难以检测的方式断裂。如果你的基础设施严重依赖提示词工程管道，监控至关重要；第 7 章将对此进行更深入的探讨。

### 4) Inference Latency and Throughput
**推理延迟与吞吐量**

Responses provided by LLMs are also called inferences. LLMs are often deployed in applications that require real-time or near-real-time responses, which means that optimizing for speed becomes important. This can be especially complex with dynamic models like LLMs. Also, maintaining high throughput without having access to model parameters can add complexity for LLMOps teams. Edge devices used in IoT applications introduce even more challenges related to limited computational resources and varying network conditions. These issues are discussed in Chapter 9.

> LLM 提供的响应也被称为推理结果。LLM 通常部署在需要实时或近实时响应的应用中，这意味着优化速度变得至关重要。对于像 LLM 这样的动态模型来说，这尤其复杂。此外，在无法访问模型参数的情况下保持高吞吐量，可能会给 LLMOps 团队增加复杂性。物联网应用中使用的边缘设备由于计算资源有限和网络条件多变，带来了更多挑战。这些问题将在第 9 章中讨论。

### 5) Ethical Considerations

Like any other machine learning model, LLMs generate outputs based on the data that they have been trained on. LLMs applications are frequently designed to create the experience of chatting with a human instead of a machine, making them accessi‐ ble to a much larger user base than specialized machine learning systems and greatly increasing the impact of potential biases introduced by the training data.

Chapter 7 discusses techniques for monitoring LLM outputs, and the privacy and ethical implications of their use are explained in Chapter 8.

### 6) Resource Scaling and Orchestration

The scale at which LLMs operate often requires load balancing and dynamic resource scaling. Different proprietary models can also behave very differently based on the use case, and constant scenario modeling is expensive and time intensive. Chapter 5 explores how to manage dependencies across various components in distributed multi-model environments, ensuring reliability and scalability.

### 7) Integrations and Toolkits

LLMs require several new integrations and toolkits that are adapted to both genera‐ tive as well as discriminative use cases and involve communicating with various APIs. Integrating these LLMs into existing systems requires robust security protocols to prevent vulnerabilities and potential misuse. Changes in LLMs and version manage‐ ment, discussed in Chapter 8, can also lead to compatibility issues across the stack.

### 8) Broad Applicability

LLMs are adaptable and easy to use, which means that they can be applied to numer‐ ous consumer-facing applications, as we will see in Chapter 3. This makes them more likely to be exposed to untested scenarios than traditional machine learning systems, and thus they require a faster feedback loop to monitor and improve their perfor‐ mance. Chapter 7 addresses monitoring techniques.

18

Chapter 1: Introduction to Large Language Models

### 9) Privacy and Security

Collecting real-time information involves handling user data, sometimes including personally identifying information (PII). This means that security and privacy become the cornerstone of maintaining trust and regulatory compliance. This chal‐ lenge extends well beyond inference monitoring, touching the domain of cybersecurity.

Even companies such as OpenAI have received reports about database leaks into user accounts that made chat interactions visible to unauthorized users. We talk more about privacy and security in Chapter 8.

Regularly auditing your data management processes, both internally and externally, is also vital for enhancing user trust and complying with legal requirements. Best prac‐ tices for data management are discussed in Chapter 4.

### 10) Costs

One of the biggest considerations for LLMs is cost, both immediate and long-term. While most transformer models require expensive training, maintaining and scaling LLMs incurs the highest costs, especially in the inference stages. You could end up paying even for failed requests, so experimenting with model performance can become very expensive very quickly for companies building on closed and propriet‐ ary models.

Even in open source models, excessive fine-tuning can quickly lead to a phenomenon called overfitting, where the model appears to perform extremely well because it learns the training dataset but does not generalize to the unseen data that will be pre‐ sented to it by real users. There are always trade-offs between generalization ability and cost; these are explored in Chapter 5.

## Conclusion

Adopting LLMs requires careful consideration and strategic planning to navigate these intricate challenges, and organizations require a new discipline and a set of new tools to succeed. We call this discipline LLMOps, and we start our journey by defin‐ ing it in the next chapter.

## References

Dao, Tri, and Albert Gu. "Transformers Are SSMs: Generalized Models and Efficient Algorithms Through Structured State Space Duality", arXiv, May 31, 2024.

Devlin, Jacob, et al. "BERT: Pre-Training of Deep Bidirectional Transformers for Lan‐ guage Understanding", arXiv, May 24, 2019.

References

19

Haptik. n.d. "A Comprehensive Guide to Agentic AI", Accessed May 21, 2025.

OpenAI. "March 20 ChatGPT Outage: Here's What Happened", March 24, 2023.

Vaswani, Ashish, et al. "Attention Is All You Need", In NIPS'17: Proceedings of the 31st International Conference on Neural Information Processing Systems, edited by Ulrike von Luxburg, Isabelle Guyon, Samy Bengio, Hanna Wallach, and Rob Fergus (Curran Associates, 2017).

Wang, Sarah, and Shangda Xu. "16 Changes to the Way Enterprises Are Building and Buying Generative AI", Andreessen Horowitz, March 21, 2024.

20

Chapter 1: Introduction to Large Language Models

CHAPTER 2

# Introduction to LLMOps

The size and complexity of LLMs' architecture can make productionizing these mod‐ els incredibly hard. Productionizing means not just deploying a model but also moni‐ toring it, evaluating it, and optimizing its performance.

There are constantly new challenges. Depending on your application, these may include how to process data, how to store and dynamically adapt prompts, how to monitor user interaction, and—most pressing—how to prevent the model from spreading misinformation or memorizing training data (which can lead it to release personal information). That's why operationalizing LLMs, which means managing them day-to-day in production, requires a new framework.

LLMOps, as it's called, is an operational framework for putting LLM applications in production. Although its name and principles are inspired by its older siblings, MLOps and DevOps, LLMOps is significantly more nuanced. The LLMOps frame‐ work can help companies reduce technical debt, maintain compliance, deal with LLMs' dynamic and experimental nature, and minimize operational and reputational risk by avoiding common pitfalls.

This chapter starts by discussing what LLMOps is and how and where it departs from MLOps. We'll then introduce you to the LLMOps engineer role and where it fits into existing ML teams. From there, we'll look at how to measure LLMOps readiness within teams, assess your organization's LLMOps maturity, and identify crucial KPIs for measuring success. Toward the end of this chapter, we will outline some chal‐ lenges that are specific to productionizing LLM applications.

21

## What Are Operational Frameworks?

Operational frameworks provide a structured approach to managing complex work‐ flows and pipelines within an organization. These frameworks integrate tools and practices to automate and streamline organizational processes and ensure consistency and quality across the project lifecycle.

Some of the earliest operational frameworks can be traced back to military strategy and the Industrial Revolution. Two of the most popular ones, both introduced in 1986, are Toyota's Lean Production System, which put Toyota ahead of most of its contemporaries, and Six Sigma, Motorola's data-driven approach to improving pro‐ cesses and reducing defects.

In 2008, the tech industry began to adopt what is now one of the most popular opera‐ tional frameworks in software: DevOps. (The term combines software development and operations.) In 2018, MLOps, an operational framework for non-generative machine learning (ML) models, became the talk of the town; since then we've seen SecOps (Security Operations), DataSecOps, and many more.

With the massive adoption of LLMs in 2023, a new operational framework started floating around within companies that were building LLM applications: LLMOps. LLMOps is still in its infancy, but as generative models become integral to software products, its popularity is likely to boom.

Figure 2-1 shows the slow rise of Ops frameworks over the years. Use of LLMOps started to pick up with the mass adoption of LLMs in early 2023. As of this writing, more and more enterprises are realizing that they can add value and profit with LLMbased offerings, leading to an upward trend for LLMOps. In fact, 2025 may be the best year yet for LLMOps frameworks.

Deploying LLMs can be as simple as integrating a chatbot into your website via an API or as complicated as building your own LLM and frontend from scratch. But maintaining them to be performant (productionizing them)—that is, keeping them reliable, scalable, secure, and robust—is a massive challenge. This book, like LLMOps, is focused on exactly this question: what happens after you deploy your LLM in production?

22

Chapter 2: Introduction to LLMOps

Figure 2-1. Google Ngram showing the rise in popularity of the term LLMOps from 2019 to 2024

/c7030bb07abc26fda04e4784134eaa66e85f59a648179fc2c3a68ee47fcf312d.jpg

## From MLOps to LLMOps: Why Do We Need a New Framework?

There is some overlap between MLOps and LLMOps; both deal with the operational lifecycles of ML models, after all. They also share common principles in terms of managing ML workflows. However, the two frameworks diverge in their primary focuses and objectives. While MLOps handles non-generative models (both language and computer vision), LLMOps deals with generative language models—and thus with mammoth levels of complexity. The complexity of these models owes not only to their scale and architecture but also to the unique processes involved in data engi‐ neering, domain adaptation, evaluation, and monitoring for them. The key distinc‐ tions are apparent in LLMs' prediction transparency, latency, and memory and computational requirements.

What Are Operational Frameworks?

23

Perhaps the biggest difference is the shift in how end users consume these models. Non-generative ML models are predictive tools used for passive consumption, such as in dashboarding, recommendations, and analytics. By contrast, LLM applications are deployed as Software 3.0 in consumer-facing applications for active user interac‐ tion. This brings several challenges from Software 1.0 (DevOps) back to the surface. In fact, it wouldn't be wrong to say that LLMOps shares more similarities with DevOps than with MLOps.

Building your own generative AI application requires tools, frameworks, and expecta‐ tions to match the scale and complexity of these models, and this is far beyond the scope of the existing MLOps solutions. To help you understand the differences between the various kinds of Ops frameworks, let's do a thought experiment.

Imagine MLOps as being something like building a small home from the ground up. In comparison, DevOps, which deals with the entire product lifecycle, would be like developing a large shopping complex. And LLMOps? It's more like building the Burj Khalifa. For all three frameworks, you are working with the same construction mate‐ rials: wood, steel, concrete, bricks, hammers, and so on. Much of the basic process is the same, too: you lay down the foundation, lay down the plumbing, and finally build the walls. But you wouldn't contract your local construction workers to engineer the Burj Khalifa, would you?

Most of MLOps for natural language modeling is based on building smaller, discrimi‐ native models for tasks like sentiment analysis, topic modeling, and summarization. For these tasks, you first hypothesize ideal features, model your data as a function of those features, and then optimize the model for that specific task.

LLMs, by contrast, are generative, domain agnostic, and task agnostic. That funda‐ mental difference means you can use the same model for summarizing or for answer‐ ing questions, without having to fine-tune it.

The best use cases for LLMs are when you don't know what features to optimize for (or, even better, if the features are too abstract) and when you need to model multi‐ modal data within a single pipeline. Unlike smaller discriminative models, LLMs don't rely on predefined features or task-specific architectures. Instead, as you learned in Chapter 1, they are trained on vast amounts of text data to learn the patterns and structures in language itself. For LLMs, the training process involves a loss function, which measures how well the model's generated outputs match the expected outputs across various tasks. For example, during training, the model might generate a sequence of text; the loss function calculates the difference between this generated sequence and the target sequence.

Additionally, for a standard comparison, the hyperparameter space for a 175-billion parameter GPT-4 model would likely be approximately 1,500 times larger than that for a standard discriminative BERT model (which has 110 million parameters). This makes it incredibly costly to fine-tune and do the kind of iterative training that is typ‐ ical in MLOps. Table 2-1 outlines some of the key differences between the MLOps and LLMOps model lifecycles.

24

Chapter 2: Introduction to LLMOps

Table 2-1. Comparing the MLOps and LLMOps model lifecycles

|   |   |   |   |
|---|---|---|---|
|Lifecycle step|Context|MLOps LLM0ps|   |
|Data collection|Ease|Always and straightforward.|Sometimes—data composition is a very hard problem.|
|Datapreprocessing|Ease|Fix missing data and outliers—very easy!|Hard. Requires:· Deduplication·Toxicity fltering·Diversity management· Quantity control|
|Model learming|Model size|MLmodels,such as classifers orregressors,typically have at maxaround 2oo million parameters andare generally less computationallyintensive for experimentation thanare LLMs.|LLMs typically have 10o billion or even trillions ofparameters, making them significantly larger andmore complex than many non-generative models.Their masive scale impacts resource requirements,storage,and computational efficiency.|
|Hyperparameters|Accuracy|Limited hyperparameter spacemakes search easy,making themideal forpredictive problems.|Massive hyperparameter space leads to real-timesearch latency.This makes them ideal forgenerativeand evolutionarytasks that requirecreativity.Accuracy can be a computationalbottleneck.|
|Model trainingduration|Trainingscale andduration|Less resource intensive andgenerallyfaster. Canbe easilydeployed as notebooks on thecloud or as containerized solutionsacross a single node.|Involves processing massive datasets withdistributed training across large clusters of GPUs orTPUs and optimizing for parall processing. Cantake days or weeks.Operationalizing may requiredynamic resource scaling and involves designingscalable infrastructure and orchestration systems tohandle varying workloads efficiently.|
|Domainadaptation|Cost|Fullfine-tuning is essentialandaffordable.|Fullfine-tuning is too expensiveand pretyrare.Instead,popular techniquesare:·Prompt engineering·RAGs· Knowledge graphs·Parameter-efficint fine-tuning|
|Evaluation|Ease|·Easy· Discriminative·Well-efined probability space|·Extremely hard problem·Generative andthus hard todetect·Unbounded probability space|
|Robustness|Staticversusdynamic|Model behavior stays the same inproduction.|Model behavior changes in production based oninteractions and requires constant monitoring foralignment.|
|Security|Secure|Highly secure.|·Highly vulnerable·Needsa DataSecOps framework|

What Are Operational Frameworks?

25

## Four Goals for LLMOps

LLMOps operates on an LLM-specific set of design pattern principles to ensure that your LLM applications achieve four key goals: security, scalability, robustness, and reliability. Let's take a closer look at these goals:

## Security

Minimizing the regulatory, reputational, and operational risks associated with deploying LLM applications in production

## Scalability

Building, storing, and maintaining LLM applications that can generalize across data and scale efficiently on demand while optimizing latency, throughput, and costs

## Robustness

Maintaining high performance of LLM applications over time in the face of data drift, model drift, third-party updates, and other challenges

## Reliability

Implementing rigorous inference monitoring, error handling, and redundancy mechanisms to prevent downtime and failures

LLMOps teams automate repetitive processes to more quickly optimize these applica‐ tions at scale and avoid those "LLM-oops!" moments. Another key aspect of the LLMOps framework is fostering consistency, transparency, and collaboration between diverse interdisciplinary teams. These teams often include data engineers, data scientists, research scientists, software engineers, and business operations teams.

LLMOps is an entirely new field, so, as of this writing in 2025, there are very few mature tools and resources available. The LLMOps teams at various organizations are thus developing their tools and processes internally, based on prototypical open source libraries and toolkits.

## LLMOps Teams and Roles

Today, there are two kinds of companies out there building with LLMs: the newer startups, which focus primarily on LLM applications, and companies with existing ML models that are now building their own GenAI teams.

In the latter category, there are so few skilled Ops professionals that most companies recruit ML engineer candidates internally and then upskill them to LLMOps, instead of hiring externally. A major reason for this is a general lack of clarity around use cases as well as the expected job responsibilities. So the current norm is to hire 8 to 10 people internally from different departments, which could include product managers, full-stack engineers, system architects, data engineers, data scientists, ML engineers, platform engineers, cybersecurity professionals, and developer advocates. Many com‐ panies want someone who already understands the business inside and out to test the feasibility of several potential use cases and projects before committing to one.

26

Chapter 2: Introduction to LLMOps

Newer startups, however, have no choice but to build a team from the ground up. These teams can look very different, depending on whether they are working on LLMOps infrastructure (LLMOps SaaS companies) or LLM use cases such as copy‐ writing, education, or process optimization. Figure 2-2 provides a very basic model of an LLMOps team, but these teams come in all shapes and sizes, with different levels of business and technical maturity. (Later in the chapter, we'll look at how to assess your company's LLMOps maturity.)

![image](file:///C:/0b6a8a13d6e48a5a36103a838e2a6fd8bf6ae152b9a6084ce75788711522c5d3.jpg)

Figure 2-2. Structure of an LLMOps team

Most companies cannot afford the cost of building and training an LLM for use in their application. Instead, most choose to use a foundational model. This is where AI engineers come in: to build a quick proof of concept using LLMOps tools. Most come from a software-engineering background; they may know how to build a full-stack application quickly, but don't necessarily have a deep understanding of ML/LLM models' inner workings or how to optimize them.

LLMOps Teams and Roles

27

Once the proof of concept is completed, building, deploying, and optimizing ML models for the business falls to LLM engineers, ML scientists (interchangeable titles, depending on the organization), and LLMOps engineers tasked as reliability engineers.

If a team chooses to deploy an LLM application using API integration, the initial deployment will be pretty straightforward. The LLMOps engineers work alongside AI engineers to scale the model and improve its performance. Ideally, each AI engineer is paired with an LLMOps engineer; the AI engineer can focus on adapting and finetuning the model to meet the business needs, while the LLMOps engineer manages deployment and optimization. For open source models, managing deployment auto‐ matically falls to the LLMOps engineer.

As the tech industry moves from non-generative models to generative models, it is shifting away from feature engineering, or creating features to model the data and experimenting with different hyperparameters to optimize performance. Generative models, and specifically LLMs, do not require feature engineering. Today, the core requirements are usually prompt engineering or building a RAG pipeline—skills that lie within the domain of AI engineers.

Another big shift is that the data engineering pipeline and the monitoring and evalu‐ ation pipeline have become far more complex. Evaluating LLMs is much more than straightforward quantitative scoring. Some industry benchmarks exist—like BLEU, a benchmark used to evaluate machine translation, and ROUGE, a benchmark used to evaluate summarization, but these are only loosely correlated with application perfor‐ mance. Moving to a model that has a better score is no guarantee of better user satis‐ faction. Standardized scores may be good for comparing LLMs in general, but ultimately users care about whether the LLM application is solving their problem.

In addition, since LLMs are deployed in consumer-facing applications, metrics like perceived latency and throughput become make-or-break factors in market competi‐ tion. The model is not the only deciding factor: the deployment, evaluation, and monitoring pipelines are also at the front and center of performance assessment.

Let's look at some of the roles involved in these pipelines:

## Data engineer

Data engineers are professionals responsible for designing, building, and main‐ taining systems and pipelines that enable the efficient collection, storage, and transformation of data as well as access to it. Their work ensures that data is available, reliable, and organized in a way that allows data scientists and other engineers to create and evaluate models and data-driven applications. Data retrieval and movement are the most fundamental skills for data engineers, but as they progress in their career, developing data architectures becomes more important.

28

Chapter 2: Introduction to LLMOps

Data engineering for LLMs requires specialized understanding: how to chunk the data, what tokenization model to use, and so on. Thus, it's best to pair each data engineer with an ML scientist (with an LLM engineering background) along with the LLMOps engineer for automating and streamlining LLM systems at scale.

## AI engineer

The core skill set of an AI engineer is full-stack engineering and development (React, Node.js, Django) plus familiarity with the common LLMOps tools and frameworks for deploying applications, like LangChain and Llama Index. They need a foundational understanding of end-to-end AI application development, including prompt engineering and RAG systems. Companies building their teams from scratch usually look to hire AI engineers who also know a lot about using cloud services to deploy and manage AI applications and have experience working with external APIs and vector databases.

## ML scientist

The day-to-day work of an ML scientist, NLP scientist, or LLM engineer involves researching, designing, and optimizing LLMs using frameworks like PyTorch, TensorFlow, and JAX. This role requires a deep understanding of NLP algorithms and tasks, such as tokenization, named-entity recognition (NER), sentiment anal‐ ysis, and machine translation. Candidates should know model architectures and training and fine-tuning processes.

## LLMOps engineer

The goal of an LLMOps engineer is to ensure that LLM applications remain reli‐ able, robust, secure, and scalable. The day-to-day work involves building and maintaining operational LLM pipelines as a project owner.

Let's now look at the LLMOps engineer role in more detail.

## The LLMOps Engineer Role

This role requires extensive expertise in deploying, monitoring, fine-tuning, training, scaling, and optimizing LLM models in production environments; infrastructure and platform engineering; data engineering; and system reliability.

Companies building LLM teams usually seek LLMOps engineers who understand the unique challenges associated with LLMs and are experienced in making build-versusbuy trade-off, including by weighing cost efficiency against system performance.

To stand out as a candidate for this role, you'll need proficiency in a unique blend of specialized skills and a deep technical understanding of the entire LLM lifecycle, from data management to model deployment and monitoring. You'll also need to be a problem solver, a strong team player, and an effective communicator as well as metic‐ ulously detail oriented.

LLMOps Teams and Roles

29

To illustrate what this means in practice, let's look at a typical day in the work life of a fictional LLMOps engineer.

## A Day in the Life

While the specific responsibilities for this role will vary across organizations, the core tasks typically encompass a blend of infrastructure management, collaboration, opti‐ mization, and compliance. To give you a quick taste of what this looks like in practice, here's what a typical LLM engineer's workday might look like:

## 7:30 AM–8:30 AM: Morning check-in

• Review monitoring dashboards for any overnight alerts or performance issues in deployed LLMs; address any urgent issues or escalate them to the appropriate teams.

• Lead the team's daily stand-up meeting to discuss ongoing projects, blockers, and priorities for the day.

8:30 AM–10:00 AM: Infrastructure management and optimization

• Modularize code for reusability , creating separate modules for provisioning GPUs, managing storage, and networking.

• Implement batching mechanisms to process multiple inference requests, reduc‐ ing the per-request overhead.

• Implement latency optimization techniques like kernel fusion, quantization, and dynamic batching to enhance model performance.

## 10:00 AM–11:30 AM: Collaboration and project planning meeting

• Meet with data scientists, ML engineers, and red teaming engineers to discuss usage requirements, timelines, monitoring errors, and scaling challenges.

## 11:30 AM–12:30 PM: API development and model deployment

• Design inference endpoints and cache for different models in production, ensur‐ ing compatibility with the rest of the application.

## 12:30 PM–1:30 PM: Lunch break

1:30 PM–3:00 PM: Monitoring and troubleshooting

• Troubleshoot any issues that arise. For example, let's say the users are experienc‐ ing long delays when making requests to the inference API. The engineer would identify the source of latency by examining hardware utilization and network latency and reviewing usage logs. They would then implement a solution; e.g., using a Pod Autoscaler or caching the frequent requests.

## 3:00 PM–4:30 PM: Research and continuous learning

• Experiment with new tools, libraries, or frameworks that could be integrated into the existing tech stack to improve efficiency and performance.

30

Chapter 2: Introduction to LLMOps

4:30 PM–5:30 PM: End-of-day wrap-up, review, and on-call prep

• Review the day's tasks and update the tickets with completed tasks and next steps.

• Prepare for any on-call duties, ensuring that all monitoring systems are correctly configured and that you're ready to respond to any incidents.

• Attend any final meetings or syncs with cross-functional teams to ensure align‐ ment on upcoming priorities.

• Wrap up any remaining tasks and make sure that all systems are running smoothly before logging off for the day.

After regular working hours, if you are on call, you'll need to remain available to address any critical issues that may arise.

## Hiring an LLMOps Engineer Externally

There are two ways to fill an LLMOps engineer role: you can hire externally, or you can hire internally and upskill your people, training ML engineers to become LLMOps engineers. This section will look at external hiring first and then discuss how to upskill current employees.

If you're hiring for this role, other skills to look for in candidates for LLMOps engi‐ neering roles include experience or proficiency in:

• Converting models to and from libraries like PyTorch or JAX

• Understanding ML metrics like accuracy, precision, recall, and PR-AUC

• Understanding data drift and concept drift

• Running and benchmarking models to understand the impact of computational graph representation on performance across the neural engine, GPU, and CPU

• Deploying and scaling ML models in cloud environments like AWS, GCP, and Azure

• Using LLM inference latency optimization techniques, including kernel fusion, quantization, and dynamic batching

• Building Ops pipelines for data engineering, deployment, and infrastructure as code (IaC) using tools like Terraform, managing vector databases, and ETL pro‐ cesses for large-scale training datasets

• Understanding red-teaming strategies, interfaces, and guidelines

• Using Docker for containerization and Kubernetes for orchestration to ensure scalable and consistent deployments

• Collaborating on and managing projects with teams that include LLM engineers, data scientists, and ML/NLP engineers

LLMOps Teams and Roles

31

Every company, of course, has its own interviewing process. Some conduct many rounds of interviews; others combine several of the interviews into a single on-site meeting. This section describes a fairly standard four-round interview process, as pic‐ tured in Figure 2-3.

![image](file:///C:/1d4df26fd9aff495f088eaa7afd01fe508bc9910880e27c919ce0594f812d3f6.jpg)

Figure 2-3. Components of an LLMOps interview

Let's look at each round in more detail:

## Round 1: Initial screening

The goal during initial screening is to determine that the applicant has the funda‐ mental skills and experience required for the role. This can be assessed via a resume assessment sheet. The questions you're asking here are very high level. Do they have experience with deploying LLMs in production environments? Do they mention specific frameworks and tools for managing LLM pipelines, and are these the same tools your company uses? If not, will they be able to learn and adopt your stack? Can they show or talk about any past projects?

## Round 2: Technical assessment

The goal in this round is to assess the candidate's technical proficiency in core areas such as LLM deployment, data engineering, and infrastructure manage‐ ment. Some questions you might ask include:

• Describe the steps you take to fine-tune a pretrained large language model. How do you ensure that the model is optimized for the specific use case?

• Walk me through the deployment process of an LLM you've worked on. What challenges did you face? How did you overcome them?

• How would you set up a CI/CD pipeline for LLM training, fine-tuning, and deployment?

• How do you design and manage data pipelines for large-scale ML projects? What tools do you use, and how do you ensure data quality?

• How do you monitor and troubleshoot latency issues in production?

• How do you handle versioning and tracking datasets used in training or finetuning LLMs?

32

Chapter 2: Introduction to LLMOps

• How do you ensure high availability and cost-efficiency in your cloud infra‐ structure?

## Round 3: System design interview

The goal in this round is to assess the candidate's ability to design scalable, relia‐ ble, and maintainable systems for deploying and managing LLMs. Sample ques‐ tions for this round could include:

• Tell me about a time when you had to make a build-versus-buy decision for a component of your ML infrastructure. What factors did you consider?

• How would you design an API for serving LLM inferences at scale? Discuss considerations for load balancing, fault tolerance, and latency reduction.

• How would you use an IaC tool to manage the cloud infrastructure for an LLM deployment? What strategies would you employ to optimize resource usage and cost? What potential problems do you think you'd encounter while scaling it?

• Describe your approach to dynamic batching in inference service. How do techniques like quantizing and mixed precision training affect the perfor‐ mance and efficiency of LLMs?

• How do you manage memory in CUDA when training LLMs? What strate‐ gies do you use to prevent issues like out-of-memory errors?

• How do you benchmark model performance before and after optimization? What metrics do you consider, and what tools do you use?

• How would you diagnose and address performance degradation after an optimization?

## Final round: Behavioral interview

In the fourth round, you've narrowed the pool to the most qualified candidates. Now you need to assess their personalities: Are they self-driven? Can they work in a team, handle challenges with equanimity, and contribute to a collaborative environment? Sample questions:

• How do you stay up-to-date on the latest advancements in LLMs and machine learning operations?

• How do you approach integrating data scientists' feedback into the deploy‐ ment process?

• How would you collaborate with a red-teaming engineer to address potential security vulnerabilities in an LLM deployment?

• What experience do you have with on-call rotations? How do you handle critical incidents during off hours?

LLMOps Teams and Roles

33

You'll also want to ensure the candidate aligns with your organization's values, particularly in areas like innovation, continuous learning, and collaboration. You can ask questions like:

• What are your favorite technology blogs or podcasts?

• How do you keep up with new advances in the field?

## Hiring Internally: Upskilling an MLOps Engineer into an LLMOps Engineer

The gap between MLOps engineers and LLMOps engineers is significant in terms of the scale, complexity, and the technical challenges involved in their roles. Thus, upskilling an existing employee requires a focused effort to build their understanding.

That said, the foundational skills of MLOps—such as model deployment, automation, and cloud management—provide a solid base from which to grow. With dedicated learning and hands-on experience, an MLOps engineer can transition into the LLMOps domain effectively. The core upside of hiring internally is that candidates are already aligned with the organization's values and culture and have a keen under‐ standing of its KPIs.

To excel, new LLMOps engineers need resources and training to deepen their under‐ standing of large-scale model architectures and transformer architectures, attention mechanisms, infrastructure management, and LLM-specific optimization techniques. They also need to understand how LLMs differ from non-generative ML models. We recommend pairing them up with LLM engineers to experiment with and evaluate different models.

This role isn't just about building an app that uses LLMs. LLMOps engineers also manage the balance among cost, cloud resources, and user experience and handle huge unstructured datasets. Therefore, pair them with data engineers to help build a data-processing pipeline so they can familiarize themselves with the data sources at their disposal, how the data is structured in the databases, how different databases retrieve information, what the company's latency expectations are, and how to handle data filtering. Allow them to introduce multi-node setups and distributed systems for different models while focusing on cost optimization and errors. Get them to bench‐ mark different LLM models and debug their performance optimization. Finally, allow them to present their logging practices and the guardrails they have set up for main‐ taining reliability and performance at scale.

Most MLOps engineers already have skills in model versioning, data versioning, managing rollbacks, and GitHub actions, so upskilling these professionals can be an effective strategy for building a strong LLMOps team.

34

Chapter 2: Introduction to LLMOps

Next, let's look at how to make sure the goals of your LLMOps engineers are aligned with your organizational goals.

## LLMs and Your Organization

You learned at the beginning of this chapter that the four key goals of the LLMOps framework are security, scalability, robustness, and reliability. For LLMOps teams, then, the next big question is how to measure the application's performance against those goals. How will you know you're succeeding? The company's expectations should be clearly defined and remain quantitatively, as well as qualitatively, measura‐ ble at all times.

Three kinds of metrics will allow you to measure your team's performance toward its goals: SLOs, SLAs, and KPIs. These terms are in common usage among site reliability engineers, and now LLMOps teams are rapidly adopting them as well:

## Service-level objectives (SLOs)

Service-level objectives are specific, measurable targets set by an organization to gauge the quality of its services internally. They define what level of service the organization aims to achieve. For example, an SLO for a cloud-hosting company might be to ensure that server uptime is at least 99.9% per month.

## Service-level agreements (SLAs)

Service-level agreements are formal contracts between a service provider and a customer that define the level of service the provider commits to deliver. They typically include specific performance goals and stipulate remedies if those met‐ rics are not met. For example, if the uptime for an internet provider falls below 99.9% annually, the SLA might stipulate that the customer will receive a 10% dis‐ count on its next billing cycle.

## Key performance indicators (KPIs)

Key performance indicators measure the overall success and performance of spe‐ cific business activities. They provide insight into how well the organization is achieving its strategic objectives. For example, an important KPI for an app might be its churn rate or the percentage of customers who stop using the app over a certain period.

LLMs and Your Organization

35

In August 2024, a Gartner Research study predicted that 30% of existing GenAI projects would fail by 2025. (In fact, Gartner published similar findings in 2018, predicting that 85% of ML projects would fail in production by 2022.) The key failure points outlined in the 2024 study are notable because they are the operational aspects of LLM development and deployment—including data quality issues, the lack of a strong evaluation framework, and the high costs of scaling these models in production.

That said, one of the most obvious issues is mismatched expectations between man‐ agement and engineering teams. For the last 10 years, one of data scientists' biggest skill gaps has been in translating ML model metrics into organizational and product success metrics. In other words, when you're measuring abstract goals like model security, scalability, robustness, and reliability, how do you communicate what this means for the business? That's what SLOs, SLAs, and KPIs are for.

Using an SLO-SLA-KPI framework allows LLMOps teams to automate, streamline, and manage expectations across multiple stakeholders. SLOs make it evident to all stakeholders what level of service is being aimed for. SLAs ensure accountability so that everyone involved is aware of their roles and the agreed-upon service levels. This can also help you track performance and address any deviations from the expected standards. And KPIs provide visibility into real-time data to help detect potential issues early, facilitating informed decision-making.

## The Four Goals of LLMOps

Let's look more closely at the LLMOps goals to see how these metrics translate.

## Reliability

As you know well by now, LLMs are extremely complex, with billions of parameters. Their behavior can be unpredictable, and they sometimes exhibit unexpected respon‐ ses or errors due to their scale and the intricacies of their training data. Additionally, if the training data is biased, outdated, or unrepresentative of certain domains, the model's performance can be unreliable in those areas.

LLMs also struggle at times with understanding the context, nuance, and intent behind user queries. This can lead to incorrect, irrelevant, or misleading responses. What's more, LLMs usually aren't updated in real time. As language evolves, if new information is not integrated into the training data via regular retraining, models can become outdated, leading to decreased reliability.

All of these issues come down to reliability. The reliability of LLM-based applications can be measured in terms of system availability, error rates, and customer satisfac‐ tion. Table 2-2 shows how these metrics would look as SLOs, SLAs, and KPIs.

36

Chapter 2: Introduction to LLMOps

Table 2-2. Example reliability comparison of SLOs, SLAs, and KPIs

|   |   |   |   |
|---|---|---|---|
|SLO SLA KPI|   |   |   |
|Availability|Maintain 99.9% uptimeper month|Ensure that the system is available for atleast 99.95%of requests overarolling 30-day period|Customer satisfaction score (CSAT)related to systemavailability|
|Error rate|Keep the error rate below0.1% for all APl requests|Ensure that less than 1%of userinteractions result in errors|Track error rate trends over timeand analyze root causes of majorerrors|
|Customersatisfaction|CSAT score of at least90%|Ensure that the net promoter score (NPS)remains above 8|Post-interaction surveys orfeedback forms; CSAT score|

## Scalability

LLMs tend to have a large memory footprint, often exceeding the capacity of a single machine. Distributing a model across multiple GPUs or nodes while maintaining per‐ formance is technically challenging. Handling large volumes of data efficiently is critical.

Another significant challenge is scaling the data pipeline to feed data into the model at the required speed without causing bottlenecks. This can be especially hard for applications like chatbots or interactive services, where low latency is crucial. Scaling while keeping response times low can be challenging, since scaling up increases resource contention and network overhead. Therefore, balancing performance with cost efficiency is a constant concern.

LLMOps scalability can be measured via metrics like latency, throughput, response time, resource scaling, capacity planning, and recovery time objective (RTO), as shown in Table 2-3.

Table 2-3. Example scalability comparison of SLOs, SLAs, and KPIs

|   |   |   |   |
|---|---|---|---|
|SLO SLA KPI|   |   |   |
|Latency|Serve 95% of requests within 200milliseconds|Keep the average response time forAPl cals under 100 milliseconds|Average response time foruser interactions|
|Throughput|Process a minimum of 1,0o requestsper second during peak traffic hours|Handle at least 1 million concurrentconnections without degradation|Peak throughput capacityduring load testing|
|Responsetime|Maintain a web page load time ofunder 3seconds for 95%of users|Ensure that the login processcompletes within 500 milliseconds for99% of users|User experience metricsrelated to response times|
|Resourcescaling|Automatically scale up resourcesto handle a 50% increase intraffic within 5 minutes|Ensure thatadding servers linearlyincreases throughput withoutimpacting latency|Scalability test results andcost-effectiveness ofscaling solutions|
|Capacityplanning|Maintain CPU utilization below80% during peak hours|Ensure that enough databaseconnections are available to handledouble the anticipated peak load|Resource utilization trendsand forecasting accuracy|
|SLO|   |SLA|KPI|
|RTO|Achievearecovery timeobjective of under30 minutes for critical system failures|Ensure that the system can recover from a database failure and restore service within 15 minutes|Historical RTO metrics and improvement initiatives|

The Four Goals of LLMOps

37

## Robustness

Over time, the statistical properties of the model's training data can change, leading to a drift in the model's performance. This is particularly problematic for models that interact with real-time or rapidly changing data. This can lead to performance degra‐ dation in the form of outdated or irrelevant responses.

Continuous training and fine-tuning are necessary to maintain robustness, but they require significant computational resources and careful management to avoid intro‐ ducing new biases or errors. You can measure robustness via metrics like data fresh‐ ness, model evaluation, and consistency, as shown in Table 2-4.

Table 2-4. Example robustness comparison of SLOs, SLAs, and KPIs

|   |   |   |   |
|---|---|---|---|
|SLO SLA KPI|   |   |   |
|Datafreshness|Ensure thatdashboard dataisrefreshed every 5 minutes|Guarantee that data is updated inreal time|Data refresh latency andaccuracy of real-time dataupdates|
|Modelevaluation|Maintaina performancedegradationrate of less than 5% over 6 months|Guarantee regular updates andreviews of model evaluationmetrics|Accuracy, relevance,andupdate frequency ofevaluation metrics|
|Consistency|Guarantee strong consistency for datareads and writes across all regions|Maintain eventual consistencywith a maximum propagationdelay of 1 second|Consistency model adherenceand replication latency|

## Security

Maintaining LLM application security is challenging: these are complex models han‐ dling sensitive data in the face of constantly evolving security threats. LLMs are espe‐ cially vulnerable to adversarial attacks, data poisoning, and other forms of exploitation that can compromise their integrity and security.

Managing and controlling access to the LLM and its data is complicated, especially in a multi-access or multi-tenant environment, but it's critical for preventing unauthor‐ ized access and misuse. Table 2-5 shows some ways to measure it.

38

Chapter 2: Introduction to LLMOps

Table 2-5. Example security comparison of SLOs, SLAs, and KPIs

|   |   |   |   |
|---|---|---|---|
|SLO SLA KPI|   |   |   |
|Dataprivacy|Ensuredataencryption forallin-transit and at-rest data|Ensure no breaches occur|Encryption compliance status|
|Model integrity|Detect and address any modeltampering within 24 hours|Guarantee prompt detection of andresponse to unauthorized modifications|Number of unauthorizedmodifications detected|
|Accescontrol|Achievea user authenticationsuccess rate of 9.9%|Ensure robust user authenticationand authorization mechanisms|Rate of unauthorized access attempts|
|Redteaming|Ensure detection of 99.9% ofattempted adversarial attacks|Ensure regular security assessmentsand updates|Frequency of securityasessments and the number ofcritical vulnerabilities identified|

When all teams—whether they are involved in development, operations, or manage‐ ment—understand the agreed-upon service levels and performance indicators, they can work together more effectively toward common goals. This alignment fosters a unified approach to managing and improving project performance. It also helps in making data-backed decisions about resource allocation, process changes, and strate‐ gic adjustments. Most importantly, it helps in building trust and ensuring that every‐ one is on the same page regarding expectations and outcomes.

Overall, implementing an SLO-SLA-KPI framework not only enhances transparency and fosters collaboration, but it also serves as a foundational element in evaluating and advancing the maturity of your LLMOps practices, which is the topic of this chapter's final section.

## The LLMOps Maturity Model

LLMOps maturity is a way of determining how well an organization's LLM operations align with industry best practices and standards. Assessing LLMOps maturity helps organizations identify their strengths, areas for improvement, and opportunities for scaling and enhancing the robustness of their LLM systems.

A few years ago, Microsoft published a machine learning operations maturity model detailing a progressive set of requirements and stages to measure the maturity of MLOps production environments and processes. The LLMOps maturity model we present here, inspired by Microsoft's MLOps model, is meant to do the same for LLMOps teams. Although this is by no means a comprehensive audit, we hope to see several variations put into practice.

The LLMOps Maturity Model

39

The three LLMOps maturity levels are as follows:

## Level 0

No LLMOps practices are implemented. The organization's lack of formal struc‐ tures and processes for managing and deploying its LLM systems hinders its effectiveness.

## Level 1

The organization applies MLOps practices but without LLM-specific adaptations. This is an improvement over Level 0 in terms of formalization and processes but still lacks the sophistication needed for full LLM operations.

## Level 2

Achieving Level 2 represents a mature LLMOps state, characterized by advanced documentation, robust monitoring and compliance measures, and the integra‐ tion of sophisticated orchestration and human review strategies. Usually, this can be assessed by asking some questions about whether decision strategies and model performance measures and metrics are well documented within the team.

Various measures of LLMOps maturity levels are outlined in Table 2-6.

Table 2-6. Documentation and strategy measures of LLMOps maturity

|   |   |   |   |
|---|---|---|---|
|Level 0:No LLM0ps|   |Level 1: Level 2:MLOps, no LLMOpsFull LLM0psFull documentation with regular updates; KPlsinclude model performance metrics,operational efficiency,and cost-effectiveness|   |
|Are the business goals and KPls ofthe LLM project documented andkept up to date?|Not documented||
|Are LLM model risk evaluationmetrics documented?|No formal riskassessment|Basic risk evaluationfor model accuracyand data security|Comprehensive risk evaluation including bias,fairness,data drift,and performancedegradation with mitigation strategies inplace|
|Is there a documented andregularly updated overviewofallteam members involved in theproject, along with theirresponsibilities?|Nodocumentation|High-level roles aredocumented,butresponsibilities maybe unclear for thenewer roles|Detailed team structure with roles,responsibilities,and contact details that isregularly reviewed and updated|
|Is the choice of LLM welldocumented and cost-comparedagainst other open source/proprietary offerings?|Nodocumentationor cost analysis|Basicdocumentation ofLLM choice, minimalcost comparison|Detailed documentation including rationalefor choice,performance benchmarks,and costcomparison against alternative models|
|Is the API for the model vendorwell documented,indudingrequest and response structure,data types,and otherrelevantdetails？|No APIdocumentation|Model developed in-house|Comprehensive APl documentation, includingrequest/response examples,data types,errorcodes,and versioning details|
|Level 0:|   |Level 1: Level 2:MLOps, no LLMOpsFull LLM0ps|   |
|No LLM0ps|
|Is the software architecture welldocumented and kept up to date?|Nodocumentation|There is a high-levelarchitectureoverview, but it maybe outdated|Detailedarchitecture diagrams indluding dataflow,system components,and integrationpoints that are updated regularly|

40

Chapter 2: Introduction to LLMOps

Documenting the factors shown in Table 2-6 can be incredibly helpful when choosing and deploying any new model. For example, given the significant costs that are asso‐ ciated with deploying an LLM application, cost-benchmark analysis documentation allows the company to decide which model to roll into production and estimate the project timeline.

After deployment, the company also needs to assess how well the team has docu‐ mented the model's performance measures and metrics. This is to make sure that everyone on the team understands the expectations and that they are comprehen‐ sively monitoring the model performance in production.

Table 2-7 outlines three levels of LLMOps maturity with regard to model perfor‐ mance and evaluation. Keeping these different levels in mind, organizations and the LLMOps team will be better prepared to deal with contingencies and can better align projects with business goals, mitigate risks, and enhance operational efficiency.

Table 2-7. Model performance and evaluation measures of LLMOps maturity

|   |   |   |   |
|---|---|---|---|
||Level 0:No LLM0ps|Level 1:MLOps, no LLMOps|Level 2:Full LM0ps|
|Does the LLM system operatewithin its knowledge limits,andrecognize when it is operatingoutside those limits?|No mechanisms todetect limits|Basic detection ofoperational limits|Advanced guardrails,limit detectionmechanisms,and documentation ofcontext-aware warnings usingtechniques ike confidence scoringand thresholding|
|Are the LLM's inputs and outputsautomatically stored?|No automaticstorage|Basic storage of inputsand outputs|Automated storage of all inputs andoutputs with indexing for easyretrieval and analysis|
|Is A/B testing performed regularly?|No A/B testing|Occasional A/B testingwith limited coverage|Regular A/B testing withcomprehensive test coverage andanalysis,using tools likeOptimizelyorcustom frameworks|
|Are all APl requestsand responseslogged,and are APl response timeand health status monitored?|No logging ormonitoring|Basic logging andresponse timemonitoring|Comprehensive logging with detailedrequest/response analysis; real-timehealth monitoring using tools like ELKstack|
|Level 0: Level 1: Level 2:No LLM0ps MLOps, no LLMOps Full LLM0ps|   |   |   |
|Is the LLM monitored for toxicityand bias?|No outlier detectionor bias monitoring|Basic outlier detectionwith manual review|Advanced automated toxicity andbias detection pipelines usingstatistical methods and regular biasaudits,with automated alerting forlow-confidence predictions|
|Are processes in place to ensurethat LLM operations comply withregulations sSuch as GDPR, HIPAA,and other relevantdata protectionlaws?|No process exists|Process to ensure thatLLM operations complywith regulations such asGDPR, HIPAA,or otherrelevant data protectionlaws|Process to ensure that LLM operationscomply with regulations such asGDPR, HIPAA,or other relevant datacollection and protection laws andcopyright laws|
|Does the LLM-based app useanonymization to protect users'identities while maintaining thedata's utility for LLMs?|No anonymization|Basic anonymizationtechniques applied|Advanced automated anonymizationmethods,including data masking andaggregations|
|Does theorganization performregular security reviews and auditsof LLM infrastructure and code?|No regular reviews|Periodic security reviewsand audits|Regular,comprehensive securityreviews and audits,including third-party assessments and vulnerabilityscans|

The LLMOps Maturity Model

41

Let's look at these levels in more detail:

## Level 0: No LLMOps

Machine learning efforts are often isolated and experimental, and they lack any systematic deployment and monitoring framework. The models may be devel‐ oped in silos, often resulting in unreliability and inefficiency. Chevrolet's chatbot blunder is an excellent example; due to a lack of monitoring and guardrails, the app was abused by the community for algebra homework. It also offered Chevro‐ let cars in no-take-backsies deals and promoted Tesla cars instead.

## Level 1: MLOps, no LLMOps

The organization is likely to have a robust pipeline for model training, testing, and deployment, with automated monitoring and retraining workflows. How‐ ever, this setup is designed to build for small models and is not fully optimized for the specific challenges of LLMs.

## Level 2: Full LLMOps

At the highest level of maturity, the organization has adopted LLMOps practices and is fully optimized for LLM applications. Its infrastructure is capable of handling large-scale LLM deployments, fine-tuning, real-time inference, auto-scaling, and resource management. Mature LLMOps teams have failover and rollback mechanisms in place and can act quickly if the updated model underperforms after deployment. The organization can deliver more reliable responses, get a good ROI, and reduce operational risks.

42

Chapter 2: Introduction to LLMOps

## Conclusion

In this chapter, we discussed the team structure for organizations building LLM applications. We discussed various roles and how to build a highly effective team. Finally, we discussed a framework for typing the LLM performance metrics with the business KPIs. In the next chapter, we will talk about how LLMs have changed the data engineering landscape, and we'll show you how to build performant data pipe‐ lines for LLMs.

## References

Azure Machine Learning. "Machine Learning Operations Maturity Model", Learn Azure, accessed May 21, 2025.

Friedman, Itamar. "Software 3.0—The Era of Intelligent Software Development", Medium, May 3, 2022.

Lin, Chin-Yew. "ROUGE: A Package for Automatic Evaluation of Summaries", Text Summarization Branches Out, (Association for Computational Linguistics, 2024).

Kadambi, Sreedher. "Shingo Principles: Bridging Lean and Toyota Production System Success". Skil Global, May 28, 2021.

Mcintyre, Branden. "Chevy Chatbot Misfire: A Case Study in LLM Guardrails and Best Practices", Medium, December 22, 2023.

Papineni, Kishore, et al. "BLEU: A Method for Automatic Evaluation of Machine Translation", ACL '02: Proceedings of the 40th Annual Meeting of the Association for Computational Linguistics, edited by Pierre Isabelle, Eugene Charniak, and Dekang Lin (Association for Computational Linguistics, 2002).

## Further Reading

Shingo, Shigeo. Zero Quality Control: Source Inspection and the Poka-Yoke System, (Routledge, 2021).

Tennant, Geoff. Six Sigma: SPC and TQM in Manufacturing and Services, (Routledge, 2001).

Further Reading

43

CHAPTER 3

# LLM-Based Applications

As of early 2025, only a few companies offer large multimodal models that can understand and generate text, images, and other media, like sound and video. For brevity, we will call these AI models. The most well-known examples are the GPT models created by OpenAI, but a few other popular examples are the Gemini models created by Google, the Claude Sonnet and Haiku models created by Anthropic, and the Llama models created by Meta.

In many cases, these companies partner with other companies to offer these models as a cloud service. For example, OpenAI has a partnership with Microsoft, which provides the infrastructure to host OpenAI's models in cloud services that can be accessed via APIs. Other companies, like Meta, provide a model snapshot, a large binary file containing the weights of a pretrained model, which users can install in their own infrastructure. This infrastructure can be "bare metal," meaning physical machines the companies own, or cloud infrastructure they purchase from other providers.

Model-building companies also offer user-facing applications. In many cases, the name of the model and the name of the user-facing application are the same or very similar, making it easy to confuse the two. For example, the Google Gemini applica‐ tion uses the Google Gemini model, and the Claude application uses the Anthropic Claude Sonnet and Haiku models. OpenAI's names are slightly different: its user-facing application, ChatGPT, allows users to interact with the GPT-4o and GPT-4o-mini models.

45

These applications can have different levels of sophistication. The simplest type of application is a chat-like web interface that allows users to send prompts directly to the model and returns the response. These days, most of the applications provided by large companies are more sophisticated than that. Instead of simply passing prompts directly, they add several layers of their own instructions to the user input, keep track of what the user asked earlier in that conversation (and sometimes in previous sessions), modify the user-submitted prompt to increase the chance of getting a bet‐ ter response, and ensure that their answers are safe and polite.

Given these additional prompts and safeguards, users get different answers when interacting with models through the API and through the default web application. For example, when a user is interacting with ChatGPT on the web through chatgpt.com, they are likely to get different answers than if they were to submit the same prompt directly to the model using an API. The answer from ChatGPT may use data from previous chats and will add some additional safeguards and instructions to the user-provided prompt. For example, when you ask a question using ChatGPT's website, it now usually finishes the response with a question inviting the user to continue the conversation, like "Would you like to explore more?" If you use the model directly from the API, it will not include this conversational phrase.

Companies don't have to develop and train an AI model in order to create an applica‐ tion that uses AI. They can license and integrate existing models such as Gemini, Claude, or GPT-4o into their user-facing applications. Since 2023, a large proportion of repositories in GitHub have been importing code that allows use of the OpenAI APIs, indicating that many developers are using the GPT cloud services to add AI features to their own applications, as shown in Figure 3-1.

This chapter discusses the operational considerations for using AI models in userfacing applications.

46

Chapter 3: LLM-Based Applications

Figure 3-1. Generative AI growth (source: Microsoft | AI for Good Lab)

/371692f17e461b3fe3971201aa030e6da71cd9f5007bf5dae0eb5ea472c85140.jpg

## Using AI Models in Applications

Many application tasks that were formerly assisted by automation and machine learn‐ ing are now using AI models. The difference between implementing automation yourself and using a foundation model is subtle but consequential, especially for LLMOps.

Using AI Models in Applications

47

Before machine learning and foundation models, if you wanted to automate a task, you would need to code it yourself, programming all the possible inputs and corre‐ sponding outputs for the application. In the last decade, a lot of this automation code could be replaced by training a model using machine learning. When a new input was submitted, the ML model would generate an appropriate output, even if that input was not explicitly programmed or previously seen by the model.

Here are some examples of popular consumer-facing applications that incorporate third-party foundation models:

## BeMyEyes

This OpenAI application helps people who are blind or have low vision to navi‐ gate the world better by using their phones. They can point their phone cameras at things and hear rich descriptions. They can use the app to count money, to identify products in the supermarket, and to assist with using automated teller machines. They can even point the app at their computer screens to get technical support.

## Duolingo

This foreign language–learning application uses LLMs to create lessons faster and with more variety. The models are used to generate more versions of dia‐ logues that adhere to difficulty standards, making lessons less repetitive and more enjoyable.

## Khan Academy

This educational website is used by hundreds of millions of people to learn aca‐ demic subjects, mainly those taught in grades K–12. Khan Academy offers Khan‐ migo (a portmanteau of Khan and amigo, Spanish and Portuguese for "friend"), which serves as a study buddy and personal tutor. Students can ask Khanmigo questions about careers and why the lesson they're taking is useful for their lives (a favorite question among teenagers: "Ugh, why do I have to learn this?"). Khan‐ migo can also generate quizzes to assess learning, provide feedback on the stu‐ dent's writing and answers, and generally help a student without providing the answers directly.

## Microsoft Copilot

The Copilot stack accounts for perhaps the widest deployment of AI to date. Available in several popular Microsoft products, including Office, Windows, and Bing, the Copilot products help users accomplish common tasks quicker. For example, you can open Word and ask Copilot to "write a letter to Bank of Amer‐ ica asking to close my checking account." A letter automatically populates with the appropriate language, and you just need to fill in a few blanks. Another fre‐ quently used example is converting Word documents to PowerPoint presenta‐ tions and vice versa.

48

Chapter 3: LLM-Based Applications

## Build Versus Buy

When using an AI model in your application, one of the main decisions is whether to build your own model from scratch, start from a model and improve it through finetuning and/or prompt engineering, or simply use an existing model out of the box. The considerations for this decision are covered in Chapter 1. This chapter assumes that the decision has already been made and you already have one or more models ready to use in your application.

## Infrastructure Applications

While the first wave of LLM applications was mostly focused on user-facing tools for tasks like writing and summarization, the current wave of LLM-based applications is largely focused on infrastructure applications that make LLMs faster, more program‐ mable, and more modular. They redefine what an LLM is and how it can be used. LLM applications are no longer limited to chatbots: they have become a new layer of code in software applications. (This is what we referred to as Software 3.0 in Chap‐ ter 2.) Let's look at some of these uses, one by one.

## Agentic Workows

A single prompt can take you far. But for anything beyond a surface-level task, you need more than one-shot queries. You need memory. You need planning. You need tools. And eventually, you need agents that can act—not just complete a prompt but choose what to do next. This is where the shift from language models to agentic sys‐ tems comes in.

At its core, an agent is just a loop. It observes, decides, and acts—over and over. Those acts might be to read an instruction, check its current state, fetch a resource, call a tool, or break a task into smaller ones. Each of those actions requires reasoning, and each decision affects what happens next. In an agentic system, the model is no longer passive. It's running code, managing steps, and adapting as it goes.

This approach unlocks more complex workflows. Instead of a user stitching together model calls by hand, an agent handles the logic. It can retry failures, store intermedi‐ ate state, track objectives, and even call other agents. This isn't prompt engineering anymore—it's system design.

Not all agents operate the same way. Some follow a fixed plan; others adapt in real time. Some agents think once, act once, and stop. Others operate in loops, revisiting goals and shifting strategy as needed. Understanding these differences helps in designing systems that are robust, interpretable, and efficient. Major types of agents include:

Infrastructure Applications

49

## Single-step agents

The simplest form of an agent is little more than a wrapped prompt. It takes an input, does some local reasoning, returns an output, and exits. There's no mem‐ ory, no iteration, no feedback loop. These are useful when the task is bounded, like generating a SQL query, converting a paragraph to a tweet, or answering a direct question. But single-step agents are brittle. They assume everything is known up front. They can't handle surprises or partial failures. You'll quickly out‐ grow them when tasks involve multiple actions or require state tracking.

## Chain-of-thought agents

Here, the agent reasons step-by-step—often in the same prompt. Instead of jumping straight to the answer, it explains its logic first. This internal decomposi‐ tion improves reasoning and often leads to better performance on multi-hop problems. However, the limitation is clear: it's still all happening within a single model call. There's no memory of what was done before. If the chain is too long or the context window too short, the agent breaks.

## Plan-and-act agents

This is where things get more interesting. These agents first generate a high-level plan, then execute it step-by-step. For example, if you tasked a plan-and-ask agent with writing a blog post, it would start by drafting an outline. Then it would write each section separately, check for coherence, and edit the result. The planning and acting can happen in the same model or across separate agents. This structure introduces what has been done, what's left, and where things went wrong. It also allows for retries and self-correction. If a step fails, the agent can replan or fall back to an alternative.

## Reflective or self-improving agents

These agents don't just act—they reflect on their performance. After completing a task, they might score their own output, compare it with a ground truth, or even consult another model to improve their reasoning. This creates a feedback loop where the agent learns from its past actions—not in the ML training sense but in the runtime sense. Reflection is costly but powerful. It adds robustness, especially in open-ended domains where correctness is hard to define in advance.

## Recursive decomposition agents

In this pattern, an agent tackles a task by recursively breaking it down. It might see a top-level goal, decide it's too big, and generate subtasks. It then becomes a manager—delegating each subtask to a new instance of itself or to other special‐ ized agents. This pattern is used in systems like AutoGPT and BabyAGI. It allows for dynamic depth: tasks get decomposed until they're small enough to solve directly. The challenge is keeping the recursion from spiraling out of control, especially in the absence of tight constraints or time limits.

50

Chapter 3: LLM-Based Applications

## Multi-agent collaborators

Rather than using recursion, some systems distribute responsibility: one agent writes, another edits. One gathers data, another analyzes it. These agents have defined roles, often with isolated tools and memories. Communication happens through shared messages or task queues.

This is effective when tasks are parallelizable or when each agent has domainspecific expertise. It also forces clear interfaces: each agent must expose how to talk to it and what kind of input it expects.

Each of these patterns serves a different purpose. Some are simple, designed for speed. Others are more expressive, built for complexity. As models improve and infrastructure grows, we'll see these workflows combine—agents that reflect and recurse in combination with systems that plan, act, and then hand off to a team. As these systems scale, coordination becomes the challenge. One agent might specialize in math. Another might handle API queries. A third might focus on summarization.

Instead of building a single monolithic agent that does everything, it makes more sense to compose smaller, focused agents that work together. This is where multiagent systems enter. A multi-agent system isn't just a collection of bots. It's an architec‐ ture in which each agent operates semi-independently, often with its own tools, memory, and goals. The agents talk, delegate, and collaborate. For instance, one agent might take a user request and break it into subgoals. Another might execute a subtask and pass the result back. Over time, agents can even evolve internal protocols—figur‐ ing out how best to share information or resolve conflicts.

Designing these workflows is not trivial. The more agents you add, the more coordi‐ nation overhead you introduce. You have to define roles, communication boundaries, and fallback plans. You need logging, observability, and memory management. You also need clarity around failure; for example, what happens when one agent goes silent or another returns an error?

That's why agentic design is not just about the model—it requires control flow. What decisions should happen inside the model versus outside of it? What should be han‐ dled by logic, and what should be learned? These are architectural questions, not just engineering ones.

As of now, we're still early in this transition. The industry is moving from LLMs as isolated prompt responders toward full-blown systems that can think in steps, dele‐ gate across agents, and operate over time. To make this possible, it needs shared protocols like MCP and A2A, which we discuss next. These protocols provide con‐ ventions that let agents talk, reason, and act as a team.

Infrastructure Applications

51

## Model Context Protocol

There is a quiet shift happening in how we build intelligent systems today. In the early days of language models, most applications were monoliths—self-contained, brittle, and tightly coupled to the tools they used. Every integration was handcrafted. If a model needed to talk to a database, spreadsheet, calendar, or code repository, some‐ one had to write a custom connection for each pairing. As the number of models and tools grew, the web of integrations became unmanageable.

What emerged out of that chaos was a new design principle—simple, but transforma‐ tive. Instead of trying to make every tool speak the model's language or forcing every model to understand every tool, AI engineers split the problem, giving each part a role. That principle now lives in the form of the Model Context Protocol (MCP), first introduced by Anthropic in late 2024 (Figure 3-2).

![image](file:///C:/137fc32cca69741d4881364244d0a22db43108b535f4b86e85ad49c5c1019ed9.jpg)

Figure 3-2. Model Context Protocol (source: Phil Schmid)

At its core, MCP is a contract among three moving parts. First, there's the host—your AI application, like a desktop assistant or a chatbot. Then there's the server—any external system or tool that exposes capabilities to the model. Finally, the client is the messenger that connects the two. What makes MCP powerful is not just that it splits the parts cleanly but that it gives them a common language; i.e., a standard way to describe what they can do, what they know, and what they can provide to the model.

With MCP, a model no longer has to guess what's possible. Instead, it can discover tools, query data sources, and select prompts—all in real time, all through a shared protocol. This means a model doesn't just generate responses; it acts, it calls tools, it gathers context, and it learns how to interact with the outside world in a modular, controlled way.

In practice, working with MCP feels less like magic and more like plumbing. You can plug in a GitHub integration, a Slack connector, or a calendar interface, and the model can learn to use it—without needing a new integration each time. Each server exposes tools and resources. The client mediates. The host orchestrates. And the model flows through it all, aware of the tools at its disposal.

52

Chapter 3: LLM-Based Applications

## MCP components

At the time of writing, MCP defines three key components that external systems can expose:

## Tools

These model-controlled functions are callable operations that the language model can invoke during a session. Think of tools as function endpoints—when a model determines that it needs to take an action, such as retrieving a document, querying an API, or triggering a workflow, it does so by calling a tool. Tools are defined with a clear input/output schema and are registered with the host appli‐ cation at runtime.

## Resources

These application-controlled data endpoints are read-only data sources that the model can reference to enrich its context. Unlike tools, resources do not execute logic. Instead, they expose structured data—such as a list of files, user profiles, or metadata—that the model can access via lookups. These are useful when the application wants to give the model direct access to information that doesn't require active computation or external side effects.

## Prompts

These user-controlled templates are pre-engineered prompt structures that can be presented to the model as part of the context or decision-making path. Prompts help guide the model's behavior using predefined instructions, formats, or strategies. They can encapsulate common workflows or suggest best practices for using tools and resources effectively.

This is the new system architecture design for Software 3.0. It's how we move from fragile, one-off agents to systems that scale. With MCP, you can build once and use what you build everywhere. The protocol acts like a universal adapter, abstracting away the messy details of each tool and giving the model a consistent way to act.

## MCP implementation

Now, let's look into how MCP works. MCP is implemented as a client–server proto‐ col. The host application—which could be a desktop assistant, IDE plugin, or custom agent—runs one or more MCP clients. Each client establishes a one-to-one connec‐ tion with an MCP server, which is an external system exposing tools, resources, and prompts.

Infrastructure Applications

53

The protocol begins with a handshake phase, where the client and server exchange version and capability metadata. This ensures compatibility and allows the client to dynamically understand what the server offers.

Once the connection is established, the discovery phase begins. The client queries the server to enumerate all available tools, resources, and prompts. The server responds with structured metadata that the client can then serialize and expose to the model through the host application.

During the interaction phase, when a model identifies a need to call a tool, it emits a structured function call (using JSON or a similar schema). The host routes this request through the client to the server, which executes the tool logic and returns the result. The host application can then inject the output back into the model's context, allowing the LLM to incorporate external data into its next reasoning step.

The same pattern applies for resource lookups—the model can request a resource by ID or query, and the host will retrieve the data from the MCP server via the client. Similarly, when using prompts, the host can offer predefined templates to the model based on the MCP server's response during discovery.

All of this happens asynchronously and incrementally. The model doesn't need to preload every tool or piece of data. It queries what it needs in real time, based on the evolving conversation or task state. This architecture introduces a high degree of modularity. A single host can connect to multiple MCP servers simultaneously. Each server needs to implement the protocol only once, and it becomes compatible with any number of model-based clients or applications that follow MCP.

## Example MCP project

Here is a quick example of how to build a simple server with Python to fetch weather data using MCP. This code connects to an MCP server running a weather data ser‐ vice. It sends a request for weather data about Lisbon, Portugal, including tempera‐ ture in Celsius. It lists available resources and tools on the server. It calls a tool (weather-tool) to fetch the weather data. Optionally, it reads a file resource contain‐ ing a weather report. Finally, it prints out the weather data received from the server:

## Step 1: Set up the server parameters

First, define the parameters required to connect to the MCP server, including the executable, server script, and any optional environment variables:

```
server_params = StdioServerParameters(
command="python", # Executable
args=["weather_server.py"], # Your new weather data server script
env=None, # Optional environment variables
)
```

54

Chapter 3: LLM-Based Applications

Step 2: Define sampling callback Create an optional callback function that handles incoming data from the server. In this case, it processes weather-related messages:

async def handle_sampling_message(message): print(f"Received weather data: {message}")

Step 3: Establish a connection to the server Here we use stdio_client to connect to the MCP server:

async with stdio_client(server_params) as (read, write): async with ClientSession( read, write, sampling_callback=handle_sampling_message ) as session:

This code has stdio_client(server_params) open a connection to the MCP server using the parameters you defined earlier. It returns two objects, read and write, which are the communication channels for reading from and writing to the server. ClientSession is used to create a session that will handle all commu‐ nication with the server. It is passed the read and write channels and the sampling_callback function to process messages from the server.

Finally, async with ensures that the connection is automatically closed once the block of code is done executing.

## Step 4: Initialize the session

This line initializes the session, setting up necessary configurations or authentica‐ tion with the server. It must be called before performing any actions like listing prompts or using tools:

await session.initialize()

## Step 5: List the available prompts

You can request a list of available prompts from the server. In this case, you need to retrieve a specific prompt from the server, passing any required arguments, such as a city name for the weather data:

```
prompt = await session.get_prompt(
"weather-prompt", arguments={"city": "Lisbon"}
)
```

## Step 6: List the available resources and tools

Next, you need to fetch two lists from the server: one of available resources and one of available tools. Resources might include files, API keys, or data that the server can access. Tools are functions or services that the server can call to per‐ form specific tasks, like fetching weather data:

```
resources = await session.list_resources()
tools = await session.list_tools()
```

Infrastructure Applications

55

## Step 7: Call a tool

This will call a specific tool on the server, again passing any necessary arguments (city name, temperature units). The tool will process the request and return the result:

```
weather_data = await session.call_tool(
"weather-tool", arguments={"city": "Lisbon", "unit": "Celsius"}
)
```

Optionally, you can also fetch and read a resource from the server:

```
content, mime_type = await
session.read_resource(
"file://weather_reports/lisbon_report.pdf"
)
preview = content[:100]
print(f"Downloaded content preview:
{preview}...")
```

## Step 8: Display the result

Print or process the result from the tool call (in this case, the weather data):

print(f"Weather data for Lisbon: {weather_data}")

## Step 9: Run the code

Finally, use an event loop (asyncio.run()) to run the asynchronous function and complete the entire process:

```
import asyncio
asyncio.run(fetch_weather_data())
```

## MCP and the future of large language models

What's most important about MCP is that it opens the door to something we couldn't do before: true agentic reasoning across systems. Instead of loading up a model with all the knowledge in the world, we give it the power to seek, to ask, to call upon the right tool at the right time. That's how intelligence works in the real world: not by knowing everything but by knowing where to look and how to act.

As the concept of MCP becomes more established, a new class of frameworks and tools has begun to emerge. These frameworks, while not always explicitly labeled as MCP based, follow similar principles of modularity and structured interaction between language models and external systems. Tools like LangChain, DSPy, and Gorilla exemplify this shift. They enable developers to build more efficient programs by managing execution across context windows, scaling interactions with language models, and integrating various tools in a consistent, predictable manner. The core logic is shared; i.e., modularize the architecture, separate concerns, and treat the lan‐ guage model as a flexible tool rather than a monolithic entity.

56

Chapter 3: LLM-Based Applications

This approach is more than just a trend; it's the beginning of a broader shift in how we interact with language models. As these frameworks mature, the interaction with models will evolve from simple prompt-based queries to more complex program‐ matic workflows. We will build layers of logic and structure around models, much like we would with any backend system. As the capabilities of language models expand, the MCP layer itself will evolve to handle more advanced functionalities, such as composable functions, modular logic, conditional execution, tool invocation, and memory manipulation.

Looking ahead, the context window will continue to grow. Tools like virtualized LLMs (vLLMs) will enable persistence across sessions, allowing a model's state to carry over from one interaction to the next. This will enable more sophisticated workflows, where a user no longer just "prompts" a model. Instead, they will interact with a fully integrated system—an LLM-native environment that includes memory, a task stack, logs, and capabilities. The line between the language model and the broader infrastructure will blur, creating an environment where the model can be treated as a dynamic, stateful component within a larger system. In the future, this protocol may be invisible to users, just as HTTP is invisible when you browse the web. But it will shape the way every AI application is built. It will become the back‐ bone of multi-agent systems, agentic workflows, and the infrastructure that supports open-ended intelligence. It doesn't just make LLMs smarter—it gives them hands, eyes, and a map of the world they operate in.

This evolution of MCP will lead to environments where tasks are not limited to short, isolated interactions but can span multiple steps and contexts, with the model acting as a true agent capable of interacting with a wider range of tools and resources. This shift is already happening, albeit incrementally, and will become a fundamental part of how we build AI-driven applications in the future.

## Agent-to-Agent Protocol

MCP brought structure to how language models interface with tools, memory, and external logic, giving us a formal way to treat models like programmable systems. But it assumes there is a single actor—a single agent querying tools, running logic, and managing state. What happens when there's more than one agent?

As agentic systems grow in complexity, so does the need for coordination. An agent that schedules meetings might need to talk to another that handles email summaries, which in turn might call a tool that fetches flight times. So the next wave of modelbased systems doesn't live in isolation—it lives in a swarm. Imagine multiple agents with specialized roles, distributed across platforms and services, all trying to talk to one another. That's where Agent2Agent protocol (A2A) steps in.

Infrastructure Applications

57

A2A, introduced by Google as an open standard, is like a foundational layer for inter‐ operability. It defines how AI agents identify each other, communicate, negotiate tasks, and share results. It picks up where MCP stops. MCP gives one agent a struc‐ ture; A2A gives a group of agents a shared language.

Without a shared protocol, these connections are brittle, with custom integrations, hard-coded dependencies, and vendor lock-in. Every agent has its own dialect, its own handshake. A2A solves this by offering a standard. It doesn't just manage cen‐ tralized orchestration—it enables decentralized collaboration. One agent doesn't need to know how another works under the hood. It just needs to know what that agent can do and how to call it.

At its core, A2A is a communication protocol for autonomous agents. It defines a set of conventions for secure, structured, and extensible agent interactions. It abstracts away the vendor-specific details and focuses on capability discovery, message exchange, task delegation, and identity verification.

Agent cards form the basis of discovery and negotiation. These are JSON-based documents that advertise who the agents are, what they can do, how to contact them, and what security policies they follow. Two agents can expose their cards, find each other, assess their mutual compatibility, and begin collaborating—all without tight coupling. The core components of A2A include:

## Agent identity

Each agent signs its messages cryptographically, so you know who you're talking to.

## Agent cards

These include structured metadata that defines an agent's capabilities, interfaces, and protocols.

## Capability discovery

Agents query each other to find out what functions or tasks the other supports.

## Task negotiation

Agents can delegate work, propose plans, or asynchronously coordinate workflows.

## Secure messaging

All communication is authenticated, encrypted, and audit friendly.

## Extensibility

A2A is built to evolve. You can extend the schema, define your own agent roles, and create domain-specific logic.

A typical A2A interaction follows a few predictable steps, as shown in Figure 3-3.

58

Chapter 3: LLM-Based Applications

![image](file:///C:/bcdfe1f5462a0d59de10770d1399bb0bdace8fb6d50764388736fa73e7e24bd4.jpg)

Figure 3-3. Typical A2A interactions

Let's look at each step in more detail:

Step 1: Discovery An agent looks up another agent's card, either from a registry or via direct request.

Step 2: Validation The calling agent checks the other agent's identity and credentials via its agent card.

## Step 3: Capability matching

The calling agent examines the other agent's listed functions and decides how to delegate a task.

## Step 4: Task delegation

The calling agent sends a structured request. The called agent may accept it, reject it, or propose an alternative.

## Step 5: Execution

If it accepts the request, the called agent performs the task, optionally invoking its own tools or subagents.

Infrastructure Applications

59

## Step 6: Response

The called agent returns a result to the calling agent, along with any relevant logs, metrics, or follow-up capabilities.

Each of these steps is modular. You can plug them into any system—whether you're building agents on top of LangChain, Haystack, or your own platform. And because it's an open spec, you don't have to rely on Google—or any one vendor—to make it work.

## The Rise of vLLMs and Multimodal LLMs

So far, most of the LLM workflows we've discussed in this book revolve around text. There are tokens in and tokens out; i.e., the model interprets language, transforms it, and spits back structured thoughts. But the world isn't made of words alone. We see. We hear. We act in spaces where text is just one part of the information stream.

Multimodal models are the next step. These models don't just read but also see, listen, describe, and even generate across modes. These systems are built to handle input and output in multiple modalities: text, image, audio, video, and sometimes even tab‐ ular data or code. A model is multimodal if it accepts more than one modality as input or produces outputs in more than one. The most common form of multimodal model today is the vision–language model (VLM). VLMs accept both text and images as input and generate text as output. Some also generate images or annotate images with bounding boxes and captions.

This shift unlocks new kinds of capabilities that were previously impossible in pure language systems. Three things in particular make multimodal LLMs viable now:

## Transformer generalization

Transformers, the architecture behind LLMs, don't care if a token is a word or a pixel. Once data is embedded into the right format, it becomes just another stream to process.

## Training scale

Pretraining now happens on massive corpora that include image–text pairs (like LAION or COCO), enabling vision–language alignment at scale.

## Tooling and open access

Projects like CLIP, Flamingo, BLIP, and LLaVA have created reusable architec‐ tures and checkpoints. You no longer need to be OpenAI or Google to train or fine-tune one.

60

Chapter 3: LLM-Based Applications

Here's how the pipeline typically works:

## 1. Input embeddings

The text is tokenized. Images are passed through a visual encoder (often a ViT).  
Both get embedded into the same vector space.

## 2. Fusion

The model combines visual and textual embeddings, attending over both. This is where reasoning happens, as the model aligns what's seen with what's said.

## 3. Output

The model produces a text output (like a caption, description, or answer) condi‐ tioned on both modalities.

Some models, like CLIP, don't generate text at all. Instead, they match image embed‐ dings with text embeddings. Others, like LLaVA or MiniGPT-4, are chat based; i.e., they can answer visual questions, describe images, or interpret charts and graphs through conversation. Some of the most well-known multimodal models, as of mid-2025, include:

## CLIP

CLIP is a model from OpenAI that learns joint vision–text embeddings. It's not generative—it's matching based. You can find the image that matches a sentence or the sentence that describes an image.

## BLIP and BLIP-2

These are bootstrapped vision–language models, pretrained to describe and rea‐ son about images in natural language. BLIP-2 uses a frozen image encoder with a lightweight query transformer.

## MiniGPT-4

MiniGPT-4 combines a visual encoder with a frozen LLM, aligning their repre‐ sentations with minimal training. It basically acts like a visual chatbot.

## LLaVA

LLaVA, which is built on LLaMA and CLIP-style vision encoders, allows for interactive visual dialogue and visual question answering (VQA).

## Flamingo

Flamingo, from DeepMind, is a powerful closed-source model that has set new benchmarks for few-shot multimodal reasoning.

## BentoML and LLM Foundry

BentoML and LLM Foundry, while not models themselves, provide deployment, serving, and training infrastructure to fine-tune and run VLMs on your own stack.

The Rise of vLLMs and Multimodal LLMs

61

Multimodal agents unlock a huge new surface area for ways to use AI. They can:

• Answer questions about an image, video frame, or document screenshot

• Parse charts, tables, or handwritten text

• Summarize slides

• Transcribe whiteboards

• Describe UI layouts

• Navigate the physical world in robotics or assistive agents

• Build more "human-like" interfaces that feel less robotic and more perceptual

It's about reasoning across modalities, treating language and vision as two views of the same world. Just like in language, the shift is from pattern recognition to contex‐ tual reasoning.

The trajectory is clear: modality boundaries are blurring. Future systems will handle vision, language, audio, code, and interaction as part of the same cognitive loop. Some already do. The open frontier is about building agentic systems that see, decide, and act—not in separate blocks but as integrated flows.

This changes the architecture of everything. Prompts become interfaces, not just instructions. Inputs are multimodal, such as a voice command plus a camera feed. Outputs are also multimodal, often including a generated summary and a visual markup.

Multimodal LLMs thus aren't just a feature upgrade—they introduce a structural change in what language models are. They represent a shift from abstract dialogue machines to embodied agents that understand and operate in the real world.

## The LLMOps Question

The main question that LLMOps teams need to answer is "Does the application per‐ form well at a reasonable cost?" Once they can answer yes to this question, they can start working on optimizations, trying to extract maximum performance at the mini‐ mum possible cost. For LLM applications, there are several dimensions of perfor‐ mance, but let's talk about cost first.

For companies that choose to buy LLM services from a cloud provider, costs can be measured directly in financial terms (you can use LLM Price Check for comparisons). While it's not trivial to define performance and measure it, let's assume for a moment that the app is already deployed in production and that the performance is at the desired level. In that case, if the main goal of the company is to maximize profits, the LLMOps team should choose the cloud LLM that provides that performance at the lowest cost.

62

Chapter 3: LLM-Based Applications

For companies that choose to build LLMs or run LLM applications in their own hard‐ ware, there's an additional consideration: the opportunity cost of building versus buy‐ ing. (Opportunity cost here means the money, time, and market lead lost if the organization chooses to build and manage the hardware itself rather than outsourc‐ ing it using model APIs.) The demand for graphics processing units (GPUs) capable of running LLMs is very high, helping to propel the stock prices of GPU manufactur‐ ers like Nvidia to record levels. In addition to determining the cost of running an application, companies that acquire GPUs must answer one surprising question: would they make more money simply renting those GPUs? Spheron has an excellent in-depth blog post on the economics and drawbacks of buying versus renting GPUs. In some cases, renting your GPUs is more profitable than running your own opera‐ tions in-house.

## Monitoring Application Performance

The field of MLOps existed for several years before LLMs, and for many application classes, the performance metrics for MLOps and LLMOps are the same or very simi‐ lar. This is because most application performance metrics are domain dependent. For example, for an application that uses LLMs to support the sales process, a key metric might be the sales conversion rate, which answers the question "Are we selling more now that we've started using LLMs?" For a human resources application that uses LLMs to match candidate resumes to job descriptions, a key metric may be the interview-screening success rate, which answers the question "Are we getting better candidates in our pipeline now that we've started using LLMs?"

Calculating these metrics doesn't depend on the underlying technology. Whether the application is using ML, an LLM, or pen and paper to determine which customers or candidates to call, these evaluation metrics are calculated the same way. LLMs can still provide additional challenges, mainly because they are less deterministic and more susceptible to a class of changes called drift than ML models are. We will discuss drift in detail in Chapter 7. For now, it helps to think of it this way: applications that use LLMs frequently behave more like processes executed by humans than like computerbased applications, especially in terms of output variability. Your application metrics should accommodate this variability.

## Measuring a Consumer LLM Application's Performance

To better illustrate the differences, let's use an example that ML has solved: classifying email as spam and not spam. Let's assume that the ML version of this application uses a popular model like XGBoost and that the LLM version of this application uses a popular model like GPT-4o. For now, let's assume we're using a simple prompt in our LLM-based application. For example:

The LLMOps Question

63

Is the following email spam? Respond with spam if the email is spam or ham if the email is not spam.

[Email contents]

Spam detection is a classic binary classification problem for which the metrics of accuracy, precision, and recall are typically used:

## Accuracy

Accuracy measures the proportion of correctly classified instances out of the total instances. In this case, it indicates the overall percentage of emails that the model correctly labeled, either as spam (true positives) or not spam (true nega‐ tives). The formula for accuracy is:

$$ \begin{array} { r } { A c c u r a c y = \frac { T r u e P o s i t i \nu e s + T r u e N e g a t i \nu e s } { T o t a l I n s t a n c e s } } \end{array} $$

While accuracy is a helpful general measure, it can be less informative when the data is imbalanced—for example, if most emails are not spam, which is a typical case.

## Precision

Precision measures the proportion of true positive predictions (correct spam classifications) out of all the instances that the model classified as positive (spam). Precision answers the question "Of all emails classified as spam, how many actually were spam?" The formula for precision is:

$$ \begin{array} { r } { P r e c i s i o n = \frac { T r u e P o s i t i \nu e s } { T r u e P o s i t i \nu e s + F a l s e P o s i t i \nu e s } } \end{array} $$

High precision indicates that when the model classifies an email as spam, it's likely correct. However, high precision may come at the expense of missing some actual spam emails, which would lower recall.

## Recall

Recall (also called sensitivity or true positive rate) measures the proportion of true positive predictions out of all actual positive instances (all actual spam emails). Recall answers the question "Of all actual spam emails, how many did the model correctly identify as spam?" The formula for recall is:

$$ \begin{array} { r } { R e c a l l = \frac { T r u e P o s i t i \nu e s } { T r u e P o s i t i \nu e s + F a l s e N e g a t i \nu e s } } \end{array} $$

High recall means the model successfully identifies most spam emails, but this can sometimes lead to more false positives, which can reduce precision.

64

Chapter 3: LLM-Based Applications

Accuracy provides an overall rate of correct classifications, precision shows accuracy within the positive predictions, and recall reflects the model's ability to capture actual positives. Together, these metrics offer a well-rounded evaluation of the model's effec‐ tiveness in distinguishing between spam and non-spam emails.

The choice of whether to prioritize precision or recall depends on the application. For instance, in spam filtering, users typically prefer higher recall—that is, catching as much spam as possible—even at the risk of flagging some non-spam emails as spam. To mitigate the problem of false positives, users have been trained over the years to look into their spam folders from time to time. In other classification tasks, such as medical diagnoses or fraud detection, your application may prefer to prioritize preci‐ sion to minimize false positives and the associated expenses and stress.

In this example, regardless of whether you are using LLMs or classic ML for your application, as long as the application produces an output of "spam" or "ham," you can calculate accuracy, precision, and recall and compare the models using the met‐ rics above. To do so, you'd use a test dataset for which you have prelabeled correct answers: the ground truth. You can use this test dataset with your model to calculate the metrics above.

In a machine learning setting, the model output has a meaning: the "spamminess" level of the email. Higher numbers mean that the email is more likely to be spam. Engineers can increase this application's precision, at the expense of recall, by setting a higher threshold for classifying an email as spam. This reduces the chance of mis‐ classifying non-spam emails as spam, which in turn results in fewer false positives and raises precision (fewer non-spam emails are flagged as spam). However, it may also mean that more spam emails go undetected, which lowers recall.

The engineers can also go in the opposite direction, setting a lower threshold. Now the model would classify more emails as spam, catching more true spam emails and increasing recall, but increasing the likelihood of false positives (non-spam emails incorrectly classified as spam) and reducing precision.

By using this process in several values of the model output, you can plot a precision– recall curve, which is a shortcut to calculate the performance of the model under sev‐ eral different settings. The precision–recall curve shows precision on the y-axis and recall on the x-axis at different threshold levels. This curve allows an MLOps team to visualize how the precision and recall change as the threshold varies, showing the trade-offs between them. Since "spamminess" is the default output of ML models, you can create this chart easily in an ML setting by simply using your test dataset with different classification thresholds, calculating precision and recall, and plotting the results.

The LLMOps Question

65

In general, a high-quality model will have a curve that reaches higher precision and recall levels, and a low-quality model will have a curve that stays near the origin (low precision and recall). You can measure the area under the curve for precision and recall (AUC-PR) in the graphs in Figure 3-4. Higher AUC-PR values indicate a better model, as they suggest that the model maintains both high precision and high recall over a range of threshold values. That is, a model with a larger area is better overall.

/21c27878c97ea2ccc46045f96b75139809c7b42fc80c236def3811b26f30371e.jpg

Figure 3-4. An example case where AUR-PC is a better predictor for model performance, even though the ROC curve may tell a different story (source: Fabio Sigrist)

/3bdbdc6de2900faec4ae0a4b953c691a61e2105d9aea32e397eb17b114495a55.jpg

When using an LLM as the engine of your application, you can't easily calculate the area under the curve. The first practical problem is that the output of the model does not contain the probability that a given email is spam. One way to solve this problem is to modify the prompt and ask for the probability instead of the output, as proposed in the 2024 paper "Calibrating Verbalized Probabilities for Large Language Models":

What is the probability that the email below is spam? Give the answer as a real number between 0 and 1. Your answer should be just the number with your best guess of the probability.

## [Email contents]

Using such a prompt would let you create the graph, but here is the problem with LLMs not being deterministic: even at a temperature of zero (as little randomness as possible), an LLM may produce wildly different probability numbers for the same input email. Temperature, along with several other parameters, such as fre quency_penalty and presence_penalty, allows us to define the randomness (or creativity) of the model output. A standard OpenAI request with our parameters could look something like the following:

66

Chapter 3: LLM-Based Applications

```
{
"model": "gpt-4",
"prompt": "Write a poem about machines.",
"temperature": 0.7,
"top_p": 0.9,
"frequency_penalty": 0.5,
"presence_penalty": 0.6,
"max_tokens": 60,
"stop": ["\n\n"]
}
```

Now, let's take an example where I use the prompt to classify an email informing me of the delivery of components for installing a solar panel.

Abi,

I just wanted to reach out and update you. We will have the components delivered by Friday. As soon as I confirm I will schedule with you all. The government permits should come in approximately two more weeks.

I sent requests twice in a row with GPT-4o at temperature 0, and I obtained two dif‐ ferent probabilities, 0.05 and 0.1. A third submission resulted in 0.05. Although set‐ ting the temperature to 0 is supposed to make the model deterministic, clearly this flip-flop in outputs means that you can never assume perfect consistency in LLMs. Therefore, you can't reliably use this probability-plotting method to generate a curve and then choose the model with the best area. The typical compute metrics, like receiver operating characteristic (ROC) or recall curve, area under the curve (AUC), and area under the precision recall curve (AUC-PR), assume stable scoring; that is, the same input gives the same score every time. However, for LLMs, these curves become noisy, and the standard methods of evaluation become unreliable. The evaluation sys‐ tem can falsely assert that one "version" of the model is better than the other, simply because of internal randomness.

## Choosing the Best Model for Your Application

One of the most common tasks in both MLOps and LLMOps is to decide whether a new version of a model is better than an existing version. This is sometimes called the champion/challenger test or A/A test in which the model that is currently in produc‐ tion is called the "champion," and the new model is called the "challenger." If the chal‐ lenger proves better than the champion, it replaces the champion and takes its place in production. The proof is usually done by evaluating both models by a metric or a collection of metrics.

To handle the inherent variability of LLM outputs, you'll need to calculate distribu‐ tions over multiple samples rather than rely on single-point metrics like AUC. In practice, this means running each test dataset several times to obtain a range of out‐ comes, allowing you to calculate statistical distributions such as the mean, standard deviation, and confidence intervals for the performance metric you're evaluating.

The LLMOps Question

67

By gathering these distributions, you can gain insights into the stability and reliability of the model's responses. These metrics help determine whether the challenger genu‐ inely outperforms the champion or if differences are simply due to inherent model variability.

For example, rather than using a single precision or recall figure, you would calculate the average precision and recall for both models over a large number of tests, record‐ ing the variance in these scores. The resulting distributions allow you to perform sig‐ nificance testing, or a t-test, which can help you determine if the difference between the two models is statistically significant. This approach accounts for the model's vari‐ ability, offering a clearer picture of whether the challenger consistently performs bet‐ ter than the champion across a range of scenarios and inputs. You can use the A/A test to see if your process works. Running your decision framework on the same model twice might produce results that have different point estimates, but the differ‐ ence between them should not be statistically significant.

Ultimately, calculating distributions (see the code in Example 3-1) rather than rely‐ ing on single metrics provides a more robust framework for comparing LLM-based applications, helping mitigate the challenges posed by the nondeterministic nature of LLMs.

Example 3-1. Calculating two models' distributions of precision and recall over a large number of tests

```
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
# Simulate two distributions of model scores with a random seed
np.random.seed(42)
champion_scores = np.random.normal(loc=0.78, scale=0.02, size=100)
challenger_scores = np.random.normal(loc=0.80, scale=0.02, size=100)
# Plot the distributions
plot.figure(figsize=(10,6))
sns.kdeplot(champion_scores, label="Champion Model", color = "blue")
sns.kdeplot(challenger_scores, label="Challenger Model", color = "red")
plt.title("Distributions of Model Performance Scores")
plt.xlabel("Score")
plt.ylabel("Density")
plt.legend()
plt.grid(True)
plt.show()
```

By evaluating performance over large test sets and using statistical tools to interpret these results, you can better determine if the challenger model is a worthwhile replacement for the champion.

68

Chapter 3: LLM-Based Applications

## Other Application Metrics

Although we used precision and recall in the preceding example for simplicity, many other metrics are used in practice. Applications like recommendation systems and ranked-choice applications (such as search algorithms) often use mean average preci‐ sion (MAP) to evaluate ranking quality. MAP calculates the average precision for each query or user and emphasizes placing relevant items higher in the results list. MAP gives higher scores to models that rank relevant items at the top, making it particu‐ larly useful for applications where the order of results is critical. This is essential in contexts like ecommerce search, where users are more likely to click on the first few results, and high MAP scores indicate that relevant items are being effectively prioritized.

Another widely used metric for ranked applications is normalized discounted cumula‐ tive gain (NDCG), which evaluates the relevance of results while accounting for their positions. NDCG applies a discount factor that reduces the importance of relevant items that appear lower in the ranking, making it ideal for systems that need to sur‐ face relevant content at the very top. For example, in a news recommendation app, users are likely to click only on the first few articles, so high NDCG scores indicate that the most relevant articles are being given prime spots.

Other key metrics in ranking and recommendation applications are hit rate (also called top-k accuracy) and coverage. Hit rate measures how often at least one relevant item appears in the top k results, indicating the model's consistency in recommending relevant items within the top ranks. For instance, in a streaming service, a high hit rate ensures that users frequently see relevant shows or movies in the top suggestions. Coverage, on the other hand, measures the proportion of items in the catalog that are recommended. This helps determine whether the model provides a wide range of options and helps it avoid repeatedly recommending popular items. High coverage in recommendation systems is desirable because it exposes users to a broader variety of content.

In many LLM-based applications, the ground truth is very subjective. For example, although you can often test whether code generated by an LLM works for a given test set, this is usually not enough to judge code quality—after all, there's a lot of code that works but is inefficient or hard to understand. In these cases, teams tend to use customer-focused metrics like user engagement metrics, including click-through rate (CTR) and conversion rate. CTR measures the percentage of recommended items that users click, while conversion rate tracks recommendations that lead to actions like purchases or sign-ups.

In the code generation example, one way to figure out whether users like the content is whether they click "accept" for the code that is offered. Another way is to check how much they modify the code once it is incorporated in their own code. In an application that sends emails, you can see whether the user who generated the email sent it as provided and monitor the read and response rate of the emails.

The LLMOps Question

69

## What Can You Control in an LLM-Based Application?

When implementing an application with an LLM as the core component, several parameters allow you to shape the model's responses while balancing creativity, coherence, and efficiency. The most well-known setting is temperature, a setting that controls the randomness of the model's output by adjusting how deterministic or variable the response should be. This is a number between 0 and 1. Lower numbers, such as 0.2, make the model focus on the most likely answer, which is useful for fac‐ tual, consistent responses. Conversely, a higher temperature setting, like 0.8, introdu‐ ces more randomness, allowing the model to generate diverse and creative content, which can be advantageous in applications like storytelling or brainstorming.

Two other parameters, top-k and top-p, control the diversity of responses by setting probabilistic limits. Top-k sampling restricts the model to only the top k most proba‐ ble tokens at each step, thus guiding it toward a focused range of words that are statis‐ tically most likely, with lower values ensuring more coherent responses. Top-p sampling, on the other hand, is a cumulative probability threshold, where the model selects from the smallest set of tokens with a combined probability above a given value (e.g., 0.9). This allows it to consider more word options for creative responses, while still ignoring highly unlikely terms. You can use the top-k and top-p parameters alongside temperature to strike a balance between response diversity and coherence, adjusting them to the specific requirements of your application.

Another parameter that influences variety is frequency penalty, which applies a pen‐ alty based on how many times a token (word or phrase) has already appeared in the generated text. This means that each additional occurrence of a previously used word is penalized progressively, making it less likely that the model will repeat specific words frequently. This parameter is particularly useful in creative applications, where avoiding repetition can make the output more pleasant, ensuring that common words or phrases are not repeated too often.

In contrast, another parameter called presence penalty applies a more general penalty to any token that has already appeared at least once, regardless of how frequently it has been used. This means that the model is discouraged from reusing any word or phrase that it has already used, even if it has only appeared once. Presence penalty is less about reducing high-frequency words and more about encouraging the model to introduce entirely new vocabulary throughout the response. This can be beneficial in applications like content generation, where avoiding even mild repetition helps keep the language fresh and varied.

70

Chapter 3: LLM-Based Applications

To manage response length and prevent excessive generation, most models allow you to set a token limit with a parameter like max tokens, determining the maximum number of tokens the model will generate for each response. This is crucial for both controlling costs and tailoring the response length to suit different scenarios; concise answers might require a low token limit, while longer, detailed outputs may need a higher limit. In our spam detection example, the max tokens can be set to a low number. In some models, the max tokens parameter represents both the inputs and the output tokens. The final parameter that you can easily control is the prompt, and this is where a lot of the real-world optimizations happen—through prompt engineering.

## Prompt Engineering Is "Hard"

In our spam detector example, we started with a very simple prompt:

Is the following email spam? Respond with spam if the email is spam or ham if the email is not spam.

[Email contents]

Note that we're back to the case in which the prompt is expected to produce answers that are only spam or ham and will not provide a "spamminess" value. If you use the preceding prompt, you may be surprised to find that there's no guarantee that the model will actually follow the instructions as you expect and output only spam or ham. Some other potential outputs I've obtained from GPT-4o are as follows:

Yes, this email is spam.

Not spam.

I'm not sure.

I'm sorry, but as an AI language model, I must follow ethical guidelines, and I cannot engage in harmful, malicious, or offensive behavior.

Although the last answer may be surprising, it is a very common message from LLMs and may be triggered unexpectedly, often if the spam email has content that is deemed grossly offensive.

This raises another consideration when using LLMs instead of machine learning in applications. When integrating an LLM into an application, you have to decide what to do when the answer doesn't conform to the expected output. A typical solution is to create a new class, such as "unknown." But even then, you could simply coerce all outputs into spam or not spam, for example by classifying all outputs that are not N into spam. Creating the "unknown" category prevents the out-of-specification errors from being hidden from you. In this case, you'll want to add a metric for out-ofspecification error percentage and set a low target.

What Can You Control in an LLM-Based Application?

71

Making adjustments to the prompt is called prompt engineering. One of the simplest things you can do to improve the prompt is to add "Use only spam or ham as the answers, nothing else." This should lower the proportion of answers that fall under "unknown."

Is the following email spam? Respond with spam if the email is spam or ham if the email is not spam. Use only spam or ham as the answers, nothing else.

```
[Email contents]
```

Let's say someone in management reads in an article that models tend to perform bet‐ ter if you ask them to think carefully. They ask you to test whether that change makes your spam detection application better. How can you test whether the new prompt shown next performs better or worse than the existing prompt?

After considering it very carefully, do you think it's likely that the email below is spam? Respond with spam if the email is spam or ham if the email is not spam. Use only spam or ham as the answers, nothing else.

```
[Email contents]
```

We do know one thing: using a more detailed prompt will increase costs, because models charge by the length of inputs and outputs combined.

## Did Our Prompt Engineering Produce Better Results?

To figure out whether the additional cost comes with additional performance, you'll have to go through a decision process. Example 3-2 shows how to do this using Python. In the example, we use the enron_spam_data.csv file, a public labeled dataset of approximately 30,000 emails, exactly half of which are spam.

The code tests just a few emails, running 10 experiments with 30 spam and 30 ham emails each. In a real setting, you would want to use your own, much larger labeled dataset (because of drift, as we will explain in Chapter 7) and do more experiments.

## Example 3-2. Prompt engineering test

```
import pandas as pd
import numpy as np
import random
from statistics import mean, stdev
import os
from openai import OpenAI
from dotenv import load_dotenv
load_dotenv()
client = OpenAI(
api_key=os.environ.get("OPENAI_API_KEY")
)
```

72

Chapter 3: LLM-Based Applications

```
# Define the prompts to test
PROMPT_A = "Is the following email spam? Respond with spam if the email is spam or
ham if the email is not spam. Use only spam or ham as the answers, nothing else.
\n\nSubject: {subject}\n\nMessage: {message}"
PROMPT_B = "After considering it very carefully, do you think it's likely that the
email below is spam? Respond with spam if the email is spam or ham if the email is
not spam. Use only spam or ham as the answers, nothing else.
\n\nSubject: {subject}\n\nMessage: {message}"
# Load the dataset and sample
df = pd.read_csv("enron_spam_data.csv")
spam_df = df[df['Spam/Ham'] == 'spam'].sample(n=30)
ham_df = df[df['Spam/Ham'] == 'ham'].sample(n=30)
sampled_df = pd.concat([spam_df, ham_df])
# Evaluation function
def evaluate_prompt(prompt_template):
true_positive = 0
false_positive = 0
true_negative = 0
false_negative = 0
for _, row in sampled_df.iterrows():
subject = row['Subject']
message = row['Message']
actual_label = row['Spam/Ham']
# Generate prompt with email data
prompt = prompt_template.format(subject=subject, message=message)
# Call the OpenAI API with the given prompt
try:
response = client.chat.completions.create(
messages=[
{
"role": "user",
"content": prompt,
}
],
model="gpt-3.5-turbo-0125",
)
predicted_label = response.choices[0].message.content.strip().lower()
except Exception as e:
print(f"Error calling OpenAI API: {e}")
continue
# Convert the actual and predicted labels to lowercase for comparison
if predicted_label == 'spam' and actual_label == 'spam':
true_positive += 1
elif predicted_label == 'spam' and actual_label == 'ham':
```

What Can You Control in an LLM-Based Application?

73

```
false_positive += 1
elif predicted_label == 'ham' and actual_label == 'ham':
true_negative += 1
elif predicted_label == 'ham' and actual_label == 'spam':
false_negative += 1
# Calculate precision and recall
precision = (
true_positive / (true_positive +
false_positive)
if (true_positive + false_positive) > 0
else 0
)
recall = (
true_positive / (true_positive +
false_negative)
if (true_positive + false_negative) > 0
else 0
)
return precision, recall
# Run experiments
def run_experiments(prompt_template, n_experiments=10):
precisions = []
recalls = []
for n in range(n_experiments):
print(f"Running experiment {n+1} of {n_experiments}")
precision, recall = evaluate_prompt(prompt_template)
print(f"Precision: {precision:.4f}, recall: {recall:.4f}")
precisions.append(precision)
recalls.append(recall)
# Calculate mean and standard deviation for precision and recall
precision_mean = mean(precisions)
precision_stdev = stdev(precisions)
recall_mean = mean(recalls)
recall_stdev = stdev(recalls)
return precision_mean, precision_stdev, recall_mean, recall_stdev
# Run experiments for Prompt A
(
precision_mean_a,
precision_stdev_a,
recall_mean_a,
recall_stdev_a,
) = run_experiments(PROMPT_A)
print(
```

74

Chapter 3: LLM-Based Applications

```
f"Prompt A - Precision: {precision_mean_a:.4f} ± {precision_stdev_a:.4f}, "
f"Recall: {recall_mean_a:.4f} ± {recall_stdev_a:.4f}"
)
# Run experiments for Prompt B
(
precision_mean_b,
precision_stdev_b,
recall_mean_b,
recall_stdev_b,
) = run_experiments(PROMPT_B)
print(
f"Prompt B - Precision: {precision_mean_b:.4f} ± {precision_stdev_b:.4f}, "
f"Recall: {recall_mean_b:.4f} ± {recall_stdev_b:.4f}"
)
```

The results are below:

Prompt A - Precision: 0.8370 ± 0.0365, Recall: 1.0000 ± 0.0000 Prompt B - Precision: 0.7763 ± 0.0311, Recall: 1.0000 ± 0.0000

You can see that the LLM is very good at finding spam in this dataset, with a recall of 100% with both prompts, but the precision is around 84% for the original prompt and 78% for the longer prompt. Is the new prompt better than the existing prompt? We can use a t-test to make that determination. Since the recall is the same for both models, we only need to do the t-test for the precision metric. First, we calculate the t-statistic:

$$ t = { \frac { { \bar { x } } _ { A } - { \bar { x } } _ { B } } { \sqrt { { \frac { s _ { A } ^ { 2 } } { n _ { A } } } + { \frac { s _ { B } ^ { 2 } } { n _ { B } } } } } } $$

In this case, the t-statistic is 6.93. We can convert the t-statistic to a p-value, which in this case is approximately 2.13 × 10–9, far smaller than a typical significance threshold of 0.05.

Since the p-value is extremely small, we can confidently conclude that Prompt A per‐ forms significantly better than Prompt B in terms of precision. This result indicates that the observed difference in mean precision is highly unlikely to be due to random variation. Since Prompt B is also more expensive, we would not update the model to use Prompt B.

What Can You Control in an LLM-Based Application?

75

## LLM-Based Infrastructure Systems Are "Harder"

Once you get past calling an LLM with just a prompt and start orchestrating it into a live system—with memory, tools, feedback, and goals—then you are no longer deal‐ ing with the nondeterministic nature of an LLM. You're dealing with a complex oper‐ ating system with its own language, state, dependencies, and failure modes, each awaiting a failure anytime. Here, both the agentic systems as well as infrastructurelevel LLM applications have their own operational or LLMOps problems.

While the agentic systems promise flexibility, reasoning, and automated decisionmaking, they also introduce complex control flows that can be very hard to debug and even harder to trust. As we saw in the example prompt in the previous section, LLM outputs can vary from one to another. This can make debugging very difficult. If your agent fails at step 6 in a 10-step task, rerunning it might make it fail at step 3 or succeed entirely. Thus, there's no clear "stack trace." Although companies like W&B have offerings like Weave (its tracing tool), perfect reproducibility in agentic workflows can be incredibly hard, if not impossible.

Another issue is that agents need context. They remember facts and refer to earlier steps to plan ahead. But storing and retrieving this memory (whether vectorized or tokenized) becomes a bottleneck in terms of both latency and accuracy. Most mem‐ ory systems are brittle, leaky, and misaligned with the model's representation space. Additionally, very few agents, if any to date, are good at "planning." This has been documented on several Twitter/X spaces where agents often skip steps, repeat tasks, or pursue irrelevant paths. This becomes ever harder when calling tools, because when the tools fail due to API errors or empty results, the agent must recover without getting stuck in a loop or hallucinating. Again, very few, if any, agents handle these edge cases gracefully without being preprogrammed using if-else conditions. More‐ over, there's no equivalent of "unit tests" or "assertions" that works well for agentic workflows yet.

Agentic workflows break when the logic is messy—if, say, the plans don't decompose or memory is poorly structured. However, infrastructure-level LLM applications introduce even more failure points and complexity. If the protocols don't sync with each other, or the data flows start leaking, or the model boundaries are unclear. . .there are far too many failure points to count. While most people have been jumping on the bandwagon to adopt MCPs or A2A, very few are equipped to handle the LLMOps issues these tools introduce.

First, MCP assumes that the memory and tools are abstracted and callable. But that couldn't be further from the truth. Memory updates go out of sync pretty often. Dif‐ ferent agents have different scores, and the tools might update shared state without coordination. You need memory versioning, namespacing, and syncing—none of which actually come "out of the box."

76

Chapter 3: LLM-Based Applications

Then, say, if a model call takes time, wrapping the model call in an MCP session adds orchestration overhead. That includes setup, prompt retrieval, and tool registration issues, all of which can compound. This is where you need to consider the opportu‐ nity cost. Similarly, A2A will add network latency, serialization, and agent discovery issues, and again, for complex tasks, all of these sources of overhead compound very quickly. When a prompt fails in LangChain, you see a clear trace. When an A2A agent fails, it might return an invalid response, break the schema, or even time out. It's never clear where it failed. Was it at the agent stage or transport or the memory layer or the tooling? You need to stack up layers and layers of observability tools and structured logging across agents and sessions.

If your workflow includes five agents, each calling three tools, and every interaction is mediated through A2A or MCP layers, then the user ends up waiting for quite a few seconds or even minutes. This ruins the user experience. Also, most of the security issues haven't even yet been documented as of this writing. Agents might hijack each other's memories, triggering unintended tool actions—the attack surface becomes incredibly wide, especially when you let LLMs act autonomously on the user data.

Agentic intelligence feels incredibly powerful in demos but breaks in production. Indeed, it is very fragile without solid infrastructure. Every day, I personally see tons of clever orchestrations around dumb prompt chains tied up in a brittle, underused LLMOps infrastructure. But building this infrastructure means acknowledging the costs: performance overhead, strict interface contracts, and state complexity, as well as a need for more LLMOps engineers to create the best practices, tooling, and frame‐ works to run these systems reliably, safely, and robustly.

## Conclusion

In this chapter, we've covered the key considerations for integrating LLMs into appli‐ cations, from measuring performance to improving models through parameter adjustment, prompt engineering, and agentic and infrastructure applications. Using LLMs successfully in enterprise applications requires defining clear performance metrics, monitoring them, and continuously improving the models.

## References

Alayrac, Jean-Baptiste et al. "Tackling Multiple Tasks with a Single Visual Language Model", Google DeepMind, April 28, 2022.

Anthropic. "Introducing the Model Context Protocol", November 25, 2024.

Bevans, Rebecca. "An Introduction to t Tests: Definitions, Formula, and Examples", Scribbr, June 22, 2023.

References

77

Fiore, Steven. "Inside Microsoft's Copilot Stack: Building Smarter AI Assistants", Lantern, August 2, 2024.

Henry, Parker. "How Duolingo Uses AI to Create Lessons Faster", Duolingo Blog, June 22, 2023.

Li, Junnan, et al. "BLIP: Bootstrapping Language-Image Pre-training for Unified Vision-Language Understanding and Generation", arXiv, February 15, 2022.

Microsoft | AI for Good Lab. "When AI Became a General-Purpose Technology" [fig‐ ure]. LinkedIn post by Brad Smith, Microsoft, September 2024.

Microsoft Research. n.d. "Building Next-Gen Multimodal Foundation Models for General-Purpose Assistants", accessed May 21, 2025.

OpenAI. n.d. "Be My Eyes", accessed May 21, 2025.

OpenAI. "CLIP: Connecting Text and Images", OpenAI, January 5, 2021.

OpenL. n.d. "LLM Price Check", accessed May 21, 2025.

Schmid, Phil. "Model Context Protocol (MCP) an Overview", personal blog, April 3, 2025.

Sigrist, Fabio. "Demystifying ROC and Precision-Recall Curves", Medium, January 25, 2022.

South, Tobin et al. "Authenticated Delegation and Authorized AI Agents", arXiv, Jan‐ uary 16, 2025.

Spheron Network. "The Economics of Renting Cloud GPUs: A Comprehensive Breakdown", March 13, 2025.

Wang, Cheng, et al. "Calibrating Verbalized Probabilities for Large Language Mod‐ els", arXiv, October 9, 2024.

78

Chapter 3: LLM-Based Applications