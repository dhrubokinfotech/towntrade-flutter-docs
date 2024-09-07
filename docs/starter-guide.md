# Starter Guide

## Introduction to Flutter

Flutter is Google's UI toolkit for building beautiful, natively compiled applications for **MOBILE**, **WEB**, and **DESKTOP** from a single codebase. It’s easy to learn and has been gaining increasing popularity. With this guide, you will learn the basics of Flutter and will be able to create a simple application using this technology.

[Click here](https://flutter.dev) to learn more about Flutter.

## Tools & Setup

### Prerequisites

- **Flutter & Dart SDK** (Flutter version 3.22.2 is recommended)
- **An IDE** (Android Studio recommended, Visual Studio Code, or IntelliJ IDEA)

To edit this project, ensure that Flutter and Dart are installed and configured successfully on your machine.

1. Set up your editor - Install the Flutter and Dart plugins.
2. If you have the Android SDK installed and configured, follow the steps below to install Flutter.

[Complete Flutter installation guide](https://flutter.dev/docs/get-started/install/)

## Android Studio – Windows Setup

Here we'll know how to install Android Studio in a Windows machine.

- [Download Android Studio](https://developer.android.com/studio/)
- [Get the Flutter SDK](https://flutter.dev/docs/get-started/install)
- [Learn more about Android Studio](https://developer.android.com/studio/intro/)

### Step 1: Get the Flutter SDK

1. Download the installation bundle for the latest stable Flutter release.
2. Extract the `.zip` file and place the `flutter` folder in your desired installation location (e.g., `C:\src\flutter`). Avoid directories that require elevated privileges, like `C:\Program Files\`.

### Step 2: Update your PATH

To run Flutter commands from the regular Windows console:

1. Search for "env" and select **Edit environment variables**.
2. Under **User variables**, check if there's an entry for `Path`.
    - If it exists, append the full path to `flutter\bin` using `;` as a separator.
    - If not, create a new user variable named `Path` with the full path to `flutter\bin`.
3. Close and reopen any existing console windows to apply the changes.

### Step 3: Run `flutter doctor`

From a console window with the Flutter directory in your PATH, run:

```bash
c:\src\flutter>flutter doctor
```

This command checks for any platform dependencies you need to resolve. [Learn more](https://flutter.dev/docs/get-started/editor).

## Android Studio – macOS Setup

### Download and Install Required Software

- [Download Android Studio](https://developer.android.com/studio)
- [Download Xcode](https://apps.apple.com/us/app/xcode/id497799835?mt=12)
- [Get the Flutter SDK](https://flutter.dev/docs/get-started/install)

### Step 1: Get the Flutter SDK

1. Download and extract the installation bundle to get the latest Flutter SDK.
2. Move the extracted `flutter` folder to your desired location (e.g., `Documents/flutter`).

### Step 2: Update Your PATH

To access Flutter commands from the terminal:

**For the current terminal window:**

```bash
export PATH="$PATH:`pwd`/flutter/bin"
```

## To Set the PATH Permanently on macOS

1. **Open or Create `.bash_profile`**

   Use the following command to open or create the `.bash_profile` file in your home directory:

   ```bash
   sudo open -e $HOME/.bash_profile
  ```
2. **Append the PATH Export Line**
  Add the following line to the bottom of the `.bash_profile` file:

   ```bash
   export PATH="$PATH:[PATH_TO_FLUTTER_GIT_DIRECTORY]/flutter/bin"
  ```
  Replace [PATH_TO_FLUTTER_GIT_DIRECTORY] with the actual path to your Flutter SDK directory
3. **Refresh the PATH Variables**
  Apply the changes by refreshing the PATH variables:

```bash
 source $HOME/.bash_profile
  ```

### Step 3: Verify the Setup `flutter doctor`

Run flutter doctor to ensure that everything is set up correctly and Flutter is properly configured:

```bash
flutter doctor
```

If flutter doctor shows no issues, your setup is complete!

## Android Studio – Linux Setup

### Download and Install Required Software

- **[Download Android Studio](https://developer.android.com/studio)**
- **[Learn more about Android Studio](https://developer.android.com/studio/intro/)**
- **[Get the Flutter SDK](https://flutter.dev/docs/get-started/install/linux)**

## Step 1: Get the Flutter SDK

1. **Download the Flutter SDK**
   - Visit the [Flutter installation page](https://flutter.dev/docs/get-started/install/linux) and download the latest stable release.

2. **Extract the Downloaded File**
   - You can extract the `.tar.xz` file by double-clicking on it, or via terminal:
     ```bash
     tar xf flutter_linux_x.x.x-stable.tar.xz
     ```

3. **Move the Extracted Folder**
   - Move the extracted `flutter` folder to your desired location (e.g., `Documents/flutter`).

## Step 2: Update Your PATH

To access the Flutter command from the terminal, you'll need to update your PATH environment variable. You can choose to update it for the current terminal session only or permanently.

### Option 1: Update PATH for Current Session

To temporarily add Flutter to your PATH:
```bash
export PATH="$PATH:[PATH_TO_FLUTTER_GIT_DIRECTORY]/flutter/bin"
```
This change will only last for the current terminal window.

### Update PATH Permanently for Flutter on Linux

## Option 2: Update PATH Permanently

To ensure Flutter commands are accessible from any terminal session, you need to update the PATH environment variable permanently.

### Open Your Shell Profile

1. Open a terminal.
2. Edit your shell profile file (e.g., `.bashrc`, `.bash_profile`, `.zshrc`) using a text editor. For example, to edit `.bashrc`:
   ```bash
   nano ~/.bashrc
   ```
### Add Flutter to PATH

## Step 1: Add Flutter to PATH

1. **Open Your Shell Profile**
   - Open your shell profile file (e.g., `.bashrc`, `.bash_profile`, `.zshrc`) in a text editor:
     ```bash
     nano ~/.bashrc
     ```

2. **Add Flutter to PATH**
   - Add the following line to the bottom of the file:
     ```bash
     export PATH="$PATH:[PATH_TO_FLUTTER_GIT_DIRECTORY]/flutter/bin"
     ```
     Replace `[PATH_TO_FLUTTER_GIT_DIRECTORY]` with the actual path to your Flutter SDK.

## Step 2: Save the File and Apply the Changes

1. **Save the File**
   - Save the file and exit the editor.

2. **Apply the Changes**
   - Apply the changes by running:
     ```bash
     source ~/.bashrc
     ```

## Step 3: Verify the Setup

1. **Confirm PATH**
   - Check that `flutter/bin` is in your PATH by running:
     ```bash
     echo $PATH
     ```

2. **Verify Flutter Command**
   - Ensure the Flutter command is available by running:
     ``` bash
     flutter --version
     ```

If the `flutter` command runs successfully and displays the Flutter version, your setup is complete!
