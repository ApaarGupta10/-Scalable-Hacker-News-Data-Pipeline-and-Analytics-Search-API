# Scalable Hacker News Data Pipeline and Analytics/Search API

## Overview
This project is a large-scale data pipeline and backend analytics/search API built on top of the Hacker News dataset.

It ingests raw Hacker News records, transforms and stores stories/comments in PostgreSQL, and exposes FastAPI endpoints for:
- story retrieval
- analytics on domains and activity
- keyword/text-based search

The goal of this project is to practice scalable data processing, backend API design, search, and analytics over a large real-world dataset.

---

## Problem Statement
Large public discussion datasets contain useful signals about trends, engagement, domains, and topic activity, but raw records are difficult to query efficiently.

This project solves that by:
- selectively ingesting large Hacker News data
- transforming raw records into queryable database tables
- creating analytics-focused endpoints
- supporting search across stories and comments

---

## Dataset
Source: Hacker News dataset from Hugging Face

The complete raw dataset is not included in this repository because of size.  
Instead, this repo provides:
- code to ingest and transform the dataset
- instructions to download data
- optional sample subset for local testing

---

## Features
### Data Pipeline
- filter story and comment records
- extract useful columns from raw data
- clean text and timestamps
- derive date and domain fields
- batch load into PostgreSQL

### Analytics API
- summary metrics
- top domains
- top stories
- activity over time

### Search API
- search stories by title/text
- filter by score, date, and domain
- retrieve individual story details

---

## Tech Stack
- Python
- FastAPI
- PostgreSQL
- SQLAlchemy
- Pydantic
- Pandas / Polars
- Docker
- Pytest

---

## Architecture
Raw Hacker News Data  
→ Ingestion / Transformation Pipeline  
→ PostgreSQL  
→ FastAPI Analytics/Search API

You can add an architecture diagram in `docs/architecture.png`.

---

## Project Structure
```text
hn-data-intelligence/
│
├── app/
├── pipeline/
├── tests/
├── docs/
├── sample_data/
├── .env.example
├── Dockerfile
├── requirements.txt
└── README.md
