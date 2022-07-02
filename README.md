# What-is-Regex

---

## <b>Summary</b>

"Regex" or "RegEx" stands for "regular expressions" and are patterns used to match character combinations in a string. Regex are used for many things such as email validation, phone number verification or even matching hexadecimal values. So you can probably tell Regex are used by string searching algorithms for "find" or "find and replace" operations on strings, or for input validation.  
<br>
So for this tutorial we will show you how you can check if an email has the valid inputs with RegEx.  
<br>

### <b>Examples:</b>

- Simple RegEx Validation:

```
/\S+@\S+\.\S+/
```

- More Specific Validation:

```
/[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*@(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?/g
```

---

## <b>Regex Components</b>

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

---

### <b>Anchors:</b> `^` `$`

Anchors don't match characters Anchors match a position before or after characters: `^` : The caret anchor "^" matches the beginning of a string. `$` : the dollar anchor "$" matches the end of a string.
<br/>

### Examples:

```
^The    -    Matches any string that starts with "The"
end$    -    Matches a string that ends with "end"
^The end$ - Exact string match (starts and ends with "The" & "end")
```

<b>Use Case:</b>
We could use `^[A-Z]` to check if there is a capital letter at the start of an email or `$[.com, .com.au, .org]` ect to check a valid domain input at the end of an email.
Although this would not be the best use case. This example is more to understand how this component works.

<br>

### <b>Quantifiers:</b> `*` `+` `$` `{}`

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

<br>

### <b>Grouping Constructs:</b>

<br>

### <b>Character Classes:</b>

<br>

### <b>The OR Operator:</b>

<br>

### <b>Flags:</b>

<br>

### <b>Character Escapes:</b>

## <br>

---

## <b>Author:</b>

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

---

---
