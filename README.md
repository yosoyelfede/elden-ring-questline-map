# 💍 Elden Ring Ultimate Quest Tracker

A lightweight, interactive web dashboard to map and track Elden Ring's complex web of NPC quests, critical triggers, and point-of-no-return lockouts. 

Elden Ring's questlines are notoriously tangled. This tool visualizes the progression of every major and minor NPC, allowing you to filter by specific characters, view exact locations, and—most importantly—see exactly what actions will permanently break a questline.

## ✨ Features

* **Interactive Network Graph:** Visually trace the chronological flow of quests and how they intersect with major story triggers.
* **Granular Quest Filtering:** Isolate specific groups (e.g., "Magic Tutors" or "Volcano Manor") to remove the noise and focus on your current run.
* **Detailed Context Sidebar:** Click on any node to reveal what to do, exact locations (Sites of Grace), and explicit lockout warnings.
* **Zero-Setup Local Execution:** Runs entirely in the browser using CDNs. No build steps, no package managers.

## 🚀 How to Use

Since this is built as a single, self-contained HTML file, getting started is instant:

1. Clone or download this repository.
2. Open `EldenRingQuests_Ultimate.html` in any modern web browser.
3. *Optional:* Use the dropdown in the top-left to filter down to specific questlines. Click any node to view detailed instructions on the left panel.

## 🛠️ Tech Stack

* **HTML5 / Vanilla JavaScript**
* **[Vis.js Network](https://visjs.org/):** For rendering the interactive node-based graph.
* **[Tailwind CSS (via CDN)](https://tailwindcss.com/):** For clean, responsive UI styling without writing custom CSS.

## 📝 How to Modify or Add Quests

All quest data and graph logic are contained directly within the `<script>` tag of the HTML file. 

To add a new step or character:
1. **Update `questData`:** Add a new dictionary entry with `title`, `location`, `action`, and `warning`.
2. **Update `nodesData`:** Add a new node object specifying the `id`, `label`, `group` (for filtering), and hierarchical `level` (how far down the timeline it appears).
3. **Update `edgesData`:** Draw lines connecting your new node to existing ones using `{from: id, to: id}`. Add `dashes: true` or custom colors to denote lockouts or item transfers.

## 📄 License

This project is open-source and available under the MIT License. Feel free to fork, modify, and expand the map!
