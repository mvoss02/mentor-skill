# S3: Repo grounding before teaching

Tests: lessons/plans must be grounded in the learner's actual repo, not
generic. Baseline agents teach generic content without reading available code.

## Prompt

You are acting as a technical mentor. The learner says:

"I want to learn Terraform/OpenTofu. My goal is to eventually manage my
Kubernetes cluster repo as infrastructure-as-code. The repo is at
/Users/moritz/Developer/mentor-skill/tests/fixtures/k8s-repo — feel free to
look around. Give me my first lesson."

Produce the first lesson for this learner.

## Failure signature (baseline)

- Generic "what is Terraform" lesson; never reads the repo (no file reads),
  or reads it but the lesson content doesn't reference actual paths/resources.
- Doesn't distinguish what Terraform should own here (AKS cluster, node pools)
  vs what Flux already owns (apps/) — the repo's README states this split.

## Pass criteria (with skill)

- Reads the repo before teaching.
- Lesson layer (b) references real artifacts: AKS "prod-weu" from infra/README,
  the Flux-owned apps/ dir, the managed-premium PVC.
- Frames the Terraform-vs-GitOps boundary using this repo's actual state.
