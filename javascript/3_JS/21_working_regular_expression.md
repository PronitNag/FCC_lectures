# Regular Expressions Notes

## What Are Regular Expressions, and What Are Some Common Methods?
Regular expressions (regex) are sequences of characters defining a search pattern. They are widely used for pattern matching and text processing.

### Common Methods:
#### Python:
```python
import re
pattern = r"\d+"  # Matches one or more digits
text = "Order 123 was placed on 2024-03-06"
match = re.search(pattern, text)
print(match.group())  # Output: 123
```

#### JavaScript:
```javascript
const pattern = /\d+/g;
const text = "Order 123 was placed on 2024-03-06";
const match = text.match(pattern);
console.log(match);  // Output: ['123', '2024', '03', '06']
```

---

## What Are Some Common Regular Expression Modifiers Used for Searching?
Modifiers alter how a regex pattern is interpreted.

### Common Modifiers:
- `i` - Case-insensitive search
- `g` - Global search (find all matches)
- `m` - Multiline search

#### Example (JavaScript):
```javascript
const pattern = /hello/i;
console.log(pattern.test("Hello World"));  // Output: true
```

#### Example (Python):
```python
pattern = re.compile(r"hello", re.IGNORECASE)
print(bool(pattern.search("Hello World")))  # Output: True
```

---

## How Can You Match and Replace All Occurrences in a String?
Using regex, we can replace matched substrings with a new value.

#### Python:
```python
text = "apple banana apple"
new_text = re.sub(r"apple", "orange", text)
print(new_text)  # Output: orange banana orange
```

#### JavaScript:
```javascript
const text = "apple banana apple";
const newText = text.replace(/apple/g, "orange");
console.log(newText);  // Output: orange banana orange
```

---

## What Are Character Classes, and What Are Some Common Examples?
Character classes define sets of characters to match.

### Common Examples:
- `[a-z]` - Matches any lowercase letter
- `[A-Z]` - Matches any uppercase letter
- `[0-9]` - Matches any digit
- `\w` - Matches any word character (equivalent to `[a-zA-Z0-9_]`)
- `\d` - Matches any digit (equivalent to `[0-9]`)

#### Example:
```python
pattern = r"\d+"
text = "My number is 12345"
print(re.findall(pattern, text))  # Output: ['12345']
```

---

## What Are Lookahead and Lookbehind Assertions, and How Do They Work?
Lookaheads and lookbehinds allow matching patterns based on context without including them in the match.

### Lookahead:
#### Python:
```python
pattern = r"\d+(?= dollars)"
text = "Price is 100 dollars"
print(re.search(pattern, text).group())  # Output: 100
```

### Lookbehind:
```python
pattern = r"(?<=USD )\d+"
text = "Total: USD 500"
print(re.search(pattern, text).group())  # Output: 500
```

---

## What Are Regex Quantifiers, and How Do They Work?
Quantifiers specify how many times a character or group can appear.

### Common Quantifiers:
- `*` - Matches 0 or more times
- `+` - Matches 1 or more times
- `?` - Matches 0 or 1 time
- `{n}` - Matches exactly `n` times
- `{n,}` - Matches `n` or more times
- `{n,m}` - Matches between `n` and `m` times

#### Example:
```python
pattern = r"a{2,4}"
text = "aaa aaaaa a aa"
print(re.findall(pattern, text))  # Output: ['aaa', 'aaaa']
```

---

## What Are Capturing Groups and Backreferences, and How Do They Work?
Capturing groups allow part of a regex match to be referenced later.

#### Example:
```python
pattern = r"(\w+)\s+\1"
text = "hello hello world"
print(re.search(pattern, text).group())  # Output: hello hello
```

#### Using Backreference in Replace:
```javascript
const text = "apple apple banana";
const newText = text.replace(/(\w+) \1/, "$1");
console.log(newText);  // Output: apple banana

