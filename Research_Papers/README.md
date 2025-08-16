- Some other important papers, that are used to build OpenAI GPT OSS model.

(1) Longformer: Introduces sliding window attention, a form of sparse attention that is utilized in alternating layers of both gpt-oss models.

(2) StreamingLLM: Describes the concept of attention sinks in large language models (LLMs)—these are tokens within a sequence that the model assigns high attention or weight to, simply because the softmax operation prevents the model from assigning attention to no tokens at all.

(3) Off-by-one attention: Proposes a solution to attention sinks by allowing the attention mechanism to assign no attention to any token. This is achieved by adding a bias term of 1 to the denominator of the softmax operation within attention. In gpt-oss models, a similar approach is used, but the bias term is learned rather than fixed at 1.

(4) Switch Transformer: Presents several ideas foundational to modern mixture-of-experts (MoE) based LLMs. It’s important to note that many other papers, in addition to Switch Transformer, have contributed to this field.

(5) RMSNorm: A streamlined variant of layer normalization that is both more efficient and has fewer trainable parameters. Both gpt-oss models employ RMSNorm.

(6) RoPE: Stands for Rotary Positional Encoding, a hybrid absolute/relative positional encoding method used by gpt-oss models. RoPE encodes absolute position using a rotation matrix and incorporates relative position information directly into the self-attention mechanism.

(7) YaRN: A method for extending the context window in LLMs, which is adopted by gpt-oss models. YaRN works by adjusting the frequency basis used within RoPE and further training the LLM to handle longer contexts.

(8) Flash Attention: Utilized by gpt-oss models, flash attention leverages system-level optimizations to significantly improve the computational and memory efficiency of the attention operation.

(9) DeepSeek-R1: While the specific reasoning or reinforcement learning (RL) training strategies used by gpt-oss models are not fully detailed, the DeepSeek-R1 technical report offers a comprehensive overview of how RL training with verifiable rewards is implemented at scale.

(10) Deliberative alignment: This is the safety training approach used by gpt-oss models, designed to teach the models how to reason through safety specifications and determine when it is appropriate to refuse a request.