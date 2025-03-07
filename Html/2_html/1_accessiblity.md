# Accessibility Notes

## What Is Accessibility?
Accessibility ensures that digital content is usable by people with disabilities. It involves designing websites and applications to be inclusive for all users, including those with visual, auditory, motor, and cognitive impairments.

### Example:
```html
<button aria-label="Submit Form">Submit</button>
```

## What Are Screen Readers, and Who Uses Them?
Screen readers are software applications that convert digital text into speech or Braille output, allowing visually impaired users to navigate digital content.

### Example:
```html
<img src="logo.png" alt="Company Logo">
```

## What Are Large Text or Braille Keyboards, and Who Uses Them?
Large text keyboards are used by individuals with low vision, featuring oversized keys and high-contrast labels. Braille keyboards allow blind users to type and read using Braille characters.

## What Are Alternative Pointing Devices Such as Trackballs, Joysticks, and Touchpads Used For?
These devices help individuals with motor disabilities who may find traditional mice difficult to use. They provide alternative ways to control a cursor.

## What Are Screen Magnifiers Used For?
Screen magnifiers enlarge digital content, making it easier for users with low vision to read text and view images without strain.

### Example:
Users can enable built-in magnifiers in operating systems, such as Windows Magnifier or macOS Zoom.

## What Is Voice Recognition Software Used For?
Voice recognition software allows users to control devices and input text using voice commands, benefiting individuals with mobility impairments or those who cannot use traditional input methods.

### Example:
```python
import speech_recognition as sr
r = sr.Recognizer()
with sr.Microphone() as source:
    audio = r.listen(source)
    text = r.recognize_google(audio)
    print(text)
```

## What Are Some Common Accessibility Auditing Tools to Use?
- **Lighthouse** (Chrome DevTools) – Audits accessibility scores
- **axe DevTools** – Detects WCAG violations
- **WAVE** – Evaluates accessibility and suggests improvements
- **NVDA & JAWS** – Screen reader testing tools

## How Does Proper Heading Level Structure Affect Accessibility?
Correct heading structures help screen reader users navigate content efficiently. Headings should follow a logical order (h1 → h2 → h3) to maintain clarity.

### Example:
```html
<h1>Main Title</h1>
  <h2>Subheading</h2>
    <h3>Detail</h3>
```

## What Are Best Practices for Tables and Accessibility?
- Use `<th>` for headers with `scope` attributes.
- Provide captions using `<caption>`.
- Use ARIA attributes if necessary.

### Example:
```html
<table>
  <caption>Student Grades</caption>
  <tr>
    <th scope="col">Name</th>
    <th scope="col">Grade</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>A</td>
  </tr>
</table>
