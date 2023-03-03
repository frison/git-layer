# git-layer
Layering another git repository ontop of your repository. Like a git sub-tree to the root.


# `git-layer <git url> <relative path>`


## Layer Repository

A layer repository is any git repository that you want to layer ontop of your repository. This is useful for when you want to have a repository that is shared between multiple projects without the complexities of `git submodule` or the limitations of `git subtree`.

Because a layer repositories usage is opaque to the user, it's important to comment the files appropriately -- for example, including the version of the file in the file itself and/or advising users against manual edits.


## Example

```bash
git-layer
