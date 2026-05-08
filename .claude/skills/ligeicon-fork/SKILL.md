```markdown
# ligeicon-fork Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides a comprehensive guide to contributing to the `ligeicon-fork` repository, a Python-based project focused on managing icon assets and rule lists. It covers coding conventions, step-by-step workflows for adding icons and updating rule lists, and best practices for maintaining consistency across the codebase.

## Coding Conventions

- **File Naming:**  
  Use camelCase for file names.  
  _Example:_  
  ```
  ligeEmbyIcon.json
  proxylist.list
  ```

- **Import Style:**  
  Use relative imports within Python files.  
  _Example:_  
  ```python
  from .utils import getIconMetadata
  ```

- **Export Style:**  
  Use named exports (explicitly define what is exported from a module).  
  _Example:_  
  ```python
  def getIconMetadata(...):
      ...

  __all__ = ['getIconMetadata']
  ```

## Workflows

### Add Icon and Auto Update Metadata
**Trigger:** When you want to add a new icon (e.g., for emby, ProxySoft, CNSoft, jichang)  
**Command:** `/add-icon`

1. Add one or more PNG files to the appropriate subdirectory under `icon/` (e.g., `icon/emby/`, `icon/04ProxySoft/`).
2. Commit the new files with a message like:
   ```
   Add files via upload
   ```
3. Trigger the auto-update process (this may be automated or require running a script) to update `README.md` and relevant JSON metadata files (e.g., `lige-emby-icon.json`, `ligeicon.json`).
4. Commit the updated metadata files with a message like:
   ```
   Auto update [skip ci]
   ```
5. Push your changes to the repository.

_Example directory structure after adding an icon:_
```
icon/
  emby/
    newIcon.png
README.md
lige-emby-icon.json
ligeicon.json
```

### Update Rule List
**Trigger:** When you need to update network/proxy or OpenAI related rules  
**Command:** `/update-rule`

1. Edit the relevant list file in the `rule/` directory (e.g., `proxylist.list`, `openai.list`).
2. Commit your changes with a descriptive message, such as:
   ```
   Update proxylist.list
   ```
   or
   ```
   Update openai.list
   ```
3. Push your changes to the repository.

_Example:_
```
rule/
  proxylist.list
  openai.list
```

## Testing Patterns

- **Framework:** Unknown (not explicitly detected)
- **File Pattern:** Test files follow the pattern `*.test.*`
  - _Example:_ `iconManager.test.py`
- **Best Practice:** Place your tests in files matching this pattern to ensure consistency.

## Commands

| Command      | Purpose                                         |
|--------------|-------------------------------------------------|
| /add-icon    | Add new icon(s) and auto-update metadata files  |
| /update-rule | Update proxy or OpenAI rule list files          |
```
