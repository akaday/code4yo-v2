# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

## Rebasing Code

### Steps to Rebase onto the `main` Branch

1. Ensure that you have committed or stashed any changes in your current branch.
2. Run `git fetch` to update your local repository with the latest changes from the remote repository.
3. Switch to the branch you want to rebase by running `git checkout <your-branch>`.
4. Start the rebase process by running `git rebase main`.
5. If any conflicts occur during the rebase, Git will pause and notify you about the conflicting files. Resolve the conflicts manually by editing the files and removing the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
6. After resolving the conflicts, stage the changes by running `git add <file>`.
7. Continue the rebase process by running `git rebase --continue`.
8. Repeat the conflict resolution process for any additional conflicts that may arise.
9. Once the rebase is complete, force push the rebased branch to the remote repository by running `git push --force-with-lease`.

### Advanced Git Rebase Techniques

#### Interactive Rebase

Interactive rebase allows you to edit, reorder, squash, or drop commits during the rebase process. This can help you clean up your commit history and make it more readable.

* Start the interactive rebase process by running `git rebase -i <base-branch>`.
* A text editor will open, displaying a list of commits. Each commit is prefixed with a command (e.g., `pick`).
* Modify the commands to perform actions such as reordering, squashing, or dropping commits. Save and close the editor.
* Git will apply the changes and prompt you to resolve any conflicts that arise.

#### Rebase with Autosquash

Autosquash is a feature that helps you automatically squash fixup commits into their corresponding base commits during a rebase.

* Start the rebase process with the `--autosquash` option by running `git rebase -i --autosquash <base-branch>`.
* Git will automatically reorder and mark fixup commits for squashing.
* Review the changes in the text editor, make any necessary adjustments, and save the file.
* Git will apply the changes and prompt you to resolve any conflicts that arise.

#### Rebase with Preserve Merges

Preserve merges is a feature that allows you to rebase a branch while preserving merge commits. This can be useful when you want to maintain the context of merges in your commit history.

* Start the rebase process with the `--preserve-merges` option by running `git rebase --preserve-merges <base-branch>`.
* Git will reapply the commits while preserving the merge commits.
* Resolve any conflicts that arise during the rebase process.

### Precautions Before Force Pushing After a Rebase

Before force pushing after a rebase, take the following precautions:

* Ensure that you have resolved all conflicts during the rebase process and that your branch is in a clean state.
* Verify that your branch is up-to-date with the latest changes from the remote repository by running `git fetch` and `git pull`.
* Double-check the commit history to ensure that the rebase has been performed correctly and that there are no unintended changes.
* Communicate with your team members to inform them about the force push and ensure that they are aware of the changes.
* Use the `--force-with-lease` option when force pushing to ensure that you do not accidentally overwrite any changes made by others. This option checks if the remote branch has been updated since you last fetched it and prevents the force push if there are new changes.

### Handling Conflicts During Rebasing

To handle conflicts during rebasing, follow these steps:

1. When Git notifies you about a conflict, open the conflicting file(s) and look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
2. Manually edit the file(s) to resolve the conflicts by choosing the correct code from each section or combining the changes as needed.
3. Remove the conflict markers after resolving the conflicts.
4. Stage the resolved file(s) by running `git add <file>`.
5. Continue the rebase process by running `git rebase --continue`.
6. Repeat the conflict resolution process for any additional conflicts that may arise.
7. Once the rebase is complete, verify that the code works as expected and run tests if applicable.
8. Force push the rebased branch to the remote repository by running `git push --force-with-lease`.
