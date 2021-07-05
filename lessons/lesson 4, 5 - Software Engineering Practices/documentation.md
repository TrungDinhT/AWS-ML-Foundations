# Code documentation
There are 3 levels of documentation:
- Inline comments
- Docstrings (module or function)
- Project document

## Inline comments
- Explain the below block of codes
- Avoid 
  - comments that just explain the below codes, because it's sign that those blocks can be refactored into functions
  - comments that are inconsistent with the below codes
- Comments are best to explain the story behind the codes (why it's implemented that way, hard-coded values, the goal of the codes that are out of the context of the codes themselves)

## Docstrings
- Types of documentation that appears at the top of function, method, class, module
- First expression, under format of string literals, after the signature of function, method, class, module 
- They can be accessed at runtime through attribute `__doc__`
- Docstrings have to be documented for each function, method, class, module, etc. -> good practice