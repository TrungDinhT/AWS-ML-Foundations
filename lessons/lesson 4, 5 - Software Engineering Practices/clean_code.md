# Clean code practices
- Clean codes:
  - simple
  - concise
  - readable
- Consistent should be a priority
  - **However**, if breaking consistency is better for cleaner codes -> it's the right time to do

## Naming convention
- Python function, variable names should be
  - concise
  - easy to differentiate
  - verbose, but not too long
- For a list of something: prefer `<name>_list` over `<name>s`.
  - **However**, this bases on the fact that everything in Python is a list. In C++, it's to be reconsidered so as not to be mistaken with something using `std::list`

## Modularization
- **DRY**: Do not Repeat Yoursel
- **Abstract out the logic to smaller entities** (functions, classes, etc.) can help us to focus on the main logic -> code more readable
- **Single responsibility**: each entity (function, class, etc.) only does one thing
- **Do not break the logic into too small parts** -> not worth for a function, sometimes make the codes less readable, because we have to look for where the functions are defined
- **Minimize the number of parameters**