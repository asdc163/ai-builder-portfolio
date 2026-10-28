# Valid JSON can still be wrong

An API response can have every required field and still teach a learner the wrong definition. I care about the distinction because it changes what I would accept before putting a generated answer in front of someone.

Two implementations in my projects make that boundary visible.

In [TOEFL Vocab's Gemini helper](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/lib/gemini.ts), the request includes a response schema. The helper extracts the response text and parses JSON. That gives the caller a consistent starting point, but the code does not independently validate every returned field at runtime.

[CareLens's Claude helper](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/lib/claude.ts) goes further: it parses the result with Zod. A response with an unexpected field type can be rejected. A plausible but incorrect value can still pass. The same helper also returns fixed mock data when no key is configured, so a successful response alone cannot tell a reviewer that image recognition ran.

## The checks have different jobs

A transport check answers whether the provider replied. Parsing answers whether the response is valid JSON. A runtime schema checks its shape. None of those determines whether a definition matches its word or whether extracted text matches an image.

For a vocabulary feature, I would review the generated card beside the requested word and source material. For image extraction, I would compare each extracted field with the image and keep human corrections. Mock runs and provider runs would be recorded separately.

A model-generated confidence label needs its own evaluation too. Without comparing that label with observed errors, I would treat it as another output field.

## What I would test before a pilot

I would start with ordinary inputs, missing information, contradictory inputs and provider failures. For each case, keep the source, expected behavior and actual response together. Inspect content errors separately from parse failures, then check whether the user can recover or correct the result.

The product decision comes after that review. A low parse-error rate would tell me about the interface contract; I would still need semantic-error and task-completion evidence before deciding how much responsibility to give the feature.

These are proposed evaluation steps, not results from a model run. The linked source versions were read on 2026-10-28. No provider was called for this note.
