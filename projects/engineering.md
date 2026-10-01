# Languages, algorithms and data structures across my projects

[← Back to my portfolio](../README.md)

Python is my strongest programming language. This guide connects the wider technical skills in my portfolio to concrete implementation examples. For team projects, these techniques describe the application as a whole; each repository separately documents my contributions.

## Canvas Dates — Python automation and data processing

**Languages:** Python, with shell scripts for installation and local commands.

- **Lists and dictionaries:** assessment records, assignment-group lookups, manually entered weights and dismissed items.
- **Parsing and normalisation:** unfolded iCalendar lines and VEVENT properties, time-zone-aware dates, and normalised course/assessment titles.
- **Sorting and filtering:** due-date ordering, removal of submitted items and selection of assessment-shaped events.
- **Weighted aggregation:** an assessment's share is its fraction of group points multiplied by the group's weight; the alternative points-based path uses its share of total points.
- **Persistence and caching:** JSON-backed settings and records, plus cached data for offline use.

Source: [grade-weight calculation and pipeline](https://github.com/khokharzain/canvas-dates/blob/main/canvasdates/fetcher.py), [calendar parser](https://github.com/khokharzain/canvas-dates/blob/main/canvasdates/icsfeed.py), [local data storage](https://github.com/khokharzain/canvas-dates/blob/main/canvasdates/store.py).

## SkillDev — Java collections and relational persistence

**Languages:** Java and SQL, with FXML/XML for interfaces and Maven configuration.

- **Lists/ArrayLists:** users, skills, reviews, messages and search/matching results.
- **Sets:** deduplication of available skill names.
- **Match scoring:** comparisons between teaching and learning skills, capped compatibility scores and descending score ordering. This rule-based path is separate from LLM-generated suggestions.
- **Relational modelling:** users, posts, participants and join requests connected through SQLite; controllers call DAO interfaces and JDBC implementations.
- **Local LLM workflow:** profile context is assembled into prompts sent to Ollama for recommendations, comparisons and scheduling suggestions.

Source: [matching and collection operations](https://github.com/khokharzain/CAB302-/blob/main_branch/src/main/java/com/example/newdesign/controller/AIController.java), [Ollama prompts and HTTP integration](https://github.com/khokharzain/CAB302-/blob/main_branch/src/main/java/com/example/newdesign/model/OllamaService.java), [DAO implementations](https://github.com/khokharzain/CAB302-/tree/main_branch/src/main/java/com/example/newdesign/model).

## ApertureX — TypeScript, SQL and security foundations

**Languages:** TypeScript and SQL, with React/TSX components and HTML/CSS presentation. **Work in progress; private source.**

- **Typed records, arrays and sets:** enquiry data, query parameters and accepted-value allowlists.
- **SQL queries:** bound parameters, filtering, counts, date ordering, and LIMIT/OFFSET pagination.
- **Fixed-window rate limiting:** database-backed counters limit public form submissions within time windows.
- **Authentication checks:** Cloudflare Access JWT signature and claim verification using platform cryptographic APIs, with cached public signing keys.
- **Cryptographic foundations:** platform SHA-256 and PBKDF2 operations, random token generation and byte-array comparisons. Gallery-related primitives exist, while private media delivery remains planned.

Read the [public architecture and implementation overview](aperturex.md). Private code and environment configuration are not published here.

## Bollywood Beats — Python, relational models and booking rules

**Languages:** Python and SQL, with HTML/Jinja templates, CSS and JavaScript for the browser interface.

- **Relational entities:** users, events, ticket types, bookings and comments linked by foreign keys and SQLAlchemy relationships.
- **Filtering and sorting:** event search/category filters and date-based catalogue/history ordering.
- **Aggregation and branching:** quantities are summed to derive remaining event capacity; cancellation, start time and availability determine event status.
- **Price arithmetic:** Decimal values preserve fixed-precision booking amounts.
- **Password handling:** Werkzeug PBKDF2 hashing supports account registration and login.

Source: [models and capacity calculations](https://github.com/harrybhatiadevs/IAB207-A2/blob/main/BollywoodBeats/models.py), [routes and booking decisions](https://github.com/harrybhatiadevs/IAB207-A2/blob/main/BollywoodBeats/views.py), [workflow diagrams and limits](https://github.com/harrybhatiadevs/IAB207-A2/blob/main/docs/workflows.md). Payments are simulated, and capacity checks do not establish transactional prevention of concurrent overselling.

## Coaching by Manav — JavaScript interaction and animation

**Languages:** JavaScript, HTML and CSS.

- **Collections and state:** navigation/section element collections, pause flags, motion preferences and gallery scroll state.
- **Frame-based animation:** requestAnimationFrame advances the gallery, carrying fractional movement between frames.
- **Scroll-position wrapping:** duplicated slides and a half-width boundary allow the gallery to loop.
- **Batched updates:** scroll feedback is queued into animation frames; IntersectionObserver supports section reveals and active navigation.

Source: [browser interaction logic](https://github.com/khokharzain/coaching-by-manav/blob/main/js/script.js), [architecture notes](https://github.com/khokharzain/coaching-by-manav/blob/main/docs/architecture.md).

## Interactive Anniversary Microsite — Browser state and events

**Languages:** JavaScript, HTML and CSS.

- **Arrays and indices:** gallery slides and navigation positions.
- **Scene transitions:** input, transition events and timers coordinate the reveal sequence.
- **Date arithmetic:** timestamp differences drive live elapsed-time/countdown displays.
- **Browser SHA-256:** Web Crypto computes a digest for a playful unlock-code interaction. This is a client-side effect, not authentication.
- **Event handling:** keyboard input, touch gestures and user-triggered browser audio.

Source: [interaction flow and engineering explanation](https://github.com/khokharzain/for-my-aloo#interaction-flow). Personal messages and media are not reproduced in this guide.

## Academic foundation and current interests

My coursework covers cybersecurity, secure network architectures, cloud computing, web development, database management, algorithms and complexity, machine learning and agile software engineering. Additional coursework languages include C# and embedded C; data tools include Pandas, NumPy and Jupyter Notebook.

My strongest interests are **cybersecurity, AI prompting and LLMs**. I am actively seeking an internship to apply my Python and software-development skills, contribute to a team and deepen these areas.
