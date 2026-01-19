# Prompt Template: Spiritual Terms Translation Reference Guide

Use this prompt to generate a comprehensive spiritual terms reference guide for any language translation.

---

## Usage Instructions

1. Copy the prompt template below
2. Replace `{LANGUAGE_CODE}` with the target language code (e.g., ar, es, zh_CN, fa_IR)
3. Replace `{LANGUAGE_NAME}` with the full language name (e.g., Arabic, Spanish, Chinese, Persian)
4. Run the prompt with Claude Code

---

## PROMPT TEMPLATE

```
{LANGUAGE_CODE} = ar
{LANGUAGE_NAME} = Arabic

Analyze the PO file at `po_files/zume-{LANGUAGE_CODE}.po` and create a comprehensive spiritual terms translation reference guide.

## Task Overview

Extract and document how key spiritual and ministry terms are translated from English to {LANGUAGE_NAME} in the Zume training materials. This reference will be used to coach translators and maintain consistency in future translation work.

## Analysis Steps

1. **Read the PO file** at `/Users/chris/Documents/ZUME/zume-ai-building-blocks/translations/po_files/zume-{LANGUAGE_CODE}.po`
   - If the file is too large, use a Task agent with subagent_type="general-purpose" to analyze it

2. **Extract translations** for the following spiritual terms (search for English msgid and find corresponding msgstr):

   ### Core Deity Terms
   - Jesus
   - Christ
   - Messiah
   - God
   - Holy Spirit
   - Spirit (spiritual, spirituality)
   - Lord
   - Father (God the Father)

   ### Discipleship Terms
   - Disciple
   - Disciple-making / Discipleship
   - Follower (of Jesus)
   - Believer
   - Obey / Obedience
   - Follow / Following

   ### Church Terms
   - Church
   - Simple church
   - Congregation
   - Assembly
   - Body of Christ (if present)

   ### Gospel and Scripture Terms
   - Gospel
   - Good News
   - Bible
   - Scripture
   - Word (Word of God)

   ### Sacraments and Practices
   - Baptism / Baptize
   - Prayer / Pray
   - Communion / Lord's Supper
   - Worship
   - Testimony
   - Witness (verb and noun)

   ### Salvation Terms
   - Salvation
   - Save / Saved
   - Repent / Repentance
   - Faith
   - Believe
   - Grace
   - Sin
   - Forgiveness / Forgive

   ### Spiritual Qualities and Actions
   - Love (agape)
   - Blessing / Bless
   - Peace
   - Joy
   - Hope
   - Serve / Service
   - Sacrifice

   ### Kingdom Terms
   - Kingdom (Kingdom of God/Heaven)
   - Heaven
   - Eternal life

   ### Leadership and Ministry Terms
   - Leader / Leadership
   - Train / Training / Trainer / Trainee
   - Mentor / Mentoring
   - Coach / Coaching
   - Pastor / Shepherd
   - Elder
   - Apostle
   - Prophet
   - Teacher

   ### Multiplication Terms
   - Multiply / Multiplication
   - Reproduce / Reproduction
   - Growth / Grow
   - Harvest

   ### Additional Terms
   - Vision
   - Mission
   - Covenant
   - Resurrection
   - Generations (spiritual generations)
   - Network

3. **For each term found**, document:
   - The translation(s) used in {LANGUAGE_NAME}
   - Literal meaning if helpful (e.g., "Jemaah = congregation/assembly")
   - Multiple examples showing English → {LANGUAGE_NAME} in context
   - Any variations or contextual differences
   - Plural forms if different
   - Verb vs noun forms if applicable
   - Any cultural or religious notes about the terminology choice

4. **Identify translation patterns**:
   - Are there multiple valid translations for the same term?
   - Does the translation use religious terminology from another faith tradition?
   - Is the vocabulary formal/liturgical or informal/practical?
   - Are there any terms consistently avoided?
   - What cultural adaptation strategies are evident?

5. **List terms NOT found** in the translation (from the list above)

6. **Analyze the overall translation strategy**:
   - What audience does this translation seem to target?
   - What cultural or religious sensitivities are addressed?
   - Is there a preference for borrowed words vs native terms?
   - What theological or denominational stance is reflected?

## Output Format

Create a markdown file at `/Users/chris/Documents/ZUME/zume-ai-building-blocks/translations/{LANGUAGE_CODE}-spiritual-terms-reference.md` with this structure:

```markdown
# {LANGUAGE_NAME} Translation Reference Guide ({LANGUAGE_CODE})

**Source File:** `po_files/zume-{LANGUAGE_CODE}.po`
**Purpose:** Reference guide for maintaining consistent spiritual terminology in {LANGUAGE_NAME} translations
**Date Analyzed:** [TODAY'S DATE]

---

## Overview

[Brief description of the translation approach and key characteristics]

---

## Core Deity Terms

### Jesus
- **{LANGUAGE_NAME}:** [translation(s)]
- **Notes:** [cultural/linguistic notes]
- **Examples:**
  - "[English]" → "[{LANGUAGE_NAME}]"
  - [3-5 examples showing usage in context]

### [Continue for all deity terms...]

---

## Discipleship Terms

[Same format as above]

---

## Church Terms

[Same format as above]

---

## Gospel and Scripture Terms

[Same format as above]

---

## Sacraments and Practices

[Same format as above]

---

## Spiritual Qualities and Actions

[Same format as above]

---

## Kingdom Terms

[Same format as above]

---

## Leadership and Ministry Terms

[Same format as above]

---

## Multiplication Terms

[Same format as above]

---

## Key Translation Principles

### 1. [Principle Name]
[Description of translation approach]

### 2. [Principle Name]
[Description]

[Continue for 4-6 key principles...]

---

## Terms NOT Present in Current Translation

The following terms were **not found** in the PO file and should be avoided or defined if needed:

- [List terms not found]
- [Include what they might be in {LANGUAGE_NAME} if relevant]

---

## Translation Strategy Summary

This {LANGUAGE_NAME} translation appears designed to [describe target audience and approach]:

1. [Key strategy point 1]
2. [Key strategy point 2]
3. [Key strategy point 3]
[etc.]

When coaching further translation work, maintain this strategy to ensure consistency with the existing translation.

---

## Recommended Usage Guidelines

### DO:
- [Specific guidance for consistent translation]
- [3-7 concrete recommendations]

### DON'T:
- [What to avoid]
- [3-7 concrete warnings]

---

**Last Updated:** [TODAY'S DATE]
**Maintained by:** Translation Coaching Team
**Reference File:** `po_files/zume-{LANGUAGE_CODE}.po`
```

## Quality Requirements

- Provide **at least 3-5 examples** for each major term
- Include **literal translations** when they provide insight
- Note **all variations** found for the same English term
- Document **patterns** not just individual translations
- Identify the **translation philosophy** (literal, dynamic, contextualized, etc.)
- Explain **cultural adaptations** that are evident
- Be specific about **religious terminology choices** (e.g., does it use Islamic, Christian, neutral, or borrowed terms?)

## Deliverable

Create a comprehensive markdown reference document that a translation coach can use to:
1. Understand the existing translation choices
2. Maintain consistency in future translations
3. Train new translators on terminology standards
4. Identify the cultural and theological positioning of the translation
```

---

## Example Usage

### For Arabic (ar):
```
Analyze the PO file at `po_files/zume-ar.po` and create a comprehensive spiritual terms translation reference guide.

[Use full prompt template above, replacing {LANGUAGE_CODE} with "ar" and {LANGUAGE_NAME} with "Arabic"]
```

### For Spanish (es):
```
Analyze the PO file at `po_files/zume-es.po` and create a comprehensive spiritual terms translation reference guide.

[Use full prompt template above, replacing {LANGUAGE_CODE} with "es" and {LANGUAGE_NAME} with "Spanish"]
```

### For Persian (fa_IR):
```
Analyze the PO file at `po_files/zume-fa_IR.po` and create a comprehensive spiritual terms translation reference guide.

[Use full prompt template above, replacing {LANGUAGE_CODE} with "fa_IR" and {LANGUAGE_NAME} with "Persian"]
```

---

## Quick Reference: Available Language Codes

Based on the po_files directory, available language codes include:
- am (Amharic)
- ar (Arabic), ar_JO (Jordanian Arabic), ar_MA (Moroccan Arabic), ar_TN (Tunisian Arabic)
- az (Azerbaijani)
- bg_BG (Bulgarian)
- bho (Bhojpuri)
- bn_IN (Bengali)
- bs_BA (Bosnian)
- ckb (Central Kurdish)
- de_DE (German)
- es (Spanish)
- fa_IR (Persian/Farsi)
- fo (Faroese)
- fr_FR (French)
- gu (Gujarati)
- ha_NG (Hausa)
- hi_IN (Hindi)
- hr (Croatian)
- hu (Hungarian)
- hy (Armenian)
- id_ID (Indonesian)
- it_IT (Italian)
- ja (Japanese)
- kn (Kannada)
- ko_KR (Korean)
- ku (Kurdish)
- ky (Kyrgyz)
- lo (Lao)
- lv (Latvian)
- mai (Maithili)
- ml_IN (Malayalam)
- mn (Mongolian)
- mr (Marathi)
- ms (Malay)
- my (Burmese)
- ne_NP (Nepali)
- om (Oromo)
- or (Odia)
- pa_IN (Punjabi - India)
- pa_PK (Punjabi - Pakistan)
- pl_PL (Polish)
- pt_PT (Portuguese)
- ro_RO (Romanian)
- ru_RU (Russian)
- si (Sinhala)
- sl_SI (Slovenian)
- so (Somali)
- swa (Swahili)
- ta_IN (Tamil)
- te (Telugu)
- th (Thai)
- tl (Tagalog)
- tr_TR (Turkish)
- uk (Ukrainian)
- ur (Urdu)
- vi (Vietnamese)
- yo (Yoruba)
- zh_CN (Chinese Simplified)
- zh_TW (Chinese Traditional)
- zh_Hant_HK (Chinese Traditional - Hong Kong)

---

## Notes

- The Task tool with subagent_type="general-purpose" is recommended for large PO files (>256KB)
- Some languages may not have translations for all terms - this is valuable to document
- Cultural and religious context is crucial - note any terminology that bridges faith traditions
- The quality of analysis depends on finding multiple contextual examples, not just single instances
