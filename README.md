# Akeed's Articles

A collection of technical articles built with MkDocs and Material theme.

## Setup

1. Clone this repository
2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Local Development

Run the local development server:

```bash
mkdocs serve
```

Visit http://127.0.0.1:8000 to preview your site.

## Adding Articles

1. Create a new Markdown file in `docs/articles/`
2. Add it to the navigation in `mkdocs.yml` (optional)
3. Write your content using Markdown

## Deployment

This site automatically deploys to GitHub Pages when you push to the `main` branch.

Visit your site at: https://akeed.github.io/articles/

## Project Structure

```
.
├── docs/              # Documentation source
│   ├── index.md      # Homepage
│   └── articles/     # Articles directory
├── mkdocs.yml        # MkDocs configuration
├── requirements.txt  # Python dependencies
└── .github/
    └── workflows/
        └── deploy.yml # GitHub Actions workflow
```

## License

MIT
