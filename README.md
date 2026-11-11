Newspaper Layout App
A comprehensive, production-grade responsive multi-section newspaper editorial layout engineered with semantic HTML5 architecture and advanced CSS Grid systems. This project fulfills all technical specifications, accessibility benchmarks, and automated lab test cases for robust web layouts.

1. Project Overview & Architecture
The Newspaper Layout App replicates the classic, structured visual hierarchy of traditional broadsheet newspapers while utilizing modern, fluid web standards. Built from the ground up to handle varying viewport dimensions, the layout leverages explicit grid placement matrices to position complex editorial pieces without relying on fragile float or inline-block hacks.

+-----------------------------------------------------------------+
|                         TITLE / HEADER                          |
+-----------------------------------+-----------------------------+
|                                   |                             |
|          FEATURE ARTICLE          |         COVER IMAGE         |
|         (Spans 2 Columns)         |    (Spans Rows 2 and 3)     |
|                                   |                             |
+-----------------------------------+-----------------------------+
|                                   |                             |
|         SECONDARY ARTICLE         |         COVER IMAGE         |
|         (Spans 2 Columns)         |        (Continuation)       |
|                                   |                             |
+-----------------+-----------------+-----------------+-----------+
|  SMALL ARTICLE  |  SMALL ARTICLE  |  SMALL ARTICLE  |           |
|       #1        |       #2        |       #3        |           |
+-----------------+-----------------+-----------------+-----------+
2. Technical Specifications & Grid Mechanics
The core engine of this layout relies on CSS Grid layout modules defined within .newspaper-layout. Below is a breakdown of the structural parameters governing the application:

A. Template Columns & Rows
Columns: Divided evenly into three fractional units (repeat(3, 1fr)), allowing articles and imagery to scale gracefully across standard and ultra-wide displays.

Rows: Explicitly structured using grid-template-rows: auto 1fr 1fr 1fr;, where the header adapts dynamically to its content height while the content rows distribute remaining vertical space proportionally.

B. Named Grid Areas Matrix
The layout mapping utilizes explicit layout strings via grid-template-areas:

CSS
.newspaper-layout {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: auto 1fr 1fr 1fr;
  grid-template-areas:
    "title title title"
    "feature-article feature-article cover-image"
    "secondary-article secondary-article cover-image"
    "small-article1 small-article2 small-article3";
  gap: 1.5rem;
}
3. Detailed File Structure
Plaintext
newspaper-layout-app/
│
├── index.html              # Core semantic structure containing all landmark tags
├── styles.css              # Grid system, typography styling, and media queries
├── assets/                 # Directory for editorial imagery and graphics
│   └── cover-graphic.jpg   # Main publication cover illustration
└── README.md               # Comprehensive project documentation and guide
4. Setup, Installation & Local Development
To get a local copy of this repository up and running on your machine, follow these simple steps using your terminal:

Step 1: Clone the Repository
Bash
git clone https://github.com/Regalson001/newspaper-layout-app.git
Step 2: Navigate to the Project Directory
Bash
cd newspaper-layout-app
Step 3: Open in Your Editor or Browser
Open the directory in VS Code:

Bash
code .
Launch index.html using a local development server (such as the VS Code Live Server extension) or double-click the file to open it directly in your web browser.

5. Development Roadmap & Future Enhancements
[x] Phase 1: Establish core HTML5 landmark elements and baseline typography.

[x] Phase 2: Implement CSS Grid architecture, templates, and named areas.

[x] Phase 3: Integrate responsive image constraints (max-width: 100%) and automated unit test verification.

[ ] Phase 4: Introduce a dark mode toggle utilizing CSS custom properties.

[ ] Phase 5: Expand editorial sections with dynamic JavaScript-powered RSS feeds.

6. Author & License
Author: Oyugi (Regalson001)

Course/Track: Software Development & Technical Engineering Lab

License: Distributed under the MIT License. See LICENSE for more information
