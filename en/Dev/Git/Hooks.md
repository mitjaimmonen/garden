---
Planted: 2025-02-16
Tended: 2025-02-16
---
# Hooks

*Planted: `= this.Planted`*
*Tended: `= this.Tended`*

---

### Set git hooks path to include hooks in source control

Place new hooks in folder ".git-hooks" and run the following:
`git config core.hooksPath .git-hooks


#### Background

In one of our game projects we have all game contents defined in dozens, maybe hundreds of json files. There are some strict requirements about their format and how they should link their data to each other.

We edit the game data without separate editors, instead just editing the json contents in a text editor, it is error prone. So currently the solution is to run a pre-commit hook that validates the json data before allowing it to be pushed to the repository at all.

The approach is also more straight forward as opposed to having some separate tests getting triggered on pull requests. We do a little corner cutting.