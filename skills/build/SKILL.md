---
name: build
description: Implement a spec in one pass at low effort, then list the assumptions made so they can be reviewed. The spec is usually the output of grill-me.
effort: low
disable-model-invocation: true
argument-hint: "[spec, or a path to it]"
---

# Build

Spec: $ARGUMENTS. If empty, the spec from the conversation.

1. Implement it in one pass. Keep it simple: nothing the spec does not ask for.
2. End with a short list of the assumptions you made where the spec was silent.
