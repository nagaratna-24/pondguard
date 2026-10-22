# PondGuard

An AI early-warning assistant that tells a small shrimp or fish farmer, in Kannada, what may happen to the pond tonight and what to do about it.

Built for DevHost 2026 (Synergia 26, Sahyadri College of Engineering & Management), Problem Statement 1.1: Early Disease & Water-Quality Alerts for Small Aquaculture Farms.

## Status
This is a concept submission for Round 1. A working prototype is planned for Round 2.

## The problem
Small aquaculture farmers lack the monitoring tools that large farms have. Water quality can fall suddenly overnight, and disease can spread before it is noticed, leading to high-value losses.

## How PondGuard works
1. TEST: The farmer enters pH, dissolved oxygen, temperature and ammonia from a low-cost test kit (about 2 minutes a day), or uploads a photo of the shrimp or fish.
2. CHECK: A hybrid risk engine gives Safe, Warning or Critical with a reason. It combines:
   - Rule layer: species-wise safe ranges (for example, dissolved oxygen below about 4 mg/L is stress).
   - ML trend model: predicts trouble from falling trends.
   - Weather forecast: heavy rain or cloud can raise the overnight oxygen-crash risk.
   - Photo model: flags suspected disease with a confidence score. It never gives a final diagnosis; if unsure, it says "refer to fisheries officer".
3. ACT: A Kannada SMS/WhatsApp alert with clear steps, a 7-day pond history, and one-tap call to a fisheries officer.

## Planned tech stack
Python, FastAPI, SQLite/Supabase, Streamlit (prototype), scikit-learn/XGBoost, TensorFlow Lite or PyTorch, Twilio SMS / WhatsApp Cloud API / Telegram bot (demo), Open-Meteo weather API.

## Open datasets (used instead of live sensors)
- Mendeley "Aquaculture - Water Quality Dataset" (4,300 samples): DOI 10.17632/y78ty2g293.1
- ShrimpDiseaseImageBD, Mendeley (1,149 images): DOI 10.17632/jhrtdj9txm.3
- Kaggle fish-disease image dataset (442 images, 7 classes)

## Important note on numbers
Figures such as early-warning time, recall and loss reduction in our presentation are pilot targets, not achieved results. The proposed pricing is our own proposal, not market data.

## Team
Tech Minds

