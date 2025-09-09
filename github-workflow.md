# 🛠️ Git Workflows Reference

This repo tracks my notes as I learn Nmap. Below are the two workflows I use depending on how I edit files.

---

## 🚀 Workflow 1: Local-Only (VS Code edits)

If I **only edit files in VS Code** on my computer:

1. **Edit in VS Code**  
   Save changes (`⌘S` on Mac).

2. **Stage changes**

   ```bash
   git add .
   ```

   _(or `git add <filename>` to stage a single file)_

3. **Commit with a clear message**

   ```bash
   git commit -m "feat: add notes on <topic>"
   ```

4. **Push to GitHub**
   ```bash
   git push
   ```

✅ One-liner:

```bash
git add . && git commit -m "feat: update notes" && git push
```

---

## 🌐 Workflow 2: Local + GitHub Web Edits

If I **sometimes edit directly on GitHub web** (e.g., quick typo fix online), I need to sync first:

1. **Pull latest changes from GitHub**

   ```bash
   git pull
   ```

2. **Edit in VS Code**  
   Save changes (`⌘S`).

3. **Stage changes**

   ```bash
   git add .
   ```

4. **Commit**

   ```bash
   git commit -m "feat: expand notes on <topic>"
   ```

5. **Push to GitHub**
   ```bash
   git push
   ```

---

## 🧠 Pro Tips

- `git status` → shows what’s modified, staged, or untracked.
- Use clear commit messages (`feat:`, `fix:`, `docs:`) so history doubles as a learning log.
- If you get “merge conflict” errors → you probably forgot to `git pull` before editing (when using Workflow 2).
- Stick to **Workflow 1** unless you _know_ you’ve made changes on GitHub or another machine.
