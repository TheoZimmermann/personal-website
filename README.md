# Theo Zimmermann's Website

A simple static website built with HTML and Tailwind CSS v4.

## Local Development

### Prerequisites

- Node.js (v20 or higher recommended)
- npm

### Setup

1. Install dependencies:
```bash
npm install
```

2. Build the CSS:
```bash
npm run build
```

3. Open `src/index.html` in your browser to view the site.

### Development Workflow

To watch for changes and automatically rebuild CSS:
```bash
npm run watch
```

This will watch your CSS files and rebuild automatically when you make changes.

## Deployment to GitHub Pages

### Initial Setup

1. **Create a GitHub repository** for your project (if you haven't already)

2. **Initialize git and push your code**:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

3. **Enable GitHub Pages in your repository settings**:
   - Go to your repository on GitHub
   - Click on **Settings** → **Pages**
   - Under "Build and deployment":
     - Source: Select **GitHub Actions**
   
4. **Push to trigger deployment**:
   - The GitHub Action will automatically run when you push to the `main` branch
   - Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

### Automatic Deployment

Once set up, every push to the `main` branch will automatically:
1. Install dependencies
2. Build the Tailwind CSS
3. Deploy the `src` folder to GitHub Pages

You can monitor the deployment progress in the **Actions** tab of your GitHub repository.

## Project Structure

```
theozimmermann-website/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions workflow for deployment
├── src/
│   ├── index.html              # Main HTML file
│   ├── input.css               # Tailwind CSS source
│   └── output.css              # Generated CSS (not committed to git)
├── .gitignore                  # Git ignore file
├── package.json                # Node.js dependencies and scripts
└── README.md                   # This file
```

## Technologies Used

- **Tailwind CSS v4** - Utility-first CSS framework
- **GitHub Pages** - Static site hosting
- **GitHub Actions** - CI/CD for automatic deployment