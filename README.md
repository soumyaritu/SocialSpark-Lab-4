# SocialSpark-Lab-4
What I've Done for Lab 4 (Optimise)
Configured the Golden Evaluation Suite:

Inspected 

evals/golden.json
, which measures the 3 non-negotiable behaviours: on-brand drafting, human approval gating, and A2A memory consultation.
Set up 

evals/eval_config.json
 with dual scoring: semantic match ($\ge 0.6$) and rubric-based tool quality ($\ge 0.7$).
Diagnosed & Fixed Why All 3 Tests Failed (0/3 $\rightarrow$ 3/3):

Fixed Model 404s: Switched GOOGLE_CLOUD_LOCATION to us-central1 and set models to active Vertex AI IDs (gemini-2.5-flash) in 

.env
 and eval_config.json.
Activated the A2A Memory Service: Added missing import os in 

mock_memory_agent.py
, started the server on port 8001, and linked MEMORY_AGENT_CARD_URL.
Fixed the Judge Model: Aligned the LLM-as-a-judge to gemini-2.5-flash.
Verified the Passing Baseline:

Ran adk eval and achieved a 100% pass rate:
text
Eval Run Summary
golden:
  Tests passed: 3
  Tests failed: 0

