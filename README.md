# Professional Portfolio Website

This is your personal portfolio website built with **Vite** and **Vanilla JavaScript**. It's designed to be fast, responsive, and easy to deploy.

## Project Structure

- `index.html`: The main page content.
- `style.css`: All styles (modern variables, dark mode).
- `main.js`: Interactivity (scroll, mobile menu).
- `vite.config.js`: Configuration for correct path handling on GitHub Pages.

## How to Run Locally

You should have Node.js installed.

1.  **Open your terminal** in this directory.
2.  **Install dependencies** (if you haven't already):
    ```bash
    npm install
    ```
3.  **Start the development server**:
    ```bash
    npm run dev
    ```
4.  Open the local URL provided (usually `http://localhost:5173`).

## How to Deploy to GitHub Pages

1.  **Create a Repository** on GitHub.
2.  **Push your code**:
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
    git push -u origin main
    ```
3.  **Enable GitHub Pages**:
    - Go to your repository **Settings** -> **Pages**.
    - Under **Build and deployment**, select **Source** as `GitHub Actions` (if you want to set up an action) OR just select **Deploy from a branch**.
    - If selecting "Deploy from a branch":
        - You might need to build it first.
        - **Easiest method**: Run `npm run build` locally. This creates a `dist` folder.
        - NOTE: The simplest way for a static site like this creates is to:
            1.  Run `npm run build`
            2.  Commit the `dist` folder using `git add dist -f` (if it's ignored) or usage a subtree push.
            
    **Recommended Flow for Vite**:
    1.  Create a file `.github/workflows/deploy.yml` with standard Vite deployment configuration (see Vite docs).
    2.  OR, since this is a simple static site:
        - Go to Settings -> Pages.
        - Source: **GitHub Actions**.
        - Select **Static HTML**.
        - It will look for `index.html`. 
        - **WAIT**: Since we use Vite, we normally need to build.
        
    **Simplest Manual Deployment**:
    1.  Run `npm run build`.
    2.  This generates a `dist` folder.
    3.  Upload the contents of the `dist` folder to your GitHub repository (or a separate `gh-pages` branch).

## Customization

- **Colors**: Edit the `:root` variables in `style.css`.
- **Text**: Update the HTML content in `index.html`.
