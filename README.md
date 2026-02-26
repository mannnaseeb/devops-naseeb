# DevOps Naseeb — Flask Portfolio

## Quick Start

### Option 1: Run with Python directly

```bash
# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py
```

Then open: http://localhost:5000

---

### Option 2: Run with Docker

```bash
# Build image
docker build -t devops-naseeb .

# Run container
docker run -p 5000:5000 devops-naseeb
```

Then open: http://localhost:5000

---

### Option 3: Run on a Linux server (production)

```bash
# Install gunicorn
pip install gunicorn

# Run with gunicorn (production-grade)
gunicorn -w 4 -b 0.0.0.0:5000 app:app
```

---

## Project Structure

```
devops-naseeb/
├── app.py              # Flask application
├── requirements.txt    # Python dependencies
├── Dockerfile          # Docker support
└── templates/
    └── index.html      # Your portfolio page
```

## To add more pages

1. Add a new route in `app.py`:
```python
@app.route("/blog")
def blog():
    return render_template("blog.html")
```

2. Create `templates/blog.html`
