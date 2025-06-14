### Step 1: Created a feature branch in VS Code
*Used the Source Control menu in Visual Studio Code to create a new branch for this assignment.*

![Feature Branch](./New%20feature%20branch.png)

---

### Step 2: Ran `git branch` and `git branch -r`
*Compared local and remote branches using CLI.*

**Difference:**  
- `git branch` shows **local branches only**.  
- `git branch -r` shows **remote branches only**, such as those on GitHub.

![Branch Check](./git%20branch%20and%20git%20branch%20-%20r.png)

---

### Step 3: Committed local changes
*Staged and committed updates to the feature branch using CLI.*

![Commit](./Commit.png)

---

### Step 4: Published Feature Branch
*Pushed the new feature branch to the remote repo using Visual Studio Code.*

![Push Branch](./Published%20Feature%20Branch.png)

---

### Step 5: Created a pull request and deleted branch on GitHub
*Merged the feature branch into the main branch via a GitHub pull request and deleted the remote feature branch.*

![Pull Request](./Pull%20Request%20and%20Delete%20on%20GitHub.png)

---

### Step 6: Ran `git fetch -p` and checked local branches
*Updated local Git metadata and confirmed which branches still existed locally.*

**Q: Will the local feature branch still exist after the remote is deleted?**  
**A:** Yes, the local feature branch remains on your machine until you delete it manually.

![Fetch](./Git%20fetch%20-p%20and%20git%20branch.png)