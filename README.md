# git-layer

Layer a git repository on top of your directory. Like a `git sub-tree` to to your current directory, without the complexity. This can also be thought of as a fancy version of `cp -r git@github.com:frison/git-layer.git/* .` but that obviously doesn't work.


# `git-layer <git url> <relative path>`

Copy all of the files from the git repository at `<git url>` into the `<relative path>` of the current directory.

## Layer Repository

A layer repository is any git repository that you want to layer ontop of your repository. This is useful for when you want to have a repository that is shared between multiple projects without the complexities of `git submodule` or the limitations of `git subtree`.

Because a layer repositories usage is opaque to the user, it's important to comment the files appropriately -- for example, including the version of the file in the file itself and/or advising users against manual edits.

### `.gitignore.layer` file

The `.gitignore.layer` file is a special file that is used to ignore files when a layer repository is copied. This is useful for when you want to ignore files that are relevant to the layer repository (for example, a README.md file) but not relevant to the current repository.

## Example

```bash
git-layer
