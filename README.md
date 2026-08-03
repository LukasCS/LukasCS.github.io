# Lukas Brkovic Leighton — Computer Science ePortfolio

BS Computer Science, Southern New Hampshire University. This portfolio showcases my capstone work: a structured code review and three categories of enhancements to a full stack application.

## Code Review

As the first artifact of this ePortfolio, I performed a structured code review of Travlr Getaways, the full stack MEAN application I built in CS 465. The review walks through the existing code in three categories — software design and engineering, algorithms and data structures, and databases — analyzing its functionality and weaknesses and laying out the enhancement plan the rest of this portfolio executes.

- 🎥 [Watch the code review video](https://youtu.be/vk7CnHw5FRs)

## Enhancement One: Software Design and Engineering

For this enhancement, I migrated the Travlr Getaways administrative single-page application from Angular to React 18 with strict TypeScript and refactored the Express backend around centralized error-handling middleware. The work eliminated roughly 240 lines of duplicated form code through a shared metadata-driven component, moved the edit workflow from hidden localStorage state to URL route parameters, closed a stored XSS vector and an unauthenticated DELETE route, and is verified by a Jest and React Testing Library suite. The narrative explains the artifact selection, the architectural mapping from each Angular construct to its React equivalent, and the lessons learned.

- 📄 [Read the narrative](CS499_Milestone_Two_Narrative.docx)
- 💻 [Download the code (original and enhanced)](CS499_Milestone_Two_Enhancement_One.zip) — the enhanced React application is in `enhanced_code/travlr/app_react/`
- 
## Enhancement Two: Algorithms and Data Structures

For this enhancement, I added an algorithmic search and recommendation layer to the Travlr Getaways application. The work includes a stable merge sort implemented from scratch with a tested stability guarantee, field-weighted relevance search over tokenized queries with no user-derived regular expressions, cursor-based pagination that resumes deterministically even as the underlying data changes, and a top-k recommendation engine that pairs a hash-map index with a bounded min-heap for O(n log k) selection, scoring similarity with inverse-document-frequency weighting so destination clusters emerge from vocabulary alone. The trip catalog was expanded to twenty-seven trips across four destination categories to make these behaviors observable, and the work is verified by thirty-six backend Jest tests, including integration tests that run the full Express and MongoDB pipeline against an in-memory database. The narrative details the design trade-offs and complexity analyses behind each choice.

- 📄 [Read the narrative](CS499_Milestone_Three_Narrative.docx)
- 💻 [Download the code (original and enhanced)](CS499_Milestone_Three_Enhancement_Two.zip) — the algorithm modules are in `enhanced_code/travlr/app_api/algorithms/`
