----
List of items needing a markup:
- [x] Shell command inline, in sentence or paragraph.
- [x] Shell commands in a block
- [x] Filename, local filesystem or on GitHub
- [x] Repo name on GitHub or in local git
- [x] UI element (button, text link, etc.)
- [ ] ???
----
# Op1st Technical Markup Style guide

Use this style guide when you are writing content using MarkDown.
This creates a consistent look and feel across the project content.

The consistent look and feel helps readers feel confident about the content they are learning from.

There is an additional benefit, which is the MarkDown source will be consistent for markup and technical terms.
This helps greatly when it comes to editing, where the markup can create errors or distract from errors.
Having use for e.g. "`filenames` use backticks" means it is easier to perform automation and programmatic tasks on the content files.

For example, efforts to convert these MarkDown files to other formats may be greatly helped by having the markup provide some context.
That is, if double-undescores `__`

## Quick reference by Markup

| Markup symbols | Name | Typical formatting effect | Used for |
| -------------- | ---- | ------------------------- | -------- |
| \`\`           | Backticks   | `monospace block`  | Inline shell commands, files and special objects |
| \_             | Underscore  | _italicized_       | First use of a new term |
| \_\_           | Double-underscore  | __boldface__ | UI element |
| \*             | Asterisk  | *italicized*         | Reserved |
| \*\*           | Underscore  | **bold**           | Reserved |


## Shell commands

Inline uses backticks without a shell identifier (`$`)
- "After creating a new branch with `git checkout -b name-of-new-branch`, return to the content folder `cd content`."

A block is created by indenting three spaces for each line in the block; do not use backticks.
We use the `$` symbol to make it clear these commands are being done as a normal user.

    ## Check that your clone is configured correctly
    $ git remote -v
    origin    git@github.com:username/community.git (fetch)
    origin    git@github.com:username/community.git (push)
    upstream    https://github.com/operate-first/community.git (fetch)
    upstream    https://github.com/operate-first/community.git (push)
    $ git add name-of-new-file.md
    $ git commit -m "adding file for prototyping" name-of-new-file.md
    $ git push --set-upstream origin name-of-new-branch

## GUI instructions

Whenever you give instructions for a graphical user interface (GUI), it is important to be accurate with spelling and descriptions.
For example, if the GUI has a tab labeled __Getting Started__ don't refer to it inaccurately or incorrectly, such as:
- "When ready click on the get started tab," or,
- "The first step is to click on the __Get-started__ tab."

Both can leave a reader not trusting the accuracy of the documentation.

Element of a GUI, such as a button, tab, or hyperlink, use the double-underline __boldface__:
- "First, click on the __Getting Started__ tab, then the __Your name__ field to fill in your name."
- "Further information can be found under the __Help__ menu."

For a menu tree or series of links, buttons, or other elements to follow, use the single-asterisk and right angle bracket:
- "Configuration for this is found in the __Tools > Options > Settings__ menu."

## Files and special objects

For a file on a filesystem, such as in a git repo locally or on GitHub, use the `backticks`:
- `operate-first/common/blob/main/docs/add_gh_member_and_access.md`
- "When working locally, the `config.yaml` file is located at the top-level of the source directory."
