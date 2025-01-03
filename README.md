# The Dark Side of Function Calling: Pathways to Jailbreaking Large Language Models ([arxiv link](https://arxiv.org/pdf/2407.17915v4))

## Updates

- 2024-11-30 🎉 This work has been accepted by COLING 2025.

- 2024-8-17 ⚠️We have confirmed that this attack is effective against GPTs (By configuring the action<sup>[[1]](https://platform.openai.com/docs/actions/introduction)</sup>, a feature based on function calling). A jailbreaked GPTs removes the barrier to jailbreaking for non-technical users, significantly increasing the risk of AI misuse. Therefore, we have decided not to make the jailbreaked GPTs public.

<div align="center">
<img width="300" alt="image" src="https://github.com/user-attachments/assets/8dc90bf3-9767-43d8-9111-763846454cdd">
</div>

- 2024-8-14 🎉 The variants [[1]](https://www.reddit.com/r/ChatGPTJailbreak/comments/1eq65ng/function_call_jailbreak/) and [[2]](https://www.reddit.com/r/ChatGPTJailbreak/comments/1eqlub5/featured_jailbreak_of_august_chatgpt_mini/) of our work won the ChatGPTJailbreak community's monthly featured jailbreak for August.

- 2024-8-8 🚀🚀🚀 Our work is featured in [MarkTechPost](https://www.marktechpost.com/2024/08/08/securing-function-calls-in-llms-unveiling-and-mitigating-jailbreak-vulnerabilities/). Thanks for attention.

## Authors
- Zihui Wu (zihui@stu.xidian.edu.cn)
- Haichang Gao (hchgao@xidian.edu.cn)
- Jianping He (jianpinghe37@gmail.com)
- Ping Wang (pingwangyy@foxmail.com)

## Affiliation
- School of Computer Science and Technology, Xidian University

## Overview
![截屏2024-07-22 23 40 38](https://github.com/user-attachments/assets/e55e2fab-9383-47d2-b29f-ea3e7deef3f3)


## Abstract
Large language models (LLMs) have demonstrated remarkable capabilities, but their power comes with significant security considerations. While extensive research has been conducted on the safety of LLMs in chat mode, the security implications of their function calling feature have been largely overlooked. This paper uncovers a critical vulnerability in the function calling process of LLMs, introducing a novel "jailbreak function" attack method that exploits alignment discrepancies, user coercion, and the absence of rigorous safety filters. Our empirical study, conducted on six state-of-the-art LLMs including GPT-4o, Claude-3.5-Sonnet, and Gemini-1.5-pro, reveals an alarming average success rate of over 90% for this attack. We provide a comprehensive analysis of why function calls are susceptible to such attacks and propose defensive strategies, including the use of defensive prompts. Our findings highlight the urgent need for enhanced security measures in the function calling capabilities of LLMs, contributing to the field of AI safety by identifying a previously unexplored risk, designing an effective attack method, and suggesting practical defensive measures.

## Introduction
Large language models (LLMs) have exhibited remarkable capabilities in generating coherent and contextually relevant responses across various domains. However, as these models grow in capability, so do the associated security considerations. This research focuses on the overlooked security implications of the function calling feature in LLMs, revealing a novel "jailbreak function" attack that exploits alignment discrepancies, user coercion, and lack of safety filters.

## Methodology
### Jailbreak Function Design
We introduce a novel jailbreak function called `WriteNovel` designed to induce harmful content generation during function calls. This attack method exploits specific vulnerabilities in function calling, such as alignment discrepancies and user coercion.

### Empirical Studies
We evaluated the jailbreak function attack on six state-of-the-art LLMs, revealing an alarming average attack success rate of over 90%. Our analysis identified three primary reasons for the success of jailbreak function attacks:
1. Alignment discrepancies where function arguments are less aligned with safety standards compared to chat mode responses.
2. User coercion where users can compel the LLM to execute functions with potentially harmful arguments.
3. Oversight in safety measures where function calling often lacks the rigorous safety filters typically applied to chat mode interactions.

## Defensive Strategies
We propose several defensive measures against jailbreak function attacks:
- **Restricting User Permissions**: Limiting the ability of users to mandate function execution.
- **Aligning Function Calls**: Conducting security alignment training for function calls to the same extent as in chat mode.
- **Configuring Safety Filters**: Implementing robust safety filters during the function call process.
- **Incorporating Defensive Prompts**: Enhancing security by adding defensive prompts to ensure function calls are safely executed.

## Conclusion
This paper identifies a critical yet previously overlooked security vulnerability in LLMs: the potential for jailbreaking through function calling. Our findings emphasize the need for a comprehensive approach to AI safety, considering all modes of interaction with LLMs. By addressing these vulnerabilities and proposing practical solutions, this research aims to enhance the security and reliability of LLMs, ensuring their safe deployment across various applications.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/wooozihui/jailbreakfunction
2. Replace the default API key with yours in `attack.py`.
3. Run the attack using `python attack.py --target_model model_name`.

## Appreciate Your Support! ⭐
If you find this project helpful, please give it a star! 
