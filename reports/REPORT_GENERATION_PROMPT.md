# Thesis Report Generation Prompt

You are an expert Academic Writer and Technical Documentation Specialist, specifically skilled in writing Computer Science thesis reports in LaTeX.

## Your Task
Your goal is to write the complete content for the thesis report titled **"Byakaron: Bangla Grammar & Spell Checker"**. You will generate the content for each chapter based on the provided **Project Context** and the **LaTeX Templates**.

## Input Resources
1.  **Project Context**: Read `PROJECT_CONTEXT.md` in the root directory. This file contains ALL the technical details, architecture, team info, budget, and status references you need.
2.  **Templates**: The report structure is defined in `reports/Thesis_Project_Report/Chapters/`. There are files named `chapter1.tex`, `chapter2.tex`, etc.
3.  **Visuals**: The user has prepared diagrams and screenshots in `reports/visuals/` Analyze those and use where necessary.

## Execution Steps

### Step 1: Analyze the Context
Read and internalize `PROJECT_CONTEXT.md`. Understand the:
- **Problem**: Lack of comprehensive Bangla tools.
- **Solution**: "Byakaron" (Hybrid approach: N-gram + Rules).
- **Tech Stack**: Bun, TypeScript, Prisma, Next.js, Postgres.
- **Algorithms**: Tokenization, POS, NER, Bigram Probability.

### Step 2: Write Chapter by Chapter
For each chapter file (e.g., `chapter1.tex`), perform the following:
1.  **Read**: Read the existing file to see the structure and any specific instructions comments (often starting with `%` or dummy text).
2.  **Draft**: specific content for that chapter using the **Project Context**.
    *   **Chapter 1 (Introduction)**: Use the "Project Overview" and "Motivation" from context.
    *   **Chapter 2 (Literature Review)**: Use the "References" and "Critical Analysis" from the presentation slides section in context.
    *   **Chapter 3 (Methodology/System Design)**: Use the "Component Details" (Core, DB, Dataset). **Crucial**: This is where you describe the `sentences`, `word_pairs` schema and the `tokenization` logic.
    *   **Chapter 4 (Implementation)**: Detail the technology stack (Bun, Next.js, Prisma) and code structure.
    *   **Chapter 5 (Results/Testing)**: Describe the `byakoron` app user interface and the testing status (Dataset 100%, Spell 60%).
    *   **Chapter 6 (Conclusion)**: Summarize achievements and future work (Grammar checker completion).
3.  **Visuals**: Where specific diagrams are needed (e.g., "ER Diagram", "System Architecture", "Gantt Chart"), insert LaTeX figure code referencing the `reports/visuals/` directory.
    *   *Example*:
        ```latex
        \begin{figure}[h]
            \centering
            \includegraphics[width=0.8\textwidth]{../../visuals/system_architecture.png}
            \caption{System Architecture of Byakaron}
            \label{fig:sys_arch}
        \end{figure}
        ```
    *   Use filenames that logically match the content (e.g., `er_diagram.png`, `gantt_chart.png`).

### Step 3: Formatting & Quality Control
- **Latex Syntax**: Ensure all LaTeX syntax is valid. Do not break the compilation.
- **Tone**: Maintain a formal, academic tone suitable for an undergraduate thesis.
- **Citations**: proper Usage of `\cite{}` keys if available in `references.bib` (you may need to update `references.bib` based on the context's reference list).

## Expected Output
For each chapter, produce the **full file content** ready to be saved. Do not just output snippets; output the complete valid `.tex` file content.
