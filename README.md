# The Archivist | Serendipity Engine

**The Archivist** is a single-file, zero-dependency web application designed to facilitate serendipitous intellectual discovery. It functions as a digital "knowledge roulette," allowing users to break free from algorithmic feeds and explore random, curated topics across Philosophy, Science, History, Arts, and Finance.

---

## 📂 Project Context & Disclaimer

**⚠️ Technical Demonstration / Generative AI Artifact**

This software was developed as a **Technical Demonstration** produced with the assistance of **Generative AI**. It serves as a digital component within a larger production by **TRACKS in Research @ PWC**.

While fully functional, the codebase is intended as an experimental interface design and a conceptual prototype rather than a production-hardened application. It explores the intersection of:
* **Curatorial Algorithms:** Moving beyond engagement-based sorting.
* **LLM Integration:** Using AI as a "Librarian" rather than just a content generator.
* **Zero-Build Architecture:** Exploring the limits of modern browser capabilities without complex toolchains.

---

## ✨ Key Features

* **The Serendipity Wheel:** A physics-simulated spinning interface that selects topics from a curated list of over 200 academic categories.
* **Topic Dossier:** Automatically aggregates data for the selected topic, including:
    * **Abstracts:** Pulled from the Wikipedia API.
    * **Public Interest:** Sparkline visualizations of page view trends (last 30 days).
    * **Reference Shelf:** Relevant monographs fetched via the Google Books API.
    * **Cross-References:** Related topics to continue the journey.
* **Scholar's Lens (AI Augmented):** An optional mode that connects to the Google Gemini API. When active, it acts as a "Research Assistant," synthesizing intellectual debates and controversies regarding the topic.
* **Atmospheric UI:** Features three distinct themes (Sepia, Obsidian, Light) with grain overlays and custom animations to evoke the feeling of a digital library.
* **Zero-Build:** The entire application lives in a single `index.html` file, utilizing CDN-hosted React, Tailwind CSS, and Babel.

## 🚀 Quick Start

Because this application uses a "Zero-Build" architecture, you do not need `npm`, `yarn`, or `webpack` to run it.

### Prerequisite
You need a modern web browser (Chrome, Firefox, Edge, Safari).

### Running Locally
Due to **CORS (Cross-Origin Resource Sharing)** policies inherent in modern browsers, fetching data from Wikipedia APIs directly from a file path (`file://...`) may be blocked.

**Recommended Method (VS Code):**
1.  Clone this repository.
2.  Open the folder in VS Code.
3.  Install the "Live Server" extension.
4.  Right-click `index.html` and select "Open with Live Server".

**Alternative (Python):**
1.  Open your terminal/command prompt in the project folder.
2.  Run: `python3 -m http.server`
3.  Open `http://localhost:8000` in your browser.

## 🧠 Configuring "Scholar's Lens" (AI Features)

The application works fully as a passive encyclopedia without an API key. However, to unlock the **Scholar's Lens** (the chat interface and AI synthesis):

1.  Click the **"Standard Mode"** button in the top right navigation.
2.  You will be prompted to enter a **Google Gemini API Key**.
    * *Note: You can get a free key at [Google AI Studio](https://aistudio.google.com/app/apikey).*
3.  The key is **stored temporarily in your browser's memory** for the duration of the session. It is never sent to any backend server other than Google's API endpoint.

## 📚 Data Sources & APIs

The Archivist aggregates real-time data from the following public APIs:

* **Wikipedia API:** For topic extraction, summaries, and category members.
* **Wikimedia REST API:** For page view metrics and analytics.
* **Google Books API:** For retrieving relevant book covers and bibliographic data.
* **Google Gemini API:** (Optional) For conversational synthesis and context.

## 🛠️ Technical Stack

* **Core:** React 18 (via CDN)
* **Styling:** Tailwind CSS (via CDN)
* **Icons:** FontAwesome
* **Transpilation:** Babel Standalone (In-browser)

## 📄 License

This project is open-source and available under the **MIT License**.

---

*Prototyped for the TRACKS @ PWC Launch Initiative. Core concept put forth by [Aaditya Chhatre](https://www.linkedin.com/in/aaditya-chhatre-70a01a215/), features and use-case developed upon later.*
