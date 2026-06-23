Commit and push the current changes to deploy the website.

Follow these steps exactly:

1. Run `git status` to see what files have changed
2. Run `git diff index.html` to read the actual changes made
3. Based on the diff, write a clear commit message in the format: `<type>: <what changed>`
   - Types: `update`, `fix`, `add`, `remove`, `style`
   - Examples: `update: hero headline copy`, `fix: contact email address`, `add: fourth service card`
4. Run `git add index.html`
5. Run `git commit -m "<your message>"`
6. Run `git push origin main`
7. Confirm the push succeeded
8. Tell the user: "Deployed. GitHub Actions will have the site live at https://dhanuka-inc.github.io in about 30 seconds."

If `git status` shows nothing to commit, tell the user there are no changes to deploy.
If the push fails, show the error and suggest the user check their GitHub credentials.
