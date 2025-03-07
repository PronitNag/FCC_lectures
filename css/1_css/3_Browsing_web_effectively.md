# Web Browsers, Websites, and Search Engines

## 1. Common Web Browsers and Installation

### Popular Web Browsers
- **Google Chrome**
- **Mozilla Firefox**
- **Microsoft Edge**
- **Apple Safari**
- **Brave**
- **Opera**

### How to Install a Web Browser

#### Windows (Google Chrome Example)
```sh
# Download and install Chrome using PowerShell
Start-Process "https://www.google.com/chrome/" -Wait
```

#### Linux (Google Chrome Example)
```sh
# Install Chrome on Debian-based systems
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
```

#### macOS (Google Chrome Example)
```sh
# Install Chrome using Homebrew
brew install --cask google-chrome
```

---

## 2. Difference Between a Web Browser, a Website, and a Search Engine

| Feature        | Web Browser       | Website         | Search Engine       |
|---------------|------------------|----------------|----------------------|
| Definition    | Software to access websites | Collection of web pages | Tool to find websites |
| Example      | Chrome, Firefox   | amazon.com, github.com | Google, Bing, DuckDuckGo |
| Functionality | Displays websites | Provides content/services | Searches the internet |

#### Example: Accessing a Website in a Browser via Code
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
</body>
</html>
```

---

## 3. How to Use a Search Engine Effectively

### Key Tips for Effective Searching
- **Use Specific Keywords**: Instead of *best phone*, try *best budget smartphone 2025*.
- **Use Quotes for Exact Match**: Searching `"machine learning basics"` returns exact matches.
- **Use Site-Specific Search**: `site:wikipedia.org Python programming` limits results to Wikipedia.
- **Use Boolean Operators**:
  - `AND`: `solar panels AND installation`
  - `OR`: `cheap OR affordable laptops`
  - `-` (minus sign) to exclude: `apple -fruit`

#### Example: Using Google Search Effectively
```sh
# Find PDFs on JavaScript tutorials
"JavaScript tutorial" filetype:pdf

# Search for articles from a specific website
site:developer.mozilla.org "async JavaScript"

