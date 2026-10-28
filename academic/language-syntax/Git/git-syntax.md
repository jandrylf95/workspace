# Step-by-step Execution Pipeline
#### To set the first commit 

### 1. Create .gitignore file

Open PowerShell and create the file on the root folder you want.
```ps
PS D:\workspace> New-Item -ItemType File -Name ".gitignore" -Force
```

Set the file content:

```ps
PS D:\workspace> Set-Content -Path .gitignore -Value @"
```
```
# ==========================================
# Security and Secrets (Critical Rule)
# ==========================================
.env
.env.*
*.pem
*.key
*.id_rsa

# ==========================================
# Dependencies and Builds
# ==========================================
node_modules/
vendor/
dist/
build/
*.tsbuildinfo

# ==========================================
# Databases and Local Dumps
# ==========================================
*.sql
*.sqlite
*.dump
/backups/

# ==========================================
# Runtime Environments and Logs
# ==========================================
*.log
npm-debug.log*
yarn-debug.log*

# ==========================================
# IDEs and Operating System Metadata
# ==========================================
.vscode/*
!.vscode/settings.json
!.vscode/extensions.json
.idea/
Thumbs.db
desktop.ini
.DS_Store
"@
```

### 2. Initialize local Git repository with 'main' as default branch
```ps
git init -b main
```

### 3. Add all files to staging
```ps
git add .
```

### 4. Verify stage files
```ps
git status
```

### 5. Commit using Conventional Commits standard
```ps
git commit -m "firts  commit"
```

### 6. Link to your GitHub remote repository
```ps
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

### 7. Push local main branch
```ps
git push -u origin main
```