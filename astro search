Hey everyone!I've got a super useful command-line tool to share that makes searching for code in any project a breeze. It's a custom function that uses ripgrep (a really fast search tool) to find exact strings of text. No more fighting with special characters or regex when you just want to find a specific line of code!

Here’s how to set it up.

Step 1: You Need ripgrep
First, you need to install ripgrep if you don't have it already. It's probably in your favorite package manager.

  
- On macOS (using Homebrew):
    brew install ripgrep
  
- On Debian/Ubuntu (using apt):
    sudo apt-get install ripgrep

Step 2: Create a .bash_functions File
We'll keep our main ~/.bashrc file clean by putting our new function in its own file.

Run this command to create a new file called .bash_functions in your home directory:

touch ~/.bash_functions


Step 3: Add the ripgrep Function and Alias
Open the new ~/.bash_functions file with your favorite text editor (like nano, vim, or VS Code) and paste the entire block of code below into it.

This creates the function and a handy, short alias _rg to call it.

#!/bin/bash

# ==============================================================================
# ripgrep (function): Find a fixed string recursively in files.
#
# Description:
#   This function serves as a user-friendly wrapper around `rg` to search
#   for an exact, literal string in the current directory and all
#   subdirectories. It automatically includes line numbers and handles search
#   terms that contain special characters without treating them as regex.
#
# Usage:
#   ripgrep "search term"
#   _rg "search term"
# ==============================================================================
ripgrep() {
  # Check if ripgrep (rg) is installed
  if ! command -v rg &> /dev/null; then
    echo "Error: 'ripgrep' (rg) is not installed or not in your PATH." >&2
    return 1
  fi

  # Check if a search term was provided
  if [ -z "$1" ]; then
    echo "Usage: _rg \"<search term>\"" >&2
    return 1
  fi

  # Execute the search for a fixed, literal string
  rg --line-number --fixed-strings -- "$1"
}

# Create a short alias for the function
alias _rg='ripgrep'


Step 4: Connect it to Your Shell
Now, we need to tell your main shell configuration file (.bashrc) to load the functions from our new file.

Open ~/.bashrc and add these lines to the end of the file. This checks if your .bash_functions file exists and, if it does, it loads it.

# Load custom functions if the file exists
if [ -f ~/.bash_functions ]; then
  . ~/.bash_functions
fi


Step 5: Reload Your Terminal
Your changes won't apply until you reload your shell's configuration. You can either open a brand new terminal window or run this command:

source ~/.bashrc


Step 6: Use Your New Command!
That's it! You're all set. Navigate to any project folder and try it out using the short _rg alias.

Example:
To find every instance of the exact string .eq('id', id), just run:

_rg ".eq('id', id)"


You'll get a clean list of every file and line number where that string appears. Enjoy! 
