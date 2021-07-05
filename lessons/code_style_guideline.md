# Python code style guideline
This is a summary of important points based on the [PEP8 guideline](https://www.python.org/dev/peps/pep-0008/?#code-lay-out). 

## Indentation
- 4 spaces
  - python 3, not mixed spaces and tabs
  - python 2, can be mixed
- Indentation should help to distinguish the header (function signature, if conditions, etc.) and the body
  - if the parameters in multiple lines -> must have same level of indent
  - if the first parameter is on a new line ->
    - at function definition: 2 extra indents compared to the function name (so that they are distinguishable with the function body where there is only 1 extra indent)
    - at function reference: 1 extra indent is enough

## Docstrings
- Conventionally, we should use `"""` to start and end docstrings
- Structure:
  - First line -> brief description
  - Blank line
  - Each paragraph describes a property of the documented entit. 
    - For examples: a paragraph for `Parameters` (each parameter with its type and description on each line), a paragraph for `Returns` (each return with its type and description on each line)
