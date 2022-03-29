# collaboration

This repo is about understanding and implementing hybrid intelligence collaboration. Feel free to raise issues and make PRs.

## Prerequisites

1. A unix or unix-like x86 machine
1. python 3.8 or higher.
1. Running in a virtual environment (e.g., conda, virtualenv, etc.) is highly recommended so that you don't mess up with the system python.
1. `pip install -r requirements.txt`

## Phase 1 - Understand HI collaboration

During our meeting, we've come up with [some keywords](keywords.yaml) to understand what HI collaboration is. We want to extend this with the following points:

- Add more keywords. Feel free to append what's necessary to the yaml file.
- Manually add relations (i.e., edges) between the entities (i.e., keywords)
  - I was gonna use [the MIRO board](https://miro.com/welcomeonboard/TzhzVmNsem1SVG56c2d2d0J4Yk9UbENuYUJWcExEcUVTRmRMdXRSczZldmMyZVZkdVF4alFiZjVlZ2hWZUZnUnwzNDU4NzY0NTIxMTEzMTM1NDY1?invite_link_id=38942586988) but the low participation rate shows that this is not the most effective way.
  - Can someone come up with something else?
- Automatically add relations. Since we are HI, we can also ask machines to do this!
  - [Try TransE](https://proceedings.neurips.cc/paper/2013/file/1cecc7a77928ca8133fa24680a88d2f9-Paper.pdf)
  - Map your concepts to Wikidata and then extract a connected component that contains all of them, with some extra entities as a bonus.

Since we are all about HI, we want to use the edges extracted by both humans and machines!

## Phase 2 - Build an app to collaborate with machines

Try below for a streamlit demo:

```sh
streamlit run app.py
```

### Why are we doing this?

Currently human-machine collaboration experiments are all done differently by researchers. It's difficult to reproduce their results. We think that we can have more canonical format for human-machine collaboration so that people can just "plug-in" what they want to experiment into this setup.

### What do we need?

1. We need an app framework. [Streamlit](https://streamlit.io/) might be a good way to achieve this.
1. We need tasks and skills.
   - Tasks are what we want to solve together with machines (e.g., puzzle solving, answering multiple-choice questions, partner selection, overcoming weak supervision, etc.)
   - Skills are what we want machines to have (e.g., theory of mind, affection, sympathy, trust, self-awareness, explanation, episodic memory, semantic memory, etc.)

The outcome of Phase 1 will help us to find the necessary skills and how they are related.

## Examples

### Partner selection with a theory-of-mind AI

In this example, I as a human want to select a human partner. In this task, an AI equipped with the skill of a theory of mind will help me. I see a list of humans with their pictures, and other information. The AI can assess what I think about the candidiates and what the candidates might think about me. Hopefully this makes it easier for me to select my partner.

Perhaps theory of mind is not the best skill that the AI should have in this task. Since from Phase 1 we know how the skills are related, we can select another skill that the AI should have and then proceed.

This is Tiffany's work. Feel free to correct it, Tiffany, haha.

### Question answering with an explicit-memory-system AI

This is actually Tae's PhD research.

The task is to answer questions (e.g., Where is Tiffany's laptop?). In this task, I might have seen Tiffany's laptop and answer the question correctly. If I haven't, an AI with an episodic memory system can help me.

Again, other skills might be more desirable.

### Puzzle solving with an affective AI

Puzzle solving can be a stressful task. An AI that can understand the emotion of the human and act accordingly might be helpful.

## Phase 3 - Do something with what we've learned from Phase 1 and Phase 2

So exciting.

## TODOs

1. Phase 1

## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
1. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
1. Run `make test && make style && make quality` in the root repo directory, to ensure code quality.
1. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
1. Push to the Branch (`git push origin feature/AmazingFeature`)
1. Open a Pull Request

## Authors

- [Taewoon Kim](https://taewoon.kim/)
