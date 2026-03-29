---
title: "Trying to Catch Up on Agentic AI"
date: 2026-03-27
permalink: /posts/2026/03/trying-to-catch-up-on-agentic-ai/
published: false
---

After attending ASPLOS, one thing became hard to ignore: everybody seems to be talking about agentic AI.

That feeling was both exciting and uncomfortable. For a long time, my use of large language models was fairly lightweight and mostly web-based. I mainly used them while writing papers, including this one. My usual workflow was to first write down the core idea, whether it was a data point or a design direction, knowing that my advisor would later ask me to refine it. Then I would ask GPT to act like me while I played the role of my advisor. At this point, I already have a decent sense of what she does not like and a vague sense of what she does like, so I would keep pushing GPT to revise based on that feedback until it felt closer to what my advisor would actually want. Poor GPT, but it often produced surprisingly useful feedback. Still, that kind of use felt bounded and very sequential: ask a question, get a response, revise, and move on. Only very recently, at Shenlong's suggestion, did I try something more hands-on by using a coding-centered workflow for vibe coding a demo application for a recently submitted paper. I was able to get something done in about a week that I would normally estimate to take two to three weeks.

After the recent submission, I had some free time and decided to attend ASPLOS, which I had actually never attended in my entire Ph.D. career. To be honest, I was not deeply interested in many of the papers. For some, I simply had no idea what they were doing; for others, many papers started to feel very similar. Paper A and Paper B would identify roughly the same problem and propose closely related solutions, with only small differences here and there. At this stage, it made me feel that if you are targeting a conference, speed matters a lot. Then, while chatting with friends, I heard about how they were powering their research workflows with agents, and I was genuinely shocked. They had many different agents doing all kinds of tasks, and when I heard how quickly some of them were able to move from idea to paper submission, I was even more shocked.

As a systems Ph.D. student, I care a lot about end-to-end efficiency. If agents can help optimize the entire pipeline of doing research and writing papers, the potential gains in both speed and scalability seem huge to me. What I do not yet know is how to get there myself.

That uncertainty is exactly why I am writing this post. This is the starting point of learning how to build that workflow for myself.

My goal is simple. I already have several agent ideas that I think could help me personally. They may not be useful to everyone, but I want to document the steps I am taking. As much as possible, I want to avoid writing the code myself when an agent can do the task. At the same time, I still want to inspect the code carefully and make sure it looks correct to me.

I also decided that the actual code for this effort should live outside this website repo. I created a separate sandbox repo, `AgentPang`, where I can keep the scripts, prompts, demos, and experiments that grow out of this document. For now I want that repo to stay private, because I am still learning and do not yet know what parts of this workflow are truly worth sharing.

## What I am starting with

For the machine itself, I bought a low-end Mac Mini with a 512 GB drive. I want a dedicated box for these experiments, and at least at the beginning I want to keep it a little isolated and not immediately connect it to my Apple account.

On the workflow side, I still expect to use web-based GPT for drafting and pressure-testing ideas, because that is the workflow I already know. But I also want to spend much more time in VS Code with Codex, because the whole point of this exercise is to move beyond a browser chatbot or a coder that only handles one specific task at a time.

The first commands I used were:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install cmake llvm python node faiss
```

The reason for that setup is pretty straightforward:

- `Homebrew` gives me a clean way to manage packages on macOS.
- `cmake` is there because native dependencies still show up all the time.
- `llvm` is there because my instincts are still very systems-oriented, and I want compiler tooling nearby.
- `python` will probably be the main glue language for scripting, orchestration, and small agent-related utilities.
- `node` is there because a lot of local agent and app tooling seems to assume a JavaScript ecosystem.
- `faiss` is there because I expect to eventually experiment with retrieval, indexing, or local memory, even if I do not use it right away.

A few practical references I looked at while getting started:

- https://zhuanlan.zhihu.com/p/2007147036185744607
