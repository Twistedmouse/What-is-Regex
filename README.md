# What is Regex

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

### Anchors: `^` `$`

Anchors don't match characters Anchors match a position before or after characters: `^` : The caret anchor "^" matches the beginning of a string. `$` : the dollar anchor "$" matches the end of a string.
<br/>

### Examples:

```
^The    -    Matches any string that starts with "The"
end$    -    Matches a string that ends with "end"
^The end$ - Exact string match (starts and ends with "The" & "end")
```

<b>Use Case:</b>
We could use `^[A-Z]` to check if there is a capital letter at the start of an email or `$[.com, .com.au, .org]` ect to check a valid domain input at the end of an email.<br><i>
Although this would not be the best use case. This example is more to understand how this component works.</i></br>

<br>

### Quantifiers: `*` `+` `?` `{}`

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. In the table below you can see Quantifiers support by .NET:
Greedy quantifier|Lazy quantifier|Description
---|---|---
`*`|`*?`|Match zero or more times.
`+`|`+?`|Match one or more times.
`?`|`??`|Match zero or one time.
`{ n }`|`{ n }?`|Match exactly <i>n</i> times.
`{ n,}`|`{ n,}?`|Match at least <i>n</i> times.
`{ n,m }`|`{ n,m }?`|Match from <i>n</i> to <i>m</i> times.

<i>The quantities n and m are integer constants. Ordinarily, quantifiers are greedy; they cause the regular expression engine to match as many occurrences of particular patterns as possible. Appending the ? character to a quantifier makes it lazy; it causes the regular expression engine to match as few occurrences as possible.</i>

Summarized:

- Greedy quantifier first tries to repeat the token as many times as possible, and gradually gives up matches as the engine backtracks to find an overall match.
- Lazy quantifier first repeats the token as few times as required, and gradually expands the match as the engine backtracks through the regex to find an overall match.

Because greediness and laziness change the order in which permutations are tried, they can change the overall regex match.
<i>However, they do not change the fact that the regex engine will backtrack to try all possible permutations of the regular expression in case no match can be found.</i>

### Example:

<i>Now let's look back at our examples in the summary.</i>

Simple example broken down:

`/\S+@\S+\.\S+/`

- "`\S+`" = Match any non whitespace character.
- "`@`" = Must match an @ symbol.
- "`\S+`" Match any non whitespace character.
- "`\.+`" = Must match a "." symbol.
- "`\S`" = Match one or more of any character.

Comprehensive example broken down:

`` /[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*@(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?/g ``

- "`` [a-z0-9!#$%&'*+/=?^_`{|}~-]+ ``" = Match one or more of any the preceding characters within the defined character sets.
- "`` (?:.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)* ``" = Match zero or more of the preceding characters within the defined character sets.
- "`@`" = Must match the @ symbol.
- "`(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?.)+`" = Match one or more of the preceding characters within the defined character sets.
- "`[a-z0-9](?:[a-z0-9-]*[a-z0-9])?`" = Match zero or one of the preceding characters within the defined character sets.
- "`/g`" = Global.
  <br>

### Grouping Constructs:

<br>

### Character Classes:

<br>

### The OR Operator:

<br>

### Flags:

<br>

### Character Escapes:

## <br>

---

## <b>Author:</b>

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

---

---
