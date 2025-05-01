# Code Difference Checker

[![Release Date](https://img.shields.io/badge/Release-May%2001,%202025-brightgreen.svg)](https://github.com/imamwahyudime/duplicate-file-finder/releases/tag/v1.2.0)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

A simple, browser-based tool to visually compare two blocks of text or code and highlight the differences side-by-side.

![image](https://github.com/user-attachments/assets/b8818005-696b-4cd0-95f1-afd9ac34c878)

## Features:

* **Side-by-Side View:** Clearly displays the original and modified text/code next to each other.
* **Difference Highlighting:**
    * Added lines shown with a green background.
    * Removed lines shown with a red background.
    * Common lines shown with a light gray background.
* **Line Numbering:** Displays line numbers for easy reference in both panes.
* **Responsive Design:** Adapts layout for usability on smaller screens (text areas and diff panes stack vertically).
* **Client-Side:** All processing happens directly in your browser using JavaScript; no server-side component needed.
* **Easy to Use:** Just paste your text/code snippets and click "Compare".

## Usage:

- **Option 1:**
1. Go to https://imamwahyudime.github.io/code-comparison-webapp/
2. Enjoy!

- **Option 2:**
1.  Clone or download this repository.
2.  Open `index.html` in your web browser.
3.  Enjoy!

## Technology Stack:

* **HTML5:** For the basic structure of the page.
* **Tailwind CSS:** For utility-first CSS styling (loaded via CDN).
* **Custom CSS:** For specific diff view styles (like line highlighting and layout).
* **JavaScript (Vanilla):** For DOM manipulation and handling user interaction.
* **jsdiff Library:** A JavaScript library for text differencing (loaded via CDN).

## Dependencies (via CDN):

* [Tailwind CSS](https://tailwindcss.com/)
* [jsdiff](https://github.com/kpdecker/jsdiff)

## How It Works:

The tool utilizes the `jsdiff` library (`Diff.diffLines` function) to compute the line-by-line differences between the content of the two text areas. 
The resulting difference array is then processed by a custom JavaScript function (`renderDiff`) which dynamically generates HTML `div` elements for each line. 
These elements are styled using CSS (Tailwind and custom styles) to show line numbers and background colors indicating whether a line was added, removed, or remained unchanged.
