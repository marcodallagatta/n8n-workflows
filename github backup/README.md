# n8n → GitHub Workflow Backup

Automate syncing your n8n workflows to a GitHub repository as versioned `.json` files.

---

## 🚀 What It Does

- 📥 Fetches all n8n workflows
- 🔍 Compares each with its GitHub version
- ✅ Adds new files
- ✏️ Updates changed files
- 🗑️ (Optional) Deletes removed workflows

---

## ⚙️ Setup

1. **Import the workflow** into n8n
2. **Set up credentials**:
   - GitHub API (for editing/creating files)
   - n8n API (optional for self-host API access)
3. **Update the `Globals` node**:
   - `repo.owner`: your GitHub username/organization
   - `repo.name`: the repo to push to
   - `repo.path`: folder to store files (e.g. `workflows/`)

4. **Triggering**:
   - Run manually via **Execute Workflow**
   - Or auto-run via the built-in **Cron** node (every 6h by default)

---

## ✅ After Setup

- Run the workflow
- Check your GitHub repo for updated `.json` backups under `workflows/`

---

## 🔧 Tips

- Commit messages reflect the status: _new_ / _update_ / _same_
- Credentials must be added manually post-import
- Customize folders, formats, or logic as needed

---

## 🔗 Resources

- [n8n Documentation](https://docs.n8n.io/)
- [GitHub REST API](https://docs.github.com/en/rest)
- [n8n Community](https://community.n8n.io/)
