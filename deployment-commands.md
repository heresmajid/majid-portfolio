# Deployment Commands Guide

## Initial Setup (One Time Only)

### 1. Git Configuration
```bash
git config --global user.name "Muhammad Majid Ahmad"
git config --global user.email "your-email@gmail.com"
```

### 2. Initialize Repository
```bash
# Project folder mein jakar
git init
git add .
git commit -m "Initial commit: Portfolio website"
```

### 3. Connect to GitHub
```bash
# Replace 'your-username' with your GitHub username
git remote add origin https://github.com/your-username/portfolio-website.git
git branch -M main
git push -u origin main
```

## Daily Workflow (For Updates)

### When Making Changes
```bash
# Check what files changed
git status

# Add all changes
git add .

# Commit with meaningful message
git commit -m "Description of changes made"

# Push to GitHub (Netlify will auto-deploy)
git push origin main
```

## Useful Git Commands

### Check Status
```bash
git status                    # See what files are changed
git log --oneline            # See commit history
```

### Undo Changes
```bash
git checkout -- filename    # Undo changes to specific file
git reset HEAD~1            # Undo last commit (keep changes)
```

### Branch Management
```bash
git branch                   # List branches
git checkout -b new-feature  # Create new branch
git checkout main           # Switch to main branch
git merge new-feature       # Merge branch to main
```

## Netlify Commands (Optional)

### Install Netlify CLI
```bash
npm install -g netlify-cli
netlify login
netlify init
```

### Local Testing
```bash
netlify dev                  # Test locally
netlify deploy              # Deploy to preview
netlify deploy --prod       # Deploy to production
```

## Troubleshooting

### If Push Fails
```bash
git pull origin main         # Pull latest changes
git push origin main         # Try push again
```

### If Merge Conflicts
```bash
git status                   # See conflicted files
# Edit files to resolve conflicts
git add .
git commit -m "Resolved merge conflicts"
git push origin main
```

### Reset to Last Working Version
```bash
git reset --hard HEAD~1      # Go back one commit
git push --force origin main # Force push (use carefully)
```