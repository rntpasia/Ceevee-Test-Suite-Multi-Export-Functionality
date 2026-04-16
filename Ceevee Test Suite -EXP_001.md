# Test Suite: Multiple Export Format (EXP_001)

> **Project:** Ceevee
> 
> **Version:** 1.0
> 
> **Priority:** High
> 

---
### 1. Objective/Scope
This document contains a comprehensive test suite for Ceevee's multi-export functionality. Under this feature, users can customize their generated resumes using the provided options in the customization settings and export them to multiple formats, including PDF, DOCX, and Markdown.

---
### 2. Testing Scenario
1.  Verify multi-format export functionality
2.  Validate the effect of UI customization on Live Preview and exported files
3.  Verify tiered access of Pro+ vs. Free on watermark and export formats
4.  Validate consistency between the exported resume and cover letter

---
### 3. Test Cases

| ID | Description | Expected Result | Priority | 
| :--- | :--- | :--- | :---: |
| TC_EXP_001 | Export PDF on free tier  | Contains watermark, downloads successfully | High | 
| TC_EXP_002 | Export docx on Pro+ tier | Editable docx file downloads successfully and does not lose formatting | High | 
| TC_EXP_003 | Export markdown file | Downloaded file preserves header/title formats and bullet points | High |
| TC_EXP_004 | Change font from “Inter” to “Merriweather”  | Live preview instantly reflects the setting; Exported file matches the preview | Med | 
| TC_EXP_005 | Change Font Size from “Medium” to “Large” | Live preview instantly reflects the setting; Exported file matches the preview | Med | 
| TC_EXP_006 | Change template from “Classic” to “Minimal” | Live preview instantly reflects the setting; Exported file matches the preview; Green accents are absent; Line spacing must be dense | Med |
| TC_EXP_007 | Change template from “Minimal” to “Modern” | Live preview instantly reflects the setting; Exported file matches the preview; Blue accents are observed; structure must reflect contemporary design; line spacing must be less dense | Med |
| TC_EXP_008 | Attempt to export DOCX format on free tier | Action prohibited; Prompt must appear that this feature is available on Pro+ tier only | High | 
| TC_EXP_009 | Export Cover Letter | Downloads a PDF containing the cover letter; content must be aligned with the resume and the customization set by the user | High | 

---
### 4. Execution Checklist
- [ ] Download the resume in multiple formats (DOCX, PDF, Markdown)
- [ ] Verify presence of watermark on PDF on free tier
- [ ] Check whether Live Preview exhibits a delay when changing customization settings
- [ ] Ensure that exported files reflect the customization
- [ ] Verify whether the content of the separate cover letter matches the resume 
