# Nemotron-Track3-CivicLens
CivicLens AI — AI-powered public document explainer built with NVIDIA Nemotron 3 Super for the NVIDIA Hackathon Track 3.

## PROBLEM STATEMENT
Local government and public policy documents are officially available to citizens, but they remain difficult to understand due to their complexity and structure. Ward committee minutes, government circulars, and budget reports are often written in technical language, spread across multiple portals, and lack clear summaries for the public. As a result, citizens struggle to identify key information such as deadlines, eligibility rules, and required actions, leading to low civic participation and missed opportunities for public feedback.
There is also no simple way for residents to interact with civic data through natural language, meaning users cannot easily ask questions and receive grounded, context-aware answers supported by actual documents. CivicLens AI bridges this gap by transforming complex civic information into simple, understandable, and interactive insights, enabling citizens to access, understand, and engage with government decisions more effectively.

## SOLUTION
CivicLens AI addresses the challenge of understanding complex government and public documents by transforming them into simple, actionable, and citizen-friendly insights using AI-powered document intelligence.
The platform enables users to upload PDFs, policy documents, scholarship approvals, tax notices, budget reports, and civic records into a Retrieval-Augmented Generation (RAG) pipeline powered by NVIDIA Nemotron 3 Super.
Uploaded documents are automatically processed, semantically chunked, embedded into a vector database, and indexed for intelligent retrieval. Users can then interact with the system using natural-language questions and receive grounded, source-backed responses instead of manually navigating lengthy technical documents.
CivicLens AI generates:
• plain-language summaries
• action items
• deadlines & alerts
• timeline extraction
• affected-user insights
• citation-backed explanations
By combining semantic retrieval, vector search, and NVIDIA-powered AI reasoning, the platform improves accessibility, transparency, and understanding of civic and institutional information for everyday users.


## CIVICLENS AI — COMPLETE SYSTEM ARCHITECTURE

```text
┌────────────────────────────────────────────────────────────────────────────┐
│                                USER LAYER                                 │
└────────────────────────────────────────────────────────────────────────────┘

Users:
• Citizens
• Students
• Organizers
• Administrators
• Civic Teams

Users interact through:
• Web Dashboard
• AI Chat Interface
• Document Upload Portal
• Timeline Viewer
• Citation Explorer


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                              FRONTEND LAYER                               │
└────────────────────────────────────────────────────────────────────────────┘

Frontend Stack:
• Next.js
• React
• Tailwind CSS
• Framer Motion

Frontend Modules:
• Landing Page
• Dashboard
• PDF Upload Interface
• AI Chat System
• Timeline Visualization
• Alerts & Notifications
• Source Citation Viewer
• Analytics Dashboard

Core Functions:
• Upload documents
• Ask AI questions
• View summaries
• Explore citations
• Monitor timelines
• Display AI-generated insights


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                               API GATEWAY                                 │
└────────────────────────────────────────────────────────────────────────────┘

REST API Endpoints:
• /api/upload
• /api/chat
• /api/analyze
• /api/timeline
• /api/citations
• /api/dashboard
• /api/rag/query

Functions:
• Handle frontend requests
• Manage authentication
• Route AI operations
• Trigger document processing


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                              BACKEND LAYER                                │
└────────────────────────────────────────────────────────────────────────────┘

Backend Stack:
• Node.js
• Express.js
• FastAPI (AI services)

Backend Modules:
• Authentication Controller
• Document Controller
• Chat Controller
• Timeline Controller
• Citation Controller
• Analytics Controller

Responsibilities:
• File upload handling
• AI orchestration
• API processing
• User management
• Request validation
• Security middleware


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                         DOCUMENT PROCESSING LAYER                          │
└────────────────────────────────────────────────────────────────────────────┘

Document Sources:
• PDFs
• DOCX
• CSV
• Government Circulars
• Scholarship Letters
• Tax Notices
• Budget Reports
• Policy Documents

Processing Tools:
• PyMuPDF
• pdf-parse
• DOCX parsers

Processing Steps:
• Text extraction
• Metadata extraction
• Cleaning & normalization
• Section identification
• Deadline detection


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                              RAG PIPELINE                                 │
└────────────────────────────────────────────────────────────────────────────┘

RAG Components:
• LangChain
• Semantic Chunking
• Embedding Generation
• Retrieval Engine
• Context Injection

Pipeline Flow:
1. Document Chunking
2. Semantic Embedding
3. Vector Indexing
4. Similarity Retrieval
5. Context Augmentation
6. AI Reasoning

Purpose:
• Grounded AI responses
• Reduce hallucinations
• Context-aware retrieval
• Citation-based answering


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                          EMBEDDING GENERATION                             │
└────────────────────────────────────────────────────────────────────────────┘

Embedding Models:
• Sentence Transformers
• HuggingFace Embeddings

Functions:
• Convert text into vectors
• Enable semantic similarity search
• Improve contextual retrieval


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                           VECTOR DATABASE LAYER                           │
└────────────────────────────────────────────────────────────────────────────┘

Vector Store:
• ChromaDB

Stored Data:
• Semantic embeddings
• Document chunks
• Metadata
• Citation references
• Timeline references

Purpose:
• Fast semantic search
• Relevant chunk retrieval
• Context persistence


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                           NVIDIA AI REASONING                             │
└────────────────────────────────────────────────────────────────────────────┘

AI Model:
• NVIDIA Nemotron 3 Super

Access:
• NVIDIA NIM API

Capabilities:
• AI reasoning
• Summarization
• Question answering
• Civic intelligence generation
• Contextual explanations
• Deadline interpretation
• Action-item extraction

Prompt Engineering:
• Grounded prompting
• Citation-aware generation
• Context injection
• Hallucination reduction


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                          RESPONSE GENERATION                              │
└────────────────────────────────────────────────────────────────────────────┘

Generated Outputs:
• Plain-language summaries
• Action items
• Timeline extraction
• Important deadlines
• Alerts & notifications
• Recommendations
• Source citations
• Citizen-friendly explanations


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                         ANALYTICS & INSIGHTS                              │
└────────────────────────────────────────────────────────────────────────────┘

Dashboard Analytics:
• Document statistics
• AI interaction metrics
• Timeline insights
• Alert summaries
• Query analytics
• Usage patterns

Visualization:
• Charts
• Cards
• Timeline graphs
• AI insight widgets


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                           STORAGE & SECURITY                              │
└────────────────────────────────────────────────────────────────────────────┘

Storage:
• Uploaded documents
• Vector embeddings
• Chat history
• Metadata
• Logs

Security:
• JWT Authentication
• Protected APIs
• Environment variables
• Upload validation
• Middleware protection
• API key management


                                        │
                                        ▼


┌────────────────────────────────────────────────────────────────────────────┐
│                            DEPLOYMENT LAYER                               │
└────────────────────────────────────────────────────────────────────────────┘

Frontend Hosting:
• Vercel

Backend Hosting:
• Render / Railway

Version Control:
• GitHub

Environment Management:
• .env configuration

Monitoring:
• Logging
• Error handling
• Performance monitoring


┌────────────────────────────────────────────────────────────────────────────┐
│                             FINAL SYSTEM FLOW                             │
└────────────────────────────────────────────────────────────────────────────┘

User Uploads Document
        ↓
Frontend Upload Interface
        ↓
Backend API Processing
        ↓
Document Extraction
        ↓
Semantic Chunking
        ↓
Embedding Generation
        ↓
ChromaDB Vector Storage
        ↓
RAG Retrieval Pipeline
        ↓
NVIDIA Nemotron Reasoning
        ↓
Grounded AI Response
        ↓
Summary + Citations + Timeline + Alerts
        ↓
Displayed in CivicLens AI Dashboard
```

## DATA SOURCE

| Source | Type | How Ingested |
|---|---|---|
| /uploads/documents | PDF, DOCX, CSV | Manual upload through CivicLens AI dashboard |
| Scholarship Approval Letters | PDF | Uploaded by students/users through portal |
| Government Circulars | PDF, DOCX | Pre-loaded into /uploads/government_docs |
| Ward Committee Meeting Minutes | PDF, CSV | Uploaded by civic administrators |
| BBMP Budget & Financial Reports | PDF, XLSX | Added through backend ingestion pipeline |
| Property Tax Notices | PDF | Uploaded manually for citizen analysis |
| Public Tax & Revenue Documents | PDF, XLSX | Indexed through RAG document processing |
| Karnataka Policy/Bill Documents | PDF | Pre-loaded into civic policy database |
| Resident Welfare Association Notices | PDF, DOCX | Uploaded through organizer/admin dashboard |
| Infrastructure & Roadwork Notices | PDF, DOCX | Uploaded by local civic teams |
| Public Tender & Procurement Notices | PDF | Added through governance document ingestion |
| Citizen Complaint Records | CSV, DOCX | Uploaded manually for analysis & tracking |
| Election & Ward Information | PDF, CSV | Preloaded into governance datasets |
| CivicLens Uploads Directory | PDF, CSV, DOCX | Automatically stored after upload |
| ChromaDB Vector Store | Vector Embeddings | Generated automatically during embedding pipeline |
| Timeline & Deadline Metadata | Structured AI Metadata | Extracted dynamically from uploaded documents |
| Source Citations & References | Metadata | Generated automatically during RAG retrieval |
| Citizen AI Chat Queries | Natural Language Text | Processed in real-time through AI assistant |
| NVIDIA Nemotron AI Responses | AI Generated Insights | Generated during summarization and Q&A pipeline |



```text
CIVICLENS AI — COMPLETE RAG PIPELINE FLOW

┌────────────────────────────────────────────────────────────────────────────┐
│                           1. DOCUMENT INGESTION                           │
└────────────────────────────────────────────────────────────────────────────┘

Sources:
• User-uploaded PDFs
• Scholarship documents
• Government circulars
• Budget reports
• Ward committee records
• Tax notices
• Policy documents
• Public announcements
• Resident welfare notices

        ↓

Frontend Upload Dashboard
(Next.js + Tailwind UI)

        ↓

Backend Upload API
(FastAPI / Express.js)

        ↓

Files stored in:
 /uploads/documents


┌────────────────────────────────────────────────────────────────────────────┐
│                           2. DOCUMENT PROCESSING                          │
└────────────────────────────────────────────────────────────────────────────┘

Uploaded documents are processed using:
• PyMuPDF
• pdf-parse
• DOCX parsers

Extract:
• raw text
• page numbers
• headings
• metadata
• dates
• deadlines

        ↓

Clean & Normalize Text:
• remove noise
• fix encoding
• remove duplicate spaces
• preserve sections


┌────────────────────────────────────────────────────────────────────────────┐
│                               3. CHUNKING                                │
└────────────────────────────────────────────────────────────────────────────┘

Large documents are split into smaller chunks.

Chunking Strategy:
• semantic chunking
• paragraph-aware splitting
• overlapping chunks for context retention

Example:
Chunk 1 → Scholarship approval details
Chunk 2 → Required documents
Chunk 3 → Submission deadlines

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                        4. EMBEDDING GENERATION                            │
└────────────────────────────────────────────────────────────────────────────┘

Each chunk is converted into vector embeddings using:
• sentence-transformers
• HuggingFace embeddings

Purpose:
Convert text into semantic numerical vectors for similarity search.

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                           5. VECTOR DATABASE                              │
└────────────────────────────────────────────────────────────────────────────┘

Embeddings stored inside:
• ChromaDB Vector Store

Stored Data:
• embeddings
• source references
• page numbers
• metadata
• chunk IDs

Purpose:
Fast semantic retrieval of relevant information.

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                         6. USER QUESTION INPUT                            │
└────────────────────────────────────────────────────────────────────────────┘

Citizen asks natural questions:

Examples:
• What changed in this policy?
• What should I do next?
• What are the important deadlines?
• Who is affected?
• Explain this scholarship approval.

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                          7. QUERY EMBEDDING                               │
└────────────────────────────────────────────────────────────────────────────┘

User query is converted into embeddings.

Purpose:
Match query semantically against stored document chunks.

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                          8. RETRIEVAL ENGINE                              │
└────────────────────────────────────────────────────────────────────────────┘

Retriever searches ChromaDB for:
• most relevant chunks
• highest semantic similarity
• contextual relevance

Retrieved:
• relevant document sections
• deadlines
• actions
• references

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                         9. CONTEXT AUGMENTATION                           │
└────────────────────────────────────────────────────────────────────────────┘

Retrieved chunks are injected into AI prompt.

Prompt contains:
• retrieved context
• source references
• instructions
• user question

Prompt Example:

“You are a civic AI assistant.
Answer ONLY using provided document context.
Explain in simple language.
Provide:
- summary
- action items
- deadlines
- affected groups
- citations”

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                   10. NVIDIA NEMOTRON AI REASONING                        │
└────────────────────────────────────────────────────────────────────────────┘

Context sent to:
• NVIDIA Nemotron 3 Super

Using:
https://integrate.api.nvidia.com/v1

Nemotron performs:
• reasoning
• summarization
• contextual explanation
• grounded response generation

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                        11. RESPONSE GENERATION                            │
└────────────────────────────────────────────────────────────────────────────┘

Generated Output:
• plain-language summary
• key decisions
• action items
• deadlines
• alerts
• affected groups
• recommendations

Example:
✔ Scholarship approved
✔ Submit bank details before Aug 15
✔ Orientation on Sept 1

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                          12. SOURCE CITATIONS                             │
└────────────────────────────────────────────────────────────────────────────┘

System attaches:
• page references
• paragraph references
• source document links
• citation metadata

Purpose:
• transparency
• grounded accuracy
• trustworthiness

        ↓


┌────────────────────────────────────────────────────────────────────────────┐
│                         13. FRONTEND DASHBOARD                            │
└────────────────────────────────────────────────────────────────────────────┘

Frontend displays:
• AI summary cards
• alerts
• deadlines
• citations
• timeline
• AI chat
• confidence scores

Features:
• glassmorphism UI
• AI chat assistant
• timeline extraction
• multilingual support
• PDF preview
• action alerts


┌────────────────────────────────────────────────────────────────────────────┐
│                         14. CONTINUOUS USER CHAT                          │
└────────────────────────────────────────────────────────────────────────────┘

Users continue asking:
• follow-up questions
• clarification requests
• document-specific queries

System re-runs:
Retrieval → Context Injection → Nemotron Response

Maintaining:
• conversational memory
• document grounding
• contextual continuity


┌────────────────────────────────────────────────────────────────────────────┐
│                         FINAL OUTPUT OF SYSTEM                            │
└────────────────────────────────────────────────────────────────────────────┘

CivicLens AI transforms complex civic and government documents into:
✔ understandable insights
✔ actionable guidance
✔ grounded AI responses
✔ citizen-friendly explanations
✔ transparent governance intelligence
```

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js, React, TypeScript, Tailwind CSS |
| UI & Animations | Framer Motion, Lucide React, Recharts |
| Dashboard & Visualization | Glassmorphism UI, Responsive Dashboard Components |
| Backend | Node.js, Express.js, FastAPI (AI Services) |
| Runtime Environment | Python 3.11+, Node.js |
| LLM / AI Model | NVIDIA Nemotron 3 Super via NVIDIA NIM API |
| API Integration | OpenAI-compatible NVIDIA API |
| Embeddings | Sentence Transformers, HuggingFace Embeddings |
| RAG Framework | LangChain |
| Vector Store | ChromaDB (semantic vector database) |
| Document Processing | PyMuPDF, pdf-parse, DOCX parsers |
| Chunking & Retrieval | Recursive Text Splitter, Semantic Chunking |
| Semantic Search | Vector Similarity Retrieval |
| Source Citation Engine | Metadata-based Citation Retrieval |
| AI Prompt Engineering | Context-aware Grounded Prompting |
| File Upload Handling | Multer / FastAPI UploadFile |
| Authentication | JWT Authentication, Middleware Validation |
| Environment Management | dotenv (.env configuration) |
| HTTP Communication | Axios, Fetch API |
| Data Storage | ChromaDB, Local File Storage |
| AI Chat System | Contextual Conversational Retrieval |
| Timeline Extraction | AI-based Event & Deadline Detection |
| Multi-language Support | AI Translation Pipeline |
| Voice Features | Web Speech API (Text-to-Speech) |
| Version Control | GitHub |
| Frontend Deployment | Vercel |
| Backend Deployment | Render / Railway |
| Styling & Responsiveness | Tailwind CSS Responsive Design System |
| Logging & Monitoring | Custom Logger Middleware |
| Security | API Key Protection, Upload Validation, CORS |
| Document Intelligence | RAG-based Semantic AI Retrieval Pipeline |
| Civic Intelligence Engine | NVIDIA Nemotron Reasoning + Context Retrieval |


## API End Points

| Method | Path | Auth | Description |
|---|---|---|---|
| POST | /api/auth/register | Public | Register new user account |
| POST | /api/auth/login | Public | Login user and return JWT token |
| GET | /api/auth/profile | User | Retrieve authenticated user profile |
| POST | /api/documents/upload | User | Upload PDF/DOCX/CSV government documents |
| GET | /api/documents | User | Retrieve uploaded documents list |
| GET | /api/documents/{id} | User | Get specific document details |
| DELETE | /api/documents/{id} | User | Delete uploaded document |
| POST | /api/rag/ingest | Admin | Process and index uploaded documents into vector DB |
| GET | /api/rag/stats | Public | View indexed document and chunk statistics |
| POST | /api/rag/query | User | Perform semantic document retrieval |
| POST | /api/chat | User | Ask questions about uploaded documents |
| GET | /api/chat/history | User | Retrieve previous AI conversations |
| DELETE | /api/chat/history | User | Clear user chat history |
| POST | /api/analyze/summary | User | Generate AI-powered document summary |
| POST | /api/analyze/timeline | User | Extract timelines, deadlines, and events |
| POST | /api/analyze/actions | User | Generate action items and recommendations |
| POST | /api/analyze/citations | User | Generate source-backed citations |
| GET | /api/dashboard/summary | User | Fetch dashboard analytics & insights |
| GET | /api/dashboard/alerts | User | Retrieve important alerts and deadlines |
| GET | /api/dashboard/timeline | User | Retrieve extracted document timeline |
| GET | /api/citations/{documentId} | User | Retrieve source citations for a document |
| POST | /api/translate | User | Translate AI responses into local languages |
| POST | /api/voice/read | User | Convert AI summaries into speech |
| POST | /api/nvidia/generate | Internal | Generate responses using NVIDIA Nemotron |
| POST | /api/nvidia/embeddings | Internal | Generate vector embeddings for RAG pipeline |
| GET | /api/system/health | Public | Backend health and status check |
| GET | /api/system/version | Public | Retrieve API version information |
| GET | /api/system/stats | Admin | View platform usage statistics |


## Key Features

RAG-Powered Civic Intelligence
Every AI response is grounded using retrieved document chunks from the vector database. CivicLens AI generates structured, source-backed answers with summaries, deadlines, action items, affected groups, and citation references to reduce hallucinations and improve transparency.

AI-Powered Document Understanding
Users can upload government circulars, scholarship approvals, policy documents, tax notices, and public reports. The platform automatically extracts, processes, and explains complex information in simple citizen-friendly language.

Semantic Search & Vector Retrieval
Documents are intelligently chunked, embedded, and indexed into ChromaDB for semantic retrieval. This allows users to ask natural-language questions and receive context-aware answers instead of keyword-based search results.

Source Citations & Transparency
Every generated response includes source references, page citations, and contextual traceability, helping users verify where information originated from inside uploaded documents.

Timeline & Deadline Extraction
The platform automatically detects important dates, deadlines, approval timelines, submission windows, and civic events from uploaded documents and displays them in an interactive timeline dashboard.

AI Chat Assistant
Citizens can interact conversationally with uploaded documents through an AI-powered assistant capable of answering follow-up questions, explaining policies, and simplifying technical government language.

Action Item Detection
CivicLens AI identifies important actions users must take, such as scholarship submission steps, tax deadlines, required approvals, or compliance tasks, and highlights them automatically.

Role-Based Dashboard Access
The platform supports role-based access for residents, organizers, and administrators. Different dashboard sections and controls are displayed dynamically based on authenticated user roles.

Modern AI SaaS Dashboard
Built with a futuristic glassmorphism-inspired UI featuring analytics cards, AI summaries, alerts, citations, timeline visualization, and responsive civic intelligence dashboards.

Multi-Document Intelligence
Users can upload and analyze multiple documents simultaneously, allowing the system to connect related policies, notices, and governance records into a unified AI-powered civic knowledge system.

Secure Document Processing
Uploaded documents are validated and securely processed through backend middleware with protected API routes, environment-based key management, and upload validation pipelines.

NVIDIA Nemotron Integration
The platform uses NVIDIA Nemotron 3 Super through NVIDIA NIM APIs for reasoning, summarization, contextual explanation, and grounded AI response generation.

Scalable RAG Architecture
The system follows a modular Retrieval-Augmented Generation architecture using LangChain, semantic embeddings, ChromaDB vector storage, and contextual AI retrieval pipelines designed for scalable civic intelligence applications.

## FOLDER STRUCTURE
``` text
CIVICLENS-AI/
│
├── frontend/
│   │
│   ├── public/
│   │   ├── images/
│   │   │   ├── logos/
│   │   │   ├── backgrounds/
│   │   │   ├── dashboard/
│   │   │   └── icons/
│   │   │
│   │   ├── animations/
│   │   └── favicon.ico
│   │
│   ├── components/
│   │   │
│   │   ├── layout/
│   │   │   ├── Navbar.jsx
│   │   │   ├── Sidebar.jsx
│   │   │   ├── Footer.jsx
│   │   │   └── PageWrapper.jsx
│   │   │
│   │   ├── dashboard/
│   │   │   ├── AnalyticsCards.jsx
│   │   │   ├── AlertsPanel.jsx
│   │   │   ├── TimelineWidget.jsx
│   │   │   ├── AIInsights.jsx
│   │   │   └── StatisticsCards.jsx
│   │   │
│   │   ├── upload/
│   │   │   ├── UploadBox.jsx
│   │   │   ├── FilePreview.jsx
│   │   │   ├── UploadProgress.jsx
│   │   │   └── DragDropZone.jsx
│   │   │
│   │   ├── chat/
│   │   │   ├── ChatBox.jsx
│   │   │   ├── ChatMessage.jsx
│   │   │   ├── SuggestedQuestions.jsx
│   │   │   └── AIResponseCard.jsx
│   │   │
│   │   ├── citations/
│   │   │   ├── CitationCard.jsx
│   │   │   └── SourceViewer.jsx
│   │   │
│   │   ├── timeline/
│   │   │   ├── Timeline.jsx
│   │   │   ├── TimelineEvent.jsx
│   │   │   └── DeadlineCard.jsx
│   │   │
│   │   ├── voice/
│   │   │   └── VoiceReader.jsx
│   │   │
│   │   └── common/
│   │       ├── Loader.jsx
│   │       ├── Modal.jsx
│   │       ├── Toast.jsx
│   │       └── Button.jsx
│   │
│   ├── pages/
│   │   ├── index.js
│   │   ├── dashboard.js
│   │   ├── upload.js
│   │   ├── chat.js
│   │   ├── citations.js
│   │   ├── timeline.js
│   │   ├── analytics.js
│   │   ├── login.js
│   │   ├── register.js
│   │   └── settings.js
│   │
│   ├── services/
│   │   ├── api.js
│   │   ├── authService.js
│   │   ├── documentService.js
│   │   ├── chatService.js
│   │   ├── citationService.js
│   │   └── analyticsService.js
│   │
│   ├── hooks/
│   │   ├── useAuth.js
│   │   ├── useChat.js
│   │   └── useUpload.js
│   │
│   ├── context/
│   │   ├── AuthContext.js
│   │   ├── ChatContext.js
│   │   └── ThemeContext.js
│   │
│   ├── styles/
│   │   ├── globals.css
│   │   ├── animations.css
│   │   ├── dashboard.css
│   │   └── glassmorphism.css
│   │
│   ├── utils/
│   │   ├── constants.js
│   │   ├── helpers.js
│   │   ├── validators.js
│   │   └── formatters.js
│   │
│   ├── package.json
│   ├── next.config.js
│   ├── tailwind.config.js
│   ├── tsconfig.json
│   └── README.md
│
│
├── backend/
│   │
│   ├── config/
│   │   ├── db.js
│   │   ├── nvidiaConfig.js
│   │   ├── chromaConfig.js
│   │   └── envConfig.js
│   │
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── documentController.js
│   │   ├── chatController.js
│   │   ├── timelineController.js
│   │   ├── citationController.js
│   │   ├── analyticsController.js
│   │   └── notificationController.js
│   │
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   ├── uploadMiddleware.js
│   │   ├── validationMiddleware.js
│   │   ├── errorMiddleware.js
│   │   └── rateLimitMiddleware.js
│   │
│   ├── models/
│   │   ├── User.js
│   │   ├── Document.js
│   │   ├── ChatHistory.js
│   │   ├── Citation.js
│   │   └── Analytics.js
│   │
│   ├── routes/
│   │   ├── index.js
│   │   ├── authRoutes.js
│   │   ├── documentRoutes.js
│   │   ├── chatRoutes.js
│   │   ├── timelineRoutes.js
│   │   ├── citationRoutes.js
│   │   ├── analyticsRoutes.js
│   │   └── notificationRoutes.js
│   │
│   ├── services/
│   │   ├── extractorService.js
│   │   ├── nvidiaService.js
│   │   ├── summaryService.js
│   │   ├── timelineService.js
│   │   ├── citationService.js
│   │   ├── translationService.js
│   │   ├── embeddingService.js
│   │   ├── notificationService.js
│   │   └── speechService.js
│   │
│   ├── rag/
│   │   ├── ingestion/
│   │   │   ├── ingestDocuments.js
│   │   │   ├── cleanText.js
│   │   │   └── metadataExtractor.js
│   │   │
│   │   ├── chunking/
│   │   │   ├── semanticChunker.js
│   │   │   └── recursiveChunker.js
│   │   │
│   │   ├── embeddings/
│   │   │   ├── embeddingGenerator.js
│   │   │   └── vectorEncoder.js
│   │   │
│   │   ├── retrieval/
│   │   │   ├── retriever.js
│   │   │   ├── semanticSearch.js
│   │   │   └── reranker.js
│   │   │
│   │   ├── vectorstore/
│   │   │   ├── chromaStore.js
│   │   │   └── vectorManager.js
│   │   │
│   │   ├── prompts/
│   │   │   ├── summaryPrompt.js
│   │   │   ├── timelinePrompt.js
│   │   │   ├── citationPrompt.js
│   │   │   └── civicPrompt.js
│   │   │
│   │   └── ragPipeline.js
│   │
│   ├── uploads/
│   │   ├── documents/
│   │   ├── temp/
│   │   └── processed/
│   │
│   ├── vectorstore/
│   │   └── chromadb/
│   │
│   ├── logs/
│   │   ├── server.log
│   │   ├── uploads.log
│   │   └── errors.log
│   │
│   ├── utils/
│   │   ├── logger.js
│   │   ├── constants.js
│   │   ├── validators.js
│   │   ├── responseFormatter.js
│   │   └── seed.js
│   │
│   ├── scripts/
│   │   ├── startServer.sh
│   │   ├── ingestData.sh
│   │   └── deploy.sh
│   │
│   ├── tests/
│   │   ├── api.test.js
│   │   ├── rag.test.js
│   │   └── upload.test.js
│   │
│   ├── .env
│   ├── package.json
│   ├── package-lock.json
│   ├── requirements.txt
│   ├── README.md
│   └── server.js
│
│
├── docs/
│   ├── sample-documents/
│   ├── civic-datasets/
│   ├── scholarship-documents/
│   ├── budget-reports/
│   └── policy-documents/
│
│
├── screenshots/
│   ├── landing-page.png
│   ├── dashboard.png
│   ├── upload-page.png
│   ├── chat-interface.png
│   ├── citations-page.png
│   └── timeline-page.png
│
│
├── architecture/
│   ├── architecture-diagram.png
│   ├── workflow-diagram.png
│   ├── rag-flow-diagram.png
│   └── deployment-diagram.png
│
│
├── presentation/
│   ├── hackathon-ppt.pptx
│   ├── demo-script.md
│   └── project-summary.md
│
│
├── deployment/
│   ├── vercel.json
│   ├── render.yaml
│   ├── docker-compose.yml
│   └── nginx.conf
│
│
├── .gitignore
├── LICENSE
├── README.md
└── CONTRIBUTING.md
```

# Setup & Running

## Prerequisites

- Python 3.11+
- Node.js 18+
- NVIDIA NIM API Key (from build.nvidia.com)
- Git
- VS Code (recommended)

### Optional
- ChromaDB
- Tavily API Key (for live web search augmentation)
- Translation APIs
- Voice synthesis support

---

# Backend Setup

```bash
cd civiclens-ai/backend

# Install backend dependencies
npm install

# Install Python AI dependencies
pip install -r requirements.txt

# Create environment file
cp .env.example .env

# Add NVIDIA API key and configuration
NVIDIA_API_KEY=your_nvidia_api_key

# Start backend server
npm run dev
```

OR

```bash
python server.py
```

---

# RAG Pipeline Setup

```bash
# Ingest uploaded documents
python -m rag.ingestion.ingestDocuments

# Generate embeddings & vector indexing
python -m rag.embeddings.embeddingGenerator

# Start ChromaDB vector retrieval pipeline
python -m rag.ragPipeline
```

---

# Frontend Setup

```bash
cd civiclens-ai/frontend

# Install frontend dependencies
npm install

# Start frontend server
npm run dev
```

Frontend runs on:

```text
http://localhost:3000
```

---

# Vector Database Setup

ChromaDB stores:
- document embeddings
- semantic vectors
- citation metadata
- retrieval chunks

Default storage path:

```text
./vectorstore/chromadb
```

---

# Run Tests

```bash
# Backend tests
npm test

# RAG pipeline tests
python -m pytest tests/
```

---

# Environment Variables

| Variable | Required | Description |
|---|---|---|
| NVIDIA_API_KEY | Yes | NVIDIA NIM API key |
| NVIDIA_MODEL | Yes | NVIDIA Nemotron 3 Super model name |
| NVIDIA_BASE_URL | No | Default: https://integrate.api.nvidia.com/v1 |
| JWT_SECRET | Yes | JWT authentication secret |
| CHROMA_DB_PATH | No | ChromaDB vector storage path |
| UPLOADS_FOLDER | No | Uploaded documents directory |
| MAX_UPLOAD_SIZE | No | Maximum upload size limit |
| ENABLE_TRANSLATION | No | Enable multilingual responses |
| ENABLE_VOICE | No | Enable voice summary feature |
| LOG_LEVEL | No | Backend logging level |
| PORT | No | Backend server port |

---

# Evaluation Metrics

| Metric | Description |
|---|---|
| Response Accuracy | AI response correctness against source documents |
| Citation Coverage | Percentage of responses containing valid citations |
| Semantic Retrieval Accuracy | Relevance of retrieved document chunks |
| Deadline Detection Accuracy | Accuracy of extracted timelines & deadlines |
| Hallucination Reduction | Grounded response consistency through RAG |
| User Comprehension | Ease of understanding generated summaries |
| Actionability Score | Quality of extracted action items & alerts |
| Latency Performance | Response generation speed |
| Document Processing Accuracy | PDF/DOCX extraction quality |

---

# Future Improvements

- Multi-language civic intelligence support
- Voice-enabled accessibility assistant
- Live government portal ingestion
- Real-time civic notifications
- AI-powered policy comparison
- WhatsApp-based citizen assistant
- Mobile application support
- Smart recommendation engine
- Regional personalization
- Advanced analytics dashboard
- OCR support for scanned government documents
- AI-generated visual insights & charts
