

# 39


# 40


# 41 - Scripts and File Paths
`./` does not mean "execute a script". It is file path syntax pointing to your current working directory.

Output will write to the current working directory of the user running  script. Make sure to place your output properly using file paths.
- Do you care where the user is running a certain script from?

# 42 - Scripting and Root Permissions
What if you want to create a script that outputs a file(s) with particular ownership / permissions?
- owned by root?
- owned by another user / group?

When using a redirect operator, it essentially spawns a sub-shell in the background to do the writing of the information (output). This sub-sell will have the permissions of who you're logged in as - NOT the permissions used when executing the command itself. In other words, `sudo` won't allow you to redirect output to a file with root-only write permissions. `sudo` only applies to the initial command it prefixes, and not the write process(es) spawned by the redirect operators.

HOWEVER... If you script out the corresponding command and then execute that script as root, it will work correctly.

## Commands

### `tee`
Can write data to files. Good alternative to redirect operators when permissions are an issue

`echo sandbox | sudo tee file.txt`


# 43 - Scripted IP Changer Low Sophistication
