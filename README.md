# Contract Risk Analyzer

AI system that reads contracts, detects risky clauses, and generates a clear red-flag report.  
It combines OCR, parsing, embeddings, rules, and an LLM to help teams review contracts faster.

---

## Overview
This project analyzes long PDF contracts and highlights risk.  
It finds missing clauses, unusual terms, and inconsistencies.  
It gives a short, actionable report that any team can understand.

---

## Why this project
Manual contract review is slow and error-prone.  
Startups and small teams often miss important clauses.  
This tool speeds up review, reduces mistakes, and helps non-legal teams make better decisions.

---

## Core Features
- Upload PDF or DOCX files  
- OCR for scanned documents  
- Clause segmentation  
- Entity extraction (dates, parties, payment terms, renewal, termination)  
- Embedding-based similarity search  
- LLM-generated summaries and explanations  
- Rule-based red flag scoring  
- Downloadable risk report  
- Audit logs for transparency  

---

## Tech Stack
### Frontend
- Angular  
- Tailwind or Material UI  
- File upload + contract viewer  

### Backend
- NestJS  
- TypeScript  
- PostgreSQL  
- Prisma or TypeORM  

### AI + Services
- OCR: Tesseract or Google Vision  
- Embeddings: OpenAI / Cohere / Local model  
- LLM: GPT, Claude, or local LLM via Ollama  
- Vector DB: Pinecone / Weaviate / Milvus  
- Storage: AWS S3 or DigitalOcean Spaces  

---

## Project Structure
contract-risk-analyzer/
├── frontend/
│ └── contract-risk-analyzer-ui/
├── backend/
│ └── contract-risk-analyzer-api/
├── services/
│ ├── ocr-service/
│ ├── parser-service/
│ ├── embeddings-service/
│ └── llm-service/
├── docs/
│ └── architecture-diagrams/
└── README.md



## How it works (high level flow)
1. User uploads a contract
2. OCR runs if needed
3. Text is cleaned and segmented
4. Parser extracts important fields
5. Embeddings stored in vector DB
6. LLM generates summary + explanation
7. Rules engine computes risk score
8. Final report is shown and can be exported

## API Modules (Backend)
- Upload Module — handles PDF/DOCX
- OCR Module — scanned text extraction
- Parser Module — NER + clause split
- Embedding Module — vector generation
- Analyzer Module — LLM + rules
- Report Module — builds final output

## Frontend UI Plans
- Upload page
- Contract viewer
- Red flag list
- Clause-by-clause explanation
- PDF export button
- History page

## Setup Instructions
### Clone the repo
git clone https://github.com/
<your-username>/contract-risk-analyzer.git

### Install frontend


cd frontend/contract-risk-analyzer-ui
npm install
npm start

### Install backend


cd backend/contract-risk-analyzer-api
npm install
npm run start:dev


## Roadmap (MVP)
- [ ] File upload
- [ ] OCR pipeline
- [ ] Clause segmentation
- [ ] Entity extraction
- [ ] Embedding + vector search
- [ ] LLM summary + flags
- [ ] Risk scoring
- [ ] Export PDF report
- [ ] Full UI Flow

## License
MIT License.

## Contact
Built by Tarun Jawla. For questions or collaboration, feel free to reach out.