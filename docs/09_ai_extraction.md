# 09_ai_extraction_public.md
**Corruptibility Index (CI) – Public Explanation of AI-Assisted Data Processing**  
**High-Level, Non-Technical Summary**

---

## 1. Purpose of This Document

This document explains, at a safe and conceptual level, **how AI is used inside the Corruptibility Index (CI)**.

It clarifies:

- what AI does  
- what AI does *not* do  
- how AI improves efficiency  
- how CI protects against misuse or inappropriate influence  

This overview contains **no proprietary models, rules, schemas, or logic** from the private CI-Core system.

---

## 2. Why CI Uses AI

Public information comes in many forms:

- news articles  
- public disclosures  
- government documents  
- regulatory filings  
- investigative reports  
- long-form public statements  

AI helps CI handle this **high volume** of text by performing **clerical extraction tasks**, such as:

- identifying dates  
- identifying named entities  
- standardizing terminology  
- locating relevant sections  
- organizing information for human-review and scoring

AI **does not** interpret, weigh, or score the data.

It simply helps prepare publicly available information for structured analysis.

---

## 3. What AI *Does* in the CI System (Public-Friendly List)

AI performs strictly limited, well-defined functions:

### **1. Extraction**
Pulls key factual elements from public documents (names, dates, events, etc.).

### **2. Classification**
Organizes information into broad conceptual categories.

### **3. Summarization**
Creates concise summaries of long public documents to help with human understanding.

### **4. Standardization**
Normalizes data formats so different documents can be compared.

### **5. Validation Support**
Flags inconsistencies, missing fields, or unclear portions of documents.

### **6. Provenance Tagging**
Ensures extracted information is linked back to a verifiable public source.

These actions make the CI pipeline more efficient and more consistent.

---

## 4. What AI *Does Not* Do (Very Important)

To maintain fairness, transparency, and defensibility:

### ❌ **AI does NOT assign scores.**  
CI’s scoring logic is entirely rule-based, deterministic, and private.

### ❌ **AI does NOT determine weights, formulas, or thresholds.**  
These are defined by the CI-Core architecture, not by model output.

### ❌ **AI does NOT interpret behavior, intent, or meaning.**  
It performs clerical tasks only.

### ❌ **AI does NOT replace public records with guesses.**  
Unknown values remain unknown.

### ❌ **AI does NOT influence the final CI score.**  
It only prepares input data in structured form.

CI’s design ensures AI cannot introduce bias or manipulation into scoring.

---

## 5. Human Oversight

Even though AI assists with clerical work, the CI process includes:

- human review  
- consistency checks  
- internal audit trails  
- strict validation requirements  

No extracted information is used unless it meets quality and verification standards.

---

## 6. Transparency and Accountability

The CI team is committed to:

- clearly explaining how AI is used  
- restricting AI to non-interpretive tasks  
- ensuring no AI model has scoring authority  
- maintaining traceability for all AI-assisted extractions  
- preventing AI-generated speculation from entering the risk model  

This approach aligns with best practices in:

- compliance analytics  
- financial risk modeling  
- journalistic analysis tools  
- government transparency platforms  

---

## 7. Why CI Does Not Publish Its Internal AI Logic

Publishing detailed AI prompts, schema definitions, or extraction rules would:

- expose proprietary intellectual property  
- allow manipulation of the scoring system  
- enable adversarial optimization (gaming)  
- risk source-dependence vulnerabilities  
- compromise the defensibility of CI outputs  

The public receives conceptual clarity without operational detail.

---

## 8. Summary for External Audiences

- AI helps CI work efficiently with large volumes of public data.  
- AI is used only for **clerical extraction and organization**, never scoring.  
- All interpretive, numerical, and risk-evaluative components are **rule-based and private**.  
- The CI architecture includes strong safeguards to prevent misuse of AI.  
- Human oversight remains central to the process.  

This ensures CI remains:

- responsible  
- fair  
- transparent in purpose  
- protected from manipulation  

---

## 9. Disclaimer

This document intentionally omits all:

- AI prompt structures  
- scoring interactions  
- extraction thresholds  
- model parameters  
- validation rules  
- schema details  
- confidence relationships  
- computational logic  

All such elements are confidential and appear only in the private CI-Core specification.

