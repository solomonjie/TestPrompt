四个级别
1. Direct User Interaction:直接和大模型进行交互，自己写完整的prompt
2. Agent/Assistant proxy:和一个大模型应用进行交互，用户提出自己的需求，应用会将用户的需求和自己优化的prompt 集成，然后交互给大模型。
3. Agent/Assistant: 需要调用外部的函数或接口功能，需要用户确认，等用户确认执行调用，获取返回结果后和应用原有的promt 结合在一起和大模型进行交流。
4. Autonomous agent: agent 接收到用户请求后，解释用户请求，制订计划，然后指定检查点，然后开始自动化的按照制订的计划进行执行。有可能执行到某些点后需要用户的确认和反馈，然后接受反馈对计划进行调正，然后继续执行。

如果复杂任务可能需要多个Agent，这些agent一起工作来完成一个复杂问题。它们之间会有 agent 的交互问题。
单Agent主要组件包括“
1. profile/persona, Profile 和 Persona。它们 一般叫做 system prompt，主要是指导 agent 如何 完成任务，如何做反应等。比如包含用户的背景（程序员，作家），生理信息（性别，年纪）等。
2. actions,
3. knowledge/memory,
4. reasoning/evaluation
5. planning/feedback.
