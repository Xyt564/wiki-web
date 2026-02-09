# Local Wiki (Flask Version)

A **simple, local wiki web app** built with **Flask**, allowing you to create, edit, delete, and search notes directly from your browser. All data is stored in a local JSON file (`wiki.json`) — no external database required.

This is perfect for personal knowledge management, note-taking, or keeping a local reference library.

---

## Features

* Web-based interface accessible via **localhost**.
* Create, edit, and delete notes.
* **Tag support** for categorizing notes.
* **Search by title or tags**.
* Sidebar navigation with **arrow key support**.
* Minimal and clean design using CSS.

---

## File Structure

```
local-wiki/
├── app.py                 # Main Flask application
├── static/
│   ├── style.css           # Styles for the web app
│   └── script.js           # Sidebar arrow key navigation
├── templates/
│   ├── index.html          # Main view showing all notes
│   └── note.html           # Individual note editing page
└── wiki.json              # Local JSON file storing notes (auto-created)
```

> `wiki.json` is automatically created in the location you specify in `app.py` if it doesn’t exist.

---

## Installation & Setup

1. **Clone the repository**:

```bash
git clone https://github.com/Xyt564/wiki-web.git
```

```
cd wiki-web
```

2. **Install Python dependencies**:

This app requires **Python 3** and **Flask**. 
1. Install python if you havent already

**For Ubuntu / Pop os / debain based systems:**

```bash
sudo apt install python3
```

**For Arch:**

```bash
sudo pacman -S python3
```

**For Windows - go to microsoft store and download from there**

Install Flask via pip:

```bash
pip install Flask
```

3. **Set the data file location**:

In `app.py`, update:

```python
data_file = "YOUR_LOCATION_TO_WIKI.JSON"
```

For example:

```python
data_file = "wiki.json"  # saves in the project root
```

The app will automatically create the file if it doesn’t exist.

4. **Run the app**:

```bash
python app.py
```

By default, the app runs in **debug mode** on `http://127.0.0.1:5000/`.

5. **Open in your browser**:

```
http://127.0.0.1:5000/
```

---

## Usage

* **Add a note**: Enter a title in the "New note title" field and click **Add Note**.
* **View/edit a note**: Click a note title in the sidebar. Update content or tags and click **Save**.
* **Delete a note**: Click the red **Delete** button while viewing a note.
* **Search**: Use the search box at the top to filter notes by title or tag.
* **Keyboard navigation**: Use **Arrow Up/Down** in the sidebar to quickly select notes.

---

## Notes & Customization

* All data is stored **locally** in the JSON file; no cloud storage.
* Tags are **comma-separated** (e.g., `python, flask, notes`).
* The sidebar sorts notes **alphabetically**.
* You can customize CSS in `static/style.css` to change colors, fonts, and layout.
* `script.js` controls **sidebar keyboard navigation** and scrolling behavior.

---

## Security

* This app is intended for **local use only**.
* Do **not expose** the Flask app to the internet without proper security measures.
* All data is stored **plainly** in a JSON file; sensitive information should be encrypted manually if needed.

---

## License

This project is licensed under the **MIT License**, one of the most permissive and widely used open-source licenses. Below is the full text:

```
MIT License

Copyright (c) 2026 Xyt564

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

> In short: You can use, modify, and redistribute the software freely, but you must include this copyright and license notice. The software is provided “as-is,” without warranty.

---
