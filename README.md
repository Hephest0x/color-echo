# 🌈  Color Echo

Welcome! This repository is a **simple, direct resource** for adding color to your terminal messages in **Bash scripts**. Forget memorizing escape codes—just copy and paste these variables and functions, and you can make your scripts more readable and visually appealing. ✨

## 🎨 Usage

To start using these colors, simply copy the code block below and paste it at the beginning of your Bash script.
```Bash

# ------COLORS---------

C_RESET='\033[0m'
C_RED='\033[0;31m'
C_GREEN='\033[0;32m'
C_YELLOW='\033[0;33m'
C_BLUE='\033[0;34m'
C_CYAN='\033[0;36m'

echo_info() { echo -e "${C_BLUE}$1${C_RESET}" }
echo_warn() { echo -e "${C_YELLOW}$1${C_RESET}" }
echo_error() { echo -e "${C_RED}$1${C_RESET}" }
echo_success() { echo -e "${C_GREEN}$1${C_RESET}" }
# --------------------------------------------------
```

## 📜 Available Functions

The repository includes the following functions, designed for specific message types:

    echo_info(): For informational messages, uses the blue color. Useful for showing progress details of a script.

    echo_warn(): For warnings, uses the yellow color. Ideal for notifying the user about situations that require attention but aren't critical errors.

    echo_error(): For error messages, uses the red color. Useful for signaling failures or problems that halt execution.

    echo_success(): For success notifications, uses the green color. Perfect for confirming that an operation has completed successfully.

## ✍️ Example

Here's an example of how to use these functions in your script:
```Bash

#!/bin/bash

# Make sure you've copied the color block here.

echo_info "Starting the operation..."
# Simulate a successful task
sleep 1
echo_success "Operation completed successfully!"

# Simulate a warning
echo_warn "Warning: Some files could not be processed."

# Simulate an error
echo_error "Error: Configuration file not found."
```

When you run this script, you'll see the messages in their corresponding colors, making it easy to quickly identify their purpose.

## 💡 How It Works

Behind the scenes, this script uses ANSI escape codes to change the color of the text in your terminal. Each variable, like C_RED, contains a special sequence of characters that tells the terminal to switch the color to red. The C_RESET variable is crucial as it resets the color to the terminal's default, preventing the rest of your text from staying the same color. The echo_* functions combine these escape codes with the message you provide, creating a colorful output that automatically resets.

Feel free to use these resources to bring your scripts to life. Feel free to modify...
