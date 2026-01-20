# GitHub Snake Animation Setup Guide

## 🐍 What This Does
This setup will automatically generate a snake animation that "eats" your **real GitHub contributions** from your contribution graph!

## 📋 Setup Instructions

### Step 1: Push These Files to GitHub
You need to push the following files to your GitHub repository:
- `.github/workflows/snake.yml` (GitHub Actions workflow)
- `README.md` (Updated README with new snake animation links)

```bash
git add .github/workflows/snake.yml README.md
git commit -m "Add snake animation workflow for real contribution data"
git push origin main
```

### Step 2: Run the GitHub Action
After pushing, the GitHub Action will run automatically. You can also trigger it manually:

1. Go to your repository on GitHub: https://github.com/Ampexqt/Ampexqt
2. Click on the "Actions" tab
3. Click on "Generate Snake Animation" workflow
4. Click "Run workflow" button
5. Wait for it to complete (usually takes less than a minute)

### Step 3: Verify the Output
Once the action completes:
1. Check that a new branch called `output` was created
2. This branch will contain your generated snake animations:
   - `github-contribution-grid-snake.svg` (light mode)
   - `github-contribution-grid-snake-dark.svg` (dark mode)
   - `ocean.gif` (ocean-themed animated version)

### Step 4: View Your README
Your README will now display the snake animation with YOUR real contribution data!

## 🔄 How It Updates
- **Automatically**: Runs every 24 hours to update with your latest contributions
- **On Push**: Runs every time you push to the main branch
- **Manually**: You can trigger it anytime from the Actions tab

## 🎨 Customization Options

### Change the Snake Color
Edit `.github/workflows/snake.yml` and modify the `outputs` section:

```yaml
outputs: |
  dist/github-contribution-grid-snake.svg
  dist/github-contribution-grid-snake-dark.svg?palette=github-dark
  dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
```

Available color options:
- `color_snake`: Color of the snake (e.g., `orange`, `blue`, `#FF5733`)
- `color_dots`: Colors for contribution levels (comma-separated hex colors)

### Use the Ocean Theme
If you prefer the animated ocean-themed version, uncomment the alternative section in your README:

```markdown
<!-- Alternative: Ocean-themed snake animation -->
<p align="center">
<img src="https://raw.githubusercontent.com/Ampexqt/Ampexqt/output/ocean.gif" alt="Snake animation" />
</p>
```

## 🐛 Troubleshooting

### Snake animation not showing?
1. Make sure the GitHub Action completed successfully
2. Check that the `output` branch exists
3. Wait a few minutes for GitHub's CDN to update
4. Try hard-refreshing your browser (Ctrl+F5)

### Action failing?
1. Check the Actions tab for error messages
2. Ensure your repository is public (or you have proper permissions)
3. Verify the workflow file syntax is correct

## 📚 Learn More
- [Platane/snk GitHub Repository](https://github.com/Platane/snk)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
