# git-layer

Layer a git repository on top of your directory. Like a `git sub-tree` to your current directory, without the complexity. This can also be thought of as a fancy version of `cp -r git@github.com:frison/git-layer.git/* .` but that obviously doesn't work.


# `git-layer <repository> <path>`

Copy all of the files from the git repository at `<repository>` into the `<path>`.

# `git-layer --apply`

Apply all layers from all `.gitlayer` files in the current and all child directories.

## `.gitlayer`

A file with line separated `<repostory> <path>` parameters for `git-layer`. Useful for record-keeping and updating existing git-layers.

## Layer Repository

A layer repository is any git repository that you want to layer ontop of your directory (or repository). This is useful for when you have scripts, tools, shared configuration, or anything else that is shared between multiple projects without the complexities of `git submodule` or the limitations of `git subtree`.

Because a layer repository's usage is opaque to the user, it's important to comment the files appropriately -- for example, including the version of the file in the file itself and/or advising users against manual edits.

### `.gitlayer.ignore` file

The `.gitlayer.ignore` file is a special file that is used to ignore files when a layer repository is copied. This is useful for when you want to ignore files that are relevant to the layer repository (for example, a README.md file) but not relevant to where the layer repository is copied into.

## Example

```bash
git-layer git@github.com:frison/git-layer.git .
```
