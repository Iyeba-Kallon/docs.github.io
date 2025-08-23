# Git & GitHub Guidelines

## Gitflow
We use **Gitflow** as our main workflow. It’s ideal for projects with scheduled release cycles, as it provides a strict branching model to organize development and releases. Gitflow helps manage multiple developers, parallel development, and emergency fixes efficiently.

### Key Branches
- **Main:** Production-ready code. Always stable.
- **Develop:** Integration branch for features. Feature branches are merged here.
- **Staging:** Pre-production branch for testing and final integration before release.

### Feature Branches
- Each new feature gets its own branch.
- Branch off **Staging**, merge back into **Staging** once complete.
- Naming: `feature/<developer-name>/<feature-name>`  
  Example: `feature/Iyeba/new-login-form`

### Hotfix Branches
- Emergency fixes to production.
- Branch off **Main**, merge into **Main** and **Develop**.
- Naming: `fix/<developer-name>/<fix-name>`  
  Example: `fix/Iyeba/login-bug`

### Release Branches
- Prepare for a new production release.
- Branch off **Develop**, merge into **Main** once ready.
- Naming: `release/<release-name>`  
  Example: `release/1.2.0`

### Benefits of Gitflow
- **Parallel Development:** Multiple developers can work on separate features without conflict.
- **Collaboration:** Feature branches act as sandboxes; easy to track contributions.
- **Staging for Releases:** Merges are tested before production.
- **Hotfix Support:** Emergency changes don’t interfere with ongoing development.

**Sources:**  
- [Gitflow Introduction](https://datasift.github.io/gitflow/IntroducingGitFlow.html)  
- [Atlassian Gitflow Tutorial](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

## Commit Messages
Commit messages are crucial for clarity. Follow these rules:

1. Specify the type of commit:
   - `feat/add:` new feature
   - `fix:` bug fix
   - `style:` styling changes
   - `refactor:` code refactoring
   - `test:` testing updates
   - `docs:` documentation updates
   - `chore:` maintenance
2. Separate subject and body with a blank line.
3. No whitespace errors or unnecessary punctuation.
4. Capitalize the subject line; use imperative mood.
5. Body should explain **what** changed and **why**.

**Examples:**
- `Add: Implement user authentication API`
- `Fix: Correct validation bug in signup form`
- `Docs: Update README with setup instructions`

**Further Reading:**  
- [Writing Good Commit Messages](https://www.freecodecamp.org/news/writing-good-commit-messages-a-practical-guide/)  
- [Gist Guide](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53)
