# Multi-Tool AI Pipeline for DataFlow Systems

This project demonstrates a proof-of-concept multi-tool AI pipeline that integrates:
- External API ingestion
- AI-based enrichment
- Storage
- Notification handling

## Data Source
JSONPlaceholder Users API  
https://jsonplaceholder.typicode.com/users

The pipeline processes the first 3 user records.

## Pipeline Stages

1. **API Integration**
   - Fetches user data from JSONPlaceholder
   - Handles partial failures gracefully

2. **AI Enrichment**
   - Generates a concise summary (1–2 sentences)
   - Classifies sentiment as enthusiastic, critical, or objective

3. **Storage**
   - Stores source data along with AI-generated analysis
   - Includes timestamp and source metadata

4. **Notification**
   - Sends a notification upon completion  
   - Notification target: 24f2002015@ds.study.iitm.ac.in

## Live Pipeline API (Deployed)

POST  
https://ai-cache-system.free.beeceptor.com/pipeline

## Sample Request

```json
{
  "email": "24f2002015@ds.study.iitm.ac.in",
  "source": "JSONPlaceholder Users"
}
