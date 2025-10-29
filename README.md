# OTUS. CI/CD

## Clone and Push to Your Own GitHub Repository

### 1) Clone the original repository
```bash
git clone https://github.com/ORG/ORIGINAL_REPO.git
cd ORIGINAL_REPO
```
### 2) Change the remote to your own repository
```bash
git remote remove origin
git remote add origin https://github.com/Ilia2704/otus-cicd.git
```

### 3) Verify the remote
```bash
git remote -v
```

#### You should see:
`origin  https://github.com/Ilia2704/otus-cicd.git (fetch)`

`origin  https://github.com/Ilia2704/otus-cicd.git (push)`

### 4) Push your local branch
```bash
git push -u origin HEAD
```

#### Note:
When using HTTPS, GitHub will ask for your username and password.
Use your Personal Access Token (PAT) instead of the password.
