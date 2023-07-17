This file contains the writing style and other guidelines for content developers and maintainers. 


# Markdown Style Guide
Refer to the [best practices](https://www.markdownguide.org/basic-syntax/) for writing standard markdown content. In addition, follow the guidelines outlined below.

## Headings
- Use heading elements to provide a hierarchical structure on a web page. Do not use headings for formatting purposes.
- Do not use any H1 headings. Page titles are automatically used as H1 headings in the new classroom design.

  ```
  ## H2 Prerequisites
  ## H2 Getting Started 
  ### H3 Instructions 
  ### H3 Results
  ### H3 Validate
  ## H2 Summary
  ```

### Important points about headings
- The top-level heading allowed in Mocha is H2. The H1 heading for the page is automatically generated in the classsroom from the page title. **Do not duplicate the page title in the top text atom**. 
- Maintain a heading hierarchy by using headings in order.  **Do not skip levels**.
- In most cases you will only need to use H2 and H3 headings, but if necessary H4 headings may be used.

To learn more, see [accessible heading structure
](https://www.a11yproject.com/posts/how-to-accessible-heading-structure/) for more details. 

## Capitalization
- Capitalize the first word and all proper nouns in your writing. 
- Avoid using *-ing* words in headings. Use action verbs instead. For example, use *Create a Manifest* (✅) instead of the *Creating a Manifest* (❌) heading. 
- For H2 headings, use the [Title case](https://en.wikipedia.org/wiki/Title_case#Chicago_Manual_of_Style). See an example below 
```bash
## Authenticate with OAuth
```
Use uppercase for:
 - Major words (nouns, pronouns, verbs, adjectives, and adverbs)
 - The first word in a title,

Use lowercase for:
  - Conjunctions:  *and*, *but*, *for*, *or*, and *nor*.
  - Articles:  *the*, *a*, and *an*.
  - Prepositions: *beneath*, *beside*, *between*, *from*, *inside*, *near*,  *off*, *through*, *toward*, *under*, *within*, etc.
  - Other small words like *to* and *as*.

- For all headings H3-H4 , use the [Sentence case](https://en.wikipedia.org/wiki/Letter_case#Sentence_case), and avoid using *-ing* words. 
- For Acronyms, use Title case while defining them in the first occurrence.

For assistance, you can use [Capitalize My Title - Chicago](https://capitalizemytitle.com/style/Chicago/)

## General Writing Tips
- Use [Active voice](https://www.grammarly.com/blog/active-vs-passive-voice/). In exceptional cases, you can use Passive voice, where it is impossible to use the Active voice. 
- For exercises and tutorials, clearly state the assumptions and prerequisites at the beginning of the page. 
- Inclusive content is important! Use gender-neutral pronouns and diverse names, ages, and locations in examples and scenarios. This list of [example names](https://developers.google.com/style/examples#example-person-names) is a good place to start. 
- Spell out the single digit numbers (zero to nine), and use numerals for numbers 10 and above. 

## Other Best Practices
- **[Required]** Provide descriptive alt text for all images.  Captions are optional and, if used, should not duplicate the alt text.
- Use simple English and avoid jargon. This makes it easier for all learners to understand the content. 
- Do not refer to the "previous" or the "following" lesson. Each lesson should be considered an independent and complete unit of content. 
- Use **bold** for file and folder names and to introduce new terms. 
- Use markdown tables to present tabular data. Do not use images of text in place of tables because those are not accessible to visually impaired learners.
- Group long instructions into several H3 headings. 
- Give credit to the author for any content (text, code, images, or media) you use in your article. Do not copy-paste content from external sources; refer to the external content just like research papers do. 
- **Do not point learners to any University website as an external resource**. 

## What to Avoid
- **Do use custom HTML in the text atoms**. It may render accurately in the Mocha interface, but custom HTML is stripped out when the content is delivered to the learner's classroom.  
- Do not special Markdown characters like `-` , `+` , `*` , `_` by themselves or at the beginning of a line. Instead, you can make use of [html entities](https://www.freeformatter.com/html-entities.html). For example, you can use `&#38;` in the place of an `&` character. 

> For items not covered in the current style guide, refer to the [Google developer documentation style guide](https://developers.google.com/style) and [Language specific style guide](https://google.github.io/styleguide/).


# Caution
Most importantly, **do not plagiarize**. Udacity checks for plagiarism before publishing any content. 

# Submit Inputs to Udacity
Udacity uses markdown for its content management platform. Therefore, use
- Github for submitting markdown files and code files.
- [Github gists](https://gist.github.com/) for submitting a code snippet.
- Google docs and spreadsheets for anything that cannot fit into Github or Gists.
- Do not host any artifact in a personal repository/account/workspace. Instead, ask the Udacity staff to host the artifacts in the Udacity repositories/Google drive/any other Udacity-owned account. 
