# college-football-sack-predictor
Machine Learning project to predict college football sacks with live gameday inference and automated messaging. 

Every Saturday in the fall, dozens of quarterbacks will drop back hundreds of times to attempt to complete a pass in college football.  If the defense can tackle the quarterback, the play results in a sack.  This result is impactful, fun, and pretty rare.  This project attempts to predict on a play by play basis the likelihood of a sack occurring, based on game status and conditions. 
# Status
Phase 1 of 7 - Data Discovery
# Architecture Overview
- Play detected (pre-snap)
  - Situational features (down, distance, field position, clock, score)
  - Weather features
  - Offense/Defense team context
- Model inference
- Confidence gate → tweet if above threshold
- Result logged to DynamoDB
- End-of-day reconciliation and summary tweet
# Project Phases
1. Data Discovery (In Progress): Feasibility, data profiling, population sizing
2. Feature Engineering: Feature selection, class imbalance strategy
3. Model Development: Training, experiment tracking, model registry
4. Live Inference Pipeline: GraphQL integration, real-time feature extraction
5. AWS Production Architecture: Lambda, EventBridge, DynamoDB
6. Confidence Threshold Tuning and X API Integration
7. Monitoring and End-of-Day Reconciliation
# Tech Stack Tools
Python, AWS (Lambda, S3, DynamoDB, EventBridge), SageMaker, CFBD API, X API
# Data Source
[College Football Database](https://collegefootballdata.com/). The Tier 3 monthly subscription is needed for live play-by-play data.
# Estimated Monthly Cost
| Service | Cost |
|---|---|
| CFBD Patreon Tier 3 | $10 |
| AWS (Lambda, S3, DynamoDB, EventBridge) | ~$5-10 |
| X API (free tier) | $0 |
| **Total** | **~$15-20/month** |
# Local Development Setup
Placeholder
# Documentation
[Docs](https://github.com/TJRader/college-football-sack-predictor/tree/main/docs)
# Key Decisions
[Architecture decision record ](https://github.com/TJRader/college-football-sack-predictor/tree/main/docs/decisions)
# License
[MIT License](https://github.com/TJRader/college-football-sack-predictor/blob/main/LICENSE)
