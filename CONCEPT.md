# Concept

I would like to write a custom agent myself, namely in the Kotlin programming language. I would like to use a farsighted architecture where I can extend the agent/harness/framework easily and add functionality.

Features must include

- easy addition of tasks / tools to use
- authentication / authorization features
- choosing different models - from different providers, with different APIs
    - OpenAI based
    - Claude / Anthropic based
    - others
- choosing different strategies for context compression
- choosing different strategies for other things like thinking, interaction with system prompt and 
user prompt etc.
- choosing the level of thinking
- choosing possibly other LLM model parameters to tweak if possible
- being able to configure and choose the level of autonomy the Gaiagent may do
- integration with other APIs
- possibly integration with IDEs etc.

My idea for a certain architecture is
* using KTor as the driving backend
    * thus providing the core logic and an API with which one can interact with the Gaiagent
    * possibly creating own plugins if that is suitable
* using a general approach with which I can "plug in" functionality through extension points
    * it is unclear to me which fundamental arch approach we should take
* creating the frontend as Kotlin/Compose multiplatform project

At the same token,
* I would like to be able to bundle the Desktop Compose app with the KTor server to one whole thing
* I would like to use the backend alone, for other "services" being able to be created up-front

Also:
- creating pipelines / workflows such that one can reach the output of one step into one other step
- creating automation workflows so tasks can be effectively done
- model escalation: choose, configure, decide whether and when steps use some local / own hosted 
model, and when things escalate to the cloud

## Goals 

The goals for this project are
- creating an agent which I, myself, can actually productively use very well
- putting this online as a public project to showcase myself
- making it awesome, with deep integrable features such that it can be very flexibly used
    - imagine e.g. using it inside Reaper, Krita or other programs