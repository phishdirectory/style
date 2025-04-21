# Code Style Guide

This document defines the code formatting standards for our organization. It applies to all repositories unless otherwise specified. Consistent formatting improves readability, reduces cognitive load, and makes collaboration easier.

---

## 🔧 General Formatting Rules

- **Indentation**: 4 spaces (no tabs)  
- **Line Length**: 100 characters max  
- **Naming Convention**: `camelCase` for variables, functions, and methods  
- **Braces**: K&R style (opening brace on the same line)  
- **Trailing Commas**: Yes, where supported  
- **Quotes**: Prefer double quotes (`"`) unless single quotes are required  

---

## 🟨 JavaScript / TypeScript

- Use [Prettier](https://prettier.io) for formatting  
- Use [ESLint](https://eslint.org) for linting  
- Enforce `camelCase` for variables and functions  
- Use `const` and `let` (avoid `var`)  
- Prefer arrow functions for anonymous functions  
- Use semicolons  

**Example:**

```js
function getUserName(userId) {
    if (!userId) {
        return null;
    }
    return userService.getName(userId);
}
```

---

## 🐍 Python

- Use [Black](https://black.readthedocs.io) for formatting  
- Use [Flake8](https://flake8.pycqa.org) or [pylint](https://pylint.org) for linting  
- 4-space indentation  
- `camelCase` for variables and functions (note: this deviates from PEP 8)  
- Use docstrings for all public functions and classes  

**Example:**

```python
def getUserName(userId):
    if not userId:
        return None
    return user_service.get_name(userId)
```

---

## 💎 Ruby

- Use [RuboCop](https://rubocop.org) for formatting and linting  
- 4-space indentation  
- `camelCase` for method and variable names  
- Prefer `do...end` for multi-line blocks  

**Example:**

```ruby
def getUserName(userId)
    return nil unless userId
    user_service.get_name(userId)
end
```

---

## 🎨 CSS / HTML

- Use [Prettier](https://prettier.io) for formatting  
- 4-space indentation  
- Use lowercase for tag and attribute names  
- Use double quotes for attribute values  
- Use `kebab-case` for class names  

**Example (HTML):**

```html
<div class="user-profile">
    <h1 class="user-name">John Doe</h1>
</div>
```

**Example (CSS):**

```css
.user-profile {
    margin-top: 20px;
    font-size: 16px;
}
```

---

## 🧮 SQL

- Use [sqlfluff](https://www.sqlfluff.com) for linting and formatting  
- Uppercase for SQL keywords  
- Indent nested queries with 4 spaces  
- Align `JOIN` and `WHERE` clauses for readability  

**Example:**

```sql
SELECT user_id, user_name
FROM users
WHERE is_active = TRUE
ORDER BY created_at DESC;
```

---

## 🛠 Tooling Setup

We recommend setting up formatters and linters to run automatically:

- Use Prettier and ESLint with your editor or as pre-commit hooks  
- Use RuboCop via CLI or editor integration  
- Use Black and Flake8 for Python  
- Use sqlfluff for SQL formatting  

---

## ✅ CI Integration

All repositories should include formatting checks in CI pipelines.  
This ensures consistency and prevents formatting issues from being merged.

---

## 📌 Notes

- This guide may evolve as we add more languages or tools.  
- If you need to propose a change, open a pull request to this document.
