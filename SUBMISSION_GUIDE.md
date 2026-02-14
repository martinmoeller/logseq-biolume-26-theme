# Logseq Marketplace Submission Guide

This guide will walk you through the steps to publish your Biolume 26 Theme to the Logseq Marketplace.

## ✅ Pre-Submission Checklist

Before submitting, ensure you have completed all of these steps:

- [ ] **Create a GitHub repository** for your theme
- [ ] **Add an icon** (`icon.png` or `icon.svg`) to represent your theme
- [ ] **Take screenshots** of both light and dark modes and add them to the README
- [ ] **Update all placeholder URLs** in the files (replace `martinmoeller` with your actual GitHub username)
- [ ] **Test your theme locally** in Logseq
- [ ] **Create a GitHub release** with a tag (e.g., `v1.0.1`)
- [ ] **Verify the release** has the automatically generated zip file

## 📋 Step-by-Step Submission Process

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com/new)
2. Create a new repository named `logseq-biolume-26-theme`
3. Make it **public** (required for marketplace)
4. Do **not** initialize with README (we already have one)

### Step 2: Push Your Theme to GitHub

```bash
cd "C:\Users\pfrmo\.gemini\antigravity\scratch\logseq-biolume-26-theme"

# Initialize git repository (if not already initialized)
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: Biolume 26 Theme v1.0.1"

# Add your GitHub repository as remote (replace martinmoeller)
git remote add origin https://github.com/martinmoeller/logseq-biolume-26-theme.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Create an Icon

You need to create an `icon.png` or `icon.svg` file. Recommended specifications:

- **Format**: PNG or SVG
- **Size**: 256x256 pixels (for PNG)
- **Content**: Something that represents the bioluminescent/futuristic aesthetic
- **Colors**: Use your theme colors (Neo-Mint #00FFC2, Electric Violet #9D65FF)

**Icon Ideas:**
- A glowing jellyfish or bioluminescent organism
- Abstract neon geometric shapes
- A stylized "B26" or "Biolume" text logo
- A futuristic plant/flora symbol

You can create this with:
- Design tools: Figma, Canva, Photoshop
- AI image generators: DALL-E, Midjourney
- Icon generators: favicon.io, icons8.com

Once created, save it as `icon.png` in the root directory and commit it:

```bash
git add icon.png
git commit -m "Add theme icon"
git push
```

### Step 4: Take Screenshots

1. **Open Logseq** and load your theme
2. **Take screenshots** showing:
   - **Light mode**: Full interface with some content
   - **Dark mode**: Full interface with some content
   - **Feature highlights**: Tags, bullets, links, code blocks

3. **Save screenshots** to a folder (e.g., `screenshots/`)
4. **Upload screenshots** to your repository or use an image host
5. **Update README.md** with actual screenshot URLs (replace the placeholder)

### Step 5: Update All Placeholder URLs

Search and replace `martinmoeller` with your actual GitHub username in these files:

- [ ] `package.json` - repository URL
- [ ] `manifest.json` - repo field
- [ ] `README.md` - all GitHub links

**Example:**
```bash
# If your GitHub username is "martinmoeller"
# Replace in package.json:
"url": "https://github.com/martinmoeller/logseq-biolume-26-theme.git"

# Replace in manifest.json:
"repo": "martinmoeller/logseq-biolume-26-theme"

# Update README.md links similarly
```

### Step 6: Test Your Theme Locally

1. Open **Logseq**
2. Go to `Settings` → `Plugins`
3. Enable **Developer Mode**
4. Click **Load unpacked plugin**
5. Select your theme directory
6. Go to `Settings` → `Themes`
7. Select "Biolume 26 Light" or "Biolume 26 Dark"
8. **Verify everything works** as expected

### Step 7: Create a GitHub Release

1. Go to your GitHub repository
2. Click on **Releases** (right sidebar)
3. Click **Create a new release**
4. **Tag version**: `v1.0.1`
5. **Release title**: `Biolume 26 Theme v1.0.1`
6. **Description**: Copy features from README
7. Click **Publish release**

The GitHub Actions workflow will automatically create and attach a zip file to the release.

### Step 8: Fork the Logseq Marketplace Repository

1. Go to [https://github.com/logseq/marketplace](https://github.com/logseq/marketplace)
2. Click **Fork** button (top right)
3. This creates your own copy of the marketplace repository

### Step 9: Add Your Theme to the Marketplace

1. In **your forked marketplace repository**, navigate to `packages/`
2. Click **Add file** → **Create new file**
3. Name it: `packages/logseq-biolume-26-theme/manifest.json`
4. Copy the contents of your `manifest.json` file
5. Commit the new file

6. **Add your icon** to the same directory:
   - Click **Add file** → **Upload files**
   - Upload your `icon.png`
   - Path should be: `packages/logseq-biolume-26-theme/icon.png`

### Step 10: Create Pull Request

1. Go to the **Pull Requests** tab in your fork
2. Click **New Pull Request**
3. Base repository: `logseq/marketplace` (base: `master`)
4. Head repository: `martinmoeller/marketplace` (compare: `master`)
5. Click **Create Pull Request**
6. **Title**: `Add Biolume 26 Theme`
7. **Description**: Fill out the pull request template checklist
8. Click **Create Pull Request**

### Step 11: Wait for Review

The Logseq team will review your submission. They typically respond within 1 business day.

**They will check:**
- ✓ All required files are present
- ✓ Theme works as described
- ✓ No malicious code
- ✓ Quality standards met
- ✓ Documentation is clear

**What to do if requested changes:**
1. Make the changes in your theme repository
2. Update the release if needed
3. Respond to the review comments
4. The PR will be re-reviewed

### Step 12: Celebration! 🎉

Once approved and merged:
- Your theme will appear in the Logseq Marketplace
- Users can install it with one click
- You'll get notifications for issues and feedback

## 📝 Maintenance

After publication, keep your theme updated:

### Releasing Updates

1. Make your changes to the theme
2. Update the `version` in `package.json` (e.g., `1.0.1` → `1.0.2`)
3. Commit and push changes
4. Create a new release with the new version tag
5. The marketplace will automatically detect the update

### Version Numbering

Follow [Semantic Versioning](https://semver.org/):
- **MAJOR** (1.x.x): Breaking changes
- **MINOR** (x.1.x): New features, backward compatible
- **PATCH** (x.x.1): Bug fixes, small tweaks

## 🆘 Getting Help

If you encounter issues:

1. **Check the marketplace documentation**: [GitHub Marketplace Repo](https://github.com/logseq/marketplace)
2. **Review existing themes**: Look at how others structure their submissions
3. **Contact support**: Email support@logseq.com
4. **Ask the community**: Logseq Discord or Forums

## 📚 Useful Resources

- [Logseq Marketplace](https://github.com/logseq/marketplace)
- [Plugin Submission Guide](https://deepwiki.com/logseq/marketplace/3-plugin-submission-process)
- [Example Theme Repositories](https://github.com/logseq/awesome-logseq#themes)
- [Semantic Versioning](https://semver.org/)

---

Good luck with your submission! 🚀
