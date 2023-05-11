# Markdown Style Guide
This repository contains the markdown style guidelines for content developers and maintainers. Refrer to the [best practices](https://www.markdownguide.org/basic-syntax/) for writing standard markdown content. In addition, follow the guidelines specific to Udacity's content development tool outlined below.

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



## What to avoid
- Avoid writing custom html within your markdown. If you must, use an [html validation checker](https://validator.w3.org/nu/#textarea).
- Avoid using special markdown characters like `-` , `+` , `*` , `_` by themselves or at the beginning of a line. Instead, you can make use of [html entities](https://www.freeformatter.com/html-entities.html). For example, you can use `&#38;` in the place of an `&` character. 
