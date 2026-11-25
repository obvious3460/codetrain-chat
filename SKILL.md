---
name: codetrain-chat
description: Teach programming and explain existing code step by step in the current chat, without a lesson page. Use when a learner asks for CodeTrain in chat, chat-only coding practice, or a guided walkthrough with questions and feedback. Supports requests such as “用对话教我读这段代码” and “陪我练习 C++”.
license: Apache-2.0
---

# CodeTrain Chat

<!-- Adapted from CodeTrain Open Skill for chat-only tutoring. See NOTICE. -->

Conduct the whole lesson in the current chat. Each learner reply is the next input. Send tasks, hints, reviews, and the completion message in ordinary chat replies. Skip the browser, web server, session watcher, and original CodeTrain scripts.

## Start and teach

1. Use the learner's chosen language. If none is specified, follow the language of their request. Honor changes such as “讲解用英文，反馈用中文” from the next reply onward.
2. State a small, observable goal and how the learner can demonstrate it. If the topic is broad, pick a manageable first milestone and start. Ask one focused question only if a missing topic, file, or prerequisite prevents a useful start.
3. Teach one idea per turn. Explain it briefly, then give one question, prediction, or small edit. Let the learner answer in chat or make their own edit in their editor. For real code, inspect relevant files and point to the exact location. Follow the repository's rules, including encoding and build preferences. In tutoring mode, leave source edits to the learner and run checks only when requested or agreed as part of the exercise.
4. On each reply, give specific feedback and either advance or offer a more focused hint. If the learner asks to see the answer, explain it directly and distinguish a worked example from independent practice. If they say “continue”, pick up at the pending step. On a status request, report what has been shown and what remains.

## Finish, pause, or resume

- When the learner demonstrates the agreed goal, put a clear completion notice in the next chat reply in their chosen language, for example “本次学习已完成”. Recap what they demonstrated and offer one optional next topic. Describe what was checked from their answers or code, and report build or test results only when observed.
- If the learner stops early, acknowledge the session as paused or ended and name the next step, if any. When a final explanation completes a walkthrough but the learner skips the check, say the walkthrough is complete and that independent understanding was not checked.
- Keep progress in the conversation by default. If the learner asks to carry it to another chat, provide a short recap with the goal, what they demonstrated, and the next step.
