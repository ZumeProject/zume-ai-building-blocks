# Campaign Build Flow


## Product/Service Document (LLM/Human Editor)
1. Identify Product/Service
1. Load context and create draft of overview document.
1. Create an expanded overview document and create "overview.md". (LLM)

**Prompts**



```
Create an expanded overview of the following concept: [ADD_CONCEPT]
Use the attached resources to understand the concept.
```
_Attach tone-and-voice.md, training-concepts.md, Zume-Training-10-Session.pdf, and appropriate script (/content/scripts/)_

```
Verify that all quoted scripture is contextually accurate. List any quotations of concern, and prompt for which changes to make. After changes or if there are no changes, output a new version of the content.
```
```
Readability & Clarity Scoring
Compute the Flesch‑Kincaid Grade Level and readability score for this text.
```
```
Tone & Voice Alignment: Rate how well this passage matches Zúme’s brand voice: knowledgeable, motivational, approachable. Suggest edits to improve alignment.
```
```
Structure & Flow Check: Identify any logical jumps, redundant sentences, or missing transitions in the step‑by‑step instructions.
```


**Tips**
- Include tone-and-voice.md, training-concepts.md, Zume-Training-10-Session.pdf, and appropriate script (/content/scripts/)

**Notes**

## Keyword Creation Process

1. Create 500 potential keywords for this core concept with LLM.(LLM)
1. Use keyword discovery tool in batches of 10 to find search words with traffic.

1. Use the Get Search Volume Forecast tool in the Keyword Planner and Google Ads by dumping in all 500 keywords. (Google Web-UI)
1. Delete every search term that does not have any search volume. (If the useful words are 10% or 90%, you can use the keyword planner to delete them. Otherwise, exporting to CSV and extracting the useful terms in a spreadsheet is ultimately easier than the keyword planner.) (Google Web-UI)
1. Take the highest performing of these keywords and add them to the keyword discovery tool.
1. Copy all of these searched keywords into the master keyword list.
1. Rinse and repeat 2-6 with variations.
1. Create a keywords file (2-keywords.md)


**Prompts**
```
Create 50 search terms for expanded overview content.
Do not include punctuation, hyphenation, or parenthesis. Do not number the list. Make sure all variations are less than 4 words.
Separate list into batches of 10.
```

```
Create a new list from this list with slight rephrasings, plurals, and alternate spellings of the original list. Do not create new concepts or search terms, just rewrite original list with variations.
```

**Tips**
- It's worth having AI take the working list and write a new variation list of rephrases, plurals, and spellings phrases for the keywords that are working.


**Notes**
- Keyword-level Forcasts through the "Get Search Volumn Forcast Tool" were limited to the Web-UI only June 1, 2023. No API access.

## Keyword Grouping and Ad Creation
1. Have the LLM write 60 headlines and 20 descriptions from each of the keywords
1. Use an evaluator LLM agent to weight the headlines and descriptions
   - Test against keyword alignment
   - Test against "Google Religious Belief in Advertising Policy" (md file)
   - Test against "Best Google Ad Headline Principles" (md file)
1. Rewrite and reduce to 15 headlines and 4 descriptions.
1. Create a markdown file. (3-google-ad.md)

**Prompts**
```

```

```

```

**Tips**


**Notes**


## Landing Page Creation
1. Create a trackable CTA link to use. Example: https://pages.zume.training/{lang_code}/{html_page}
1. Combine the Keywords, the Advertisement, and the Product/Service document to create a 5 landing page JSON file content that promotes the product/service with a trackable link.
1. Use the LLM to judge and rank the different JSON pages according to clarity, persuasion, and conversion principles.
1. Identify the best JSON page.
1. Generate HTML page with winner. (4-landing-page.html)

**Prompts**
```

```

```

```

**Tips**


**Notes**

