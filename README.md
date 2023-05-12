This file contains the writing style and other guidelines for content developers and maintainers. 


# Markdown Style Guide
Refer to the [best practices](https://www.markdownguide.org/basic-syntax/) for writing standard markdown content. In addition, follow the guidelines specific to Udacity's content development tool outlined below.

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
- Do not duplicate the page title in the top text atom. 
- Maintain a heading hierarchy by using headings in order. Prefer to use headings through H3, but you can add H4 and H5 headings if *necessary*. If you want to learn more, refer to [accessible heading structure
](https://www.a11yproject.com/posts/how-to-accessible-heading-structure/) for more details. 


## Capitalization
- Capitalize the first word and all proper nouns in your writing. 
- Avoid using *-ing* words in headings. Prefer to use action verbs. For example, use *Create a Manifest* instead of the *Creat***ing*** a Manifest*  heading. 
- For H2 heading, use the [Title case](https://en.wikipedia.org/wiki/Title_case#Chicago_Manual_of_Style). See an example below 
```bash
## Authenticate with OAuth
```
	- Always capitalize "major" words (nouns, pronouns, verbs, adjectives, adverbs, and some conjunctions).
	- Lowercase the conjunctions *and, but, for, or*, and *nor*.
	- Lowercase the articles the, *a*, and *an*.
	- Lowercase prepositions.
	- Lowercase the words *to* and *as*.

- For all headings except H1 and H2, use the [Sentence case](https://en.wikipedia.org/wiki/Letter_case#Sentence_case), and avoid using *-ing* words. 
- For Acronyms, use the Title case while defining them in the first occurrence.


## General Writing
- Use [Active voice](https://www.grammarly.com/blog/active-vs-passive-voice/). In exceptional cases, you can use Passive voice, where it is impossible to use the Active voice. 
- For exercises and tutorials, clearly state the assumptions and prerequisites at the beginning of the page. 
- Use gender-neutral pronouns and diverse names, ages, and locations in examples. Here are [some common names](https://developers.google.com/style/examples#example-person-names) you can use in your examples. Udacity is sensitive to diversity and inclusion. 
- Spell out the single digit numbers (zero to nine), and use numerals for numbers 10 and above. 


## Other Best Practices
- Provide a descriptive caption for all media images. 
- Use simple English, making it easier for all learners to understand the content. 
- Do not point learners to the "previous" or the "following" lesson. Each lesson must be an independent and complete unit of content. 
- Use **bold** for file and folder names. 
- Use *italics* to emphasize any word. 
- Use markdown tables to present fields and values in a workflow. 
- Group long instructions into several H3 headings. 
- Give credit to the author for any content (text, code, images, or media) you use in your article. Do not copy-paste content from external sources; refer to the external content just like research papers do. 
- **Do not point learners to any University website as an external resource**. 


## What to Avoid
- Avoid writing custom html within your markdown. If you must, use an [html validation checker](https://validator.w3.org/nu/#textarea).
- Avoid using special markdown characters like `-` , `+` , `*` , `_` by themselves or at the beginning of a line. Instead, you can make use of [html entities](https://www.freeformatter.com/html-entities.html). For example, you can use `&#38;` in the place of an `&` character. 
- 

> For items not covered in the current style guide, refer to the [Google developer documentation style guide](https://developers.google.com/style) and [Language specific style guide](https://google.github.io/styleguide/).


# Caution
Most importantly, **do not plagiarize**. Udacity checks for plagiarism before publishing any content. 

# Submit Inputs to Udacity
Udacity uses markdown for its content management platform. Therefore, use
- Github for submitting markdown files and code files.
- [Github gists](https://gist.github.com/) for submitting a code snippet.
- Google docs and spreadsheets for anything that cannot fit into Github or Gists.
- Do not host any artifact in a personal repository/account/workspace. Instead, ask the Udacity staff to host the artifacts in the Udacity's repositories/Google drive/any other Udacity owned account. 
