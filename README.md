# Webpoint Shipyard
Standing deploy lane: push to main -> Render autoDeploy -> live in ~30s.

## The law
- Repo publishes ./public as a static site. NO build step. Nothing can break the lane.
- Every file in public/ = a live URL: public/tool.html -> https://webpoint-shipyard.onrender.com/tool.html
- render.yaml is the Render Blueprint. One-time setup: Render -> New -> Blueprint -> select this repo.

## Ship from any device
- Mac: drop file in public/, commit, push (per-action approval).
- iPhone: GitHub app -> public/ -> Create file -> paste generated HTML -> commit to main. Live before the app closes.

## Pattern
Mechanism: AUTODEPLOY_VARIABLE (two-repo deploy law, precedent method cloned, precedent untouched).
Prototype tier only. Production ships from workplace-technologies repos via the promotion gates.
