# quantitative-market-screener
Quantitative Market Screener & Algorithmic Trading System
Ein in Python entwickeltes, datengetriebenes Analyse-Tool zur Identifikation asymmetrischer Marktchancen. Das System kombiniert stochastische Modellierung, Optionsmarkt-Pricing und NLP-basierte Sentiment-Analyse, um strategische Marktbewegungen (Top-Down Sector Rotation) und mikrostrukturelle Trends zu evaluieren.
Executive Summary
Dieses Projekt demonstriert die automatisierte Verarbeitung großer Finanzdatensätze zur fundierten Entscheidungsfindung. Es übersetzt theoretische Kapitalmarktmodelle in programmatische Logik und bewertet Assets anhand von sieben quantitativen Strategien, gefiltert durch strikte Risikoparameter.
Core Architecture & Strategies
Options Implied Probability (Black-Scholes & SVI): Modellierung von Volatilitätskurven zur Ableitung absoluter Preiserwartungen des Smart Moneys.
Institutional Order Flow: Z-Score-Normalisierung von Put-Call-Ratios zur Identifikation von institutionellen Positionierungen.
Probabilistic Forecasting (Markov Chains): Monte-Carlo-Simulationen und stationäre Markov-Ketten zur Berechnung der Wahrscheinlichkeit von Regimewechseln.
Market Breadth & Sector Rotation: Top-Down-Analyse von 15 Sektor-ETFs zur Bestimmung des Makro-Umfelds (Risk-On / Risk-Off) inkl. Momentum-Ranking (Micro R² Linear Regression).
NLP Sentiment Analysis (FinBERT): Dynamische Integration von RSS-Feeds und Auswertung der Nachrichten-Stimmung durch das vortrainierte Transformer-Modell FinBERT.
Technical Stack
Data Pipeline: yfinance, feedparser, requests
Quantitative & Statistical Modeling: numpy, pandas, scipy.stats, scipy.optimize
Machine Learning & NLP: transformers (Hugging Face), torch
Risk Management Engine
Integrierte Filtermechanismen blockieren vollautomatisiert Trades bei extremen Marktkonditionen (z.B. VIX-Spikes > 10%), unvorteilhaften relativen Volumina oder kritischen Distanzen zum SMA-50 (Volatilitäts-adaptiert).
