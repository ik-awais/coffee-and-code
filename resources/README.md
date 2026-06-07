# 📚 Git & GitHub Resources

Helpful resources for learning Git and GitHub.

## Quick Reference

### Essential Git Commands

```bash
# Setup
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Basic Operations
git init                    # Initialize a new repository
git clone <url>            # Clone a repository
git status                 # Check repository status
git add <file>             # Stage changes
git commit -m "message"    # Commit changes
git push                   # Push to remote
git pull                   # Pull from remote

# Branching
git branch                 # List branches
git branch <name>          # Create branch
git checkout <name>        # Switch branch
git checkout -b <name>     # Create and switch
git merge <branch>         # Merge branch
git branch -d <name>       # Delete branch

# Viewing History
git log                    # View commit history
git log --oneline          # Compact view
git show <commit>          # Show commit details
git diff                   # Show changes

# Undoing Changes
git revert <commit>        # Revert a commit
git reset --soft <commit>  # Soft reset
git reset --hard <commit>  # Hard reset (careful!)
git stash                  # Stash changes
git stash pop              # Apply stashed changes
```

## Learning Resources

### Official Documentation
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/)
- [GitHub Learning Lab](https://lab.github.com/)

### Interactive Tutorials
- [Learn Git Branching](https://learngitbranching.js.org/)
- [Git Immersion](https://gitimmersion.com/)
- [Codecademy Git Course](https://www.codecademy.com/learn/learn-git)

### Video Tutorials
- [Git and GitHub for Beginners](https://www.youtube.com/watch?v=RGOj5yH7evk)
- [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials)

### Cheat Sheets
- [Git Cheat Sheet by GitHub](https://training.github.com/)
- [Git Cheat Sheet by Atlassian](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

## Best Practices

### Commit Messages
- One of the four categories of commits:
- 1. doc: Used when you make any commits in documentation
- 2. feat: When your code make changes to any features
- 3. chore: When you perform some restructuring or other works
- 4. fix: Debugging code
- Use clear, descriptive messages 
- Start with a verb in present tense ("Add feature" not "Added feature")
- Keep the first line under 50 characters
- Add detailed explanation after a blank line if needed

Example:
```
Add user authentication feature

- Implemented login/logout functionality
- Added password hashing with bcrypt
- Created session management
```

### Branch Naming
- `feature/description` - for new features
- `fix/description` - for bug fixes
- `hotfix/description` - for urgent fixes
- `docs/description` - for documentation
- `refactor/description` - for code refactoring

### Workflow Tips
1. Always pull before starting work
2. Create a new branch for each feature/fix
3. Commit frequently with clear messages
4. Push regularly to avoid losing work
5. Create PRs early for feedback
6. Review your own code before requesting review

## Common Scenarios

### I made a mistake in my last commit
```bash
git commit --amend -m "Correct message"
```

### I want to undo my last commit but keep changes
```bash
git reset --soft HEAD~1
```

### I need to update my branch with latest main
```bash
git checkout main
git pull origin main
git checkout your-branch
git rebase main
```

### I have conflicts during merge/rebase
1. Open the conflicted files
2. Look for `<<<<<<<`, `=======`, `>>>>>>>` markers
3. Edit to resolve conflicts
4. `git add <file>` to mark as resolved
5. Continue with `git merge --continue` or `git rebase --continue`

---

**Need Help?** Ask in the team chat or tag someone for review!
