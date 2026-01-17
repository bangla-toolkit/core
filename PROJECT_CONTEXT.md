# BNTK (Bangla Toolkit) / Byakoron - Project Context

## 1. Project Overview
**Title**: Byakaron: Bangla Grammar & Spell Checker
**Subtitle**: Design and Development of Bangla Grammar Correction System
**Type**: Undergraduate Thesis Project  
**Goal**: Develop a comprehensive Bengali spellchecker using modern NLP techniques (N-gram models, Rule-based correction) and a robust web application for users.

## 2. Technical Architecture
**Monorepo**: Managed using Bun workspaces.
**Stack**:
- **Runtime**: Bun
- **Language**: TypeScript
- **Database**: PostgreSQL (with PCA/Prisma)
- **Frontend**: Next.js (App Router)
- **ORM**: Prisma

### Directory Structure
- `apps/`: User-facing applications
  - `byakoron`: Main web interface (Next.js)
  - `training`: Model training scripts (implied)
- `packages/`: Shared libraries
  - `core`: Core NLP algorithms (Tokenizer, POS, NER, Stemming)
  - `db`: Database schema and connection logic (Prisma)
  - `dataset`: ETL pipelines for processing raw text data
- `reports/`: Thesis documentation and presentation material
- `docs/`: Project documentation (Docusaurus)

## 3. Component Details

### A. Core NLP (`packages/core`)
Implements fundamental NLP tasks for Bangla.
- **Tokenization**: 
  - Splits text into sentences and words. 
  - Regex-based cleanup (removes URLs, English chars, brackets) to isolate pure Bangla text.
  - See `packages/core/tokenization/src/sentence.ts`.
- **Other Modules**: NER, POS, Stemming, Transliteration (structure exists).

### B. Database & Data Model (`packages/db`)
Uses Prisma with PostgreSQL. Key tables (`packages/db/schemas/main.prisma`):
- **`sentences`**: Raw sentences from datasources (e.g., Wikipedia).
- **`words`**: Unique collection of Bangla words.
- **`word_pairs`**: Bigram model (prev_word, next_word) with `weight` and `occurance`. This is the backbone of the statistical spell/grammar checking.
- **`grammar_rules` & `rules`**: Explicit rule-based corrections (keyword -> replacement).
- **`pos_tag`**: Enum for Part-of-Speech tags (UD v2 standard).
- **`ner_tag`**: Enum for Named Entity Recognition tags.

### C. Dataset Pipeline (`packages/dataset`)
ETL process to populate the database.
- **Extract**: Downloads raw text (e.g., from Wikipedia dumps).
- **Transform**: Cleanses text, tokenizes, and generates n-grams (word pairs).
- **Load**: Efficiently inserts data into Postgres using `pg-copy-streams`.

### D. Application (`apps/byakoron`)
- **Framework**: Next.js 14+ (App Router).
- **Styling**: Tailwind CSS (inferred from standard Next.js setup/user preferences).
- **Purpose**: User interface for text input and displaying correction suggestions.

## 4. Research & Documentation
- **`RESEARCH.md`**: Explores NLP concepts (Tokenization, POS, NER, Lemmatization) relevant to the project.
- **`PAPER.md`**: Draft of the thesis paper including Introduction, Methodology, and Conclusion.
- **Presentation**: `reports/presentation-slide/Byakaron - Thesis Project Pre-defense .pdf`.

## 5. Current Status
- The core data pipeline is established.
- Database schema supports both statistical (N-gram) and rule-based corrections.
- Basic applications are set up.
- **Thesis report content generated** in `reports/Thesis_Project_Report`.
- 7 chapters written with proper IEEE citations and 8 integrated diagrams.

### Visual Assets (`reports/Thesis_Project_Report/Visuals/`)
| File | Description |
|------|-------------|
| `system_architecture.png` | Overall system architecture showing data flow |
| `er_diagram.png` | Entity-Relationship diagram of database schema |
| `er_diagram_detailed.png` | Detailed ER with word_pairs and rules tables |
| `spell_engine_flow.png` | Spell checker engine processing flow |
| `data_pipeline.png` | ETL pipeline from Wikipedia to database |
| `nlp_modules.png` | NLP processing modules diagram |
| `stemmer_pipeline.png` | Bangla stemmer morphological analysis |
| `data_sources.png` | List of data sources used |

## 6. Instructions for Thesis Report Generation
When generating the thesis report:
1.  **Methodology Chapter**: Describe the Hybrid approach (Statistical N-gram + Rule-based). Refer to `packages/db/schemas/main.prisma` for the data structure proof.
2.  **Implementation Chapter**: Detail the `dataset` ETL pipeline and `core` tokenization logic `packages/core/tokenization/src/sentence.ts` as key contributions.
3.  **Results**: Mention the web application `byakoron` as the practical output.

## 7. Additional Context from Presentation Slides
**Team Members (Green University of Bangladesh):**
- Nurul Huda (221902012)
- Jubaer Al Mamun (221902013)
- Md. Mursaline Parvez (221902363)
**Supervisor**: Dr. Muhammad Aminur Rahaman

**Project Status (as of Pre-defense):**
- Dataset: 100% Complete
- Engines: 50%
- Spell Checker: 60%
- Grammar Checker: 10%

**Budget Breakdown (Total: ৳3,60,000):**
- Developers: 1,50,000
- Computing (GPU/Cloud): 80,000
- Hosting & Infra: 40,000
- Mobile App Dev: 40,000
- Marketing: 30,000
- Misc: 20,000

**Key References:**
1. Wikimedia Dumps (bnwiki) - Primary data source.
2. OpenBangla - Existing open source tools.
3. Bhattacharyya et al. (2024) - VAIYAKARANA Benchmark.
4. Akter & Rahman (2023) - Transformer Models for Bangla Grammar.
5. Saha & Dey (2023) - Fine-tuned Language Models.
6. Islam & Kabir (2023) - BERT/T5 Models for correction.
