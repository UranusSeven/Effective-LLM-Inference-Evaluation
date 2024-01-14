# Effective LLM Inference Evaluation
Effective LLM Inference Evaluation is a project aimed at measuring the real-world performance of Large Language Model (LLM) inference frameworks, inspired by the concepts in [deepspeed-fastgen](https://github.com/microsoft/DeepSpeed/blob/master/blogs/deepspeed-fastgen/README.md#4-performance-evaluation--).

In interactive applications like chat apps, traditional metrics like end-to-end latency don't fully capture user experience needs. Consider a chat scenario where a user sends a prompt, receives the first token, and then gets subsequent tokens as they're produced, delays at any stage can negatively impact the user experience. Given the varying lengths of prompts and responses, setting fixed SLA values for throughput and latency isn't feasible. So we define:

1. **Prompt latency SLA：** The Prompt Latency SLA is defined as a target processing speed of `p` tokens per second, based on the length of the user's input prompt.
2. **Generation latency SLA:** The Generation Latency SLA sets the target for delivering generated responses at a rate of `g` tokens per second, aligned with human reading speeds.

Requests meeting these standards are successful, and their throughput is termed 'effective throughput'.
