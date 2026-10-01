# git-practice

A sandbox repo for practicing the basic git workflow: clone, change, commit, push.

## Your task

1. **Clone** the repo (once):
   ```bash
   git clone git@github.com:GreshamLab/git-practice.git
   cd git-practice
   ```
2. **Set your identity** (once per machine, if you haven't already):
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@nyu.edu"
   ```
3. **Make a change**: create a file named after yourself in `people/`:
   ```bash
   cp people/TEMPLATE.md people/yourname.md
   # edit people/yourname.md with any editor
   ```
4. **Commit** it:
   ```bash
   git add people/yourname.md
   git commit -m "Add yourname"
   ```
5. **Push** it:
   ```bash
   git pull --rebase   # pick up everyone else's changes first
   git push
   ```

If `git push` is rejected with "fetch first" or "non-fast-forward", someone pushed
before you. Run `git pull --rebase` and then `git push` again.

## Bonus: a merge conflict

Once everyone has pushed, add one line to the bottom of `guestbook.md`, then commit and push.
Since everyone is editing the same spot, most people will get a conflict. To fix one:
open the file, keep everyone's lines, delete the `<<<<<<<`, `=======`, `>>>>>>>` markers, then:
```bash
git add guestbook.md
git rebase --continue
git push
```
