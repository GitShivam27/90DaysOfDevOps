### Github-hoted-Runner
**Task 1**
Multiple-os and printed: OS, hostname and user

```
name: Multi-OS Info Workflow

on: [push, workflow_dispatch]

jobs:
  build:
    runs-on: ${{ matrix.os }}
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest, macos-latest]
    steps:
    - name: Print OS, Hostname, and User
      run: |
        # Commands for Linux and macOS runners
        if [ "$RUNNER_OS" == "Linux" ] || [ "$RUNNER_OS" == "macOS" ]; then
          echo "OS: $RUNNER_OS"
          echo "Hostname: $(hostname)"
          echo "User: $(whoami)"
          
        # Commands for Windows runners (using PowerShell)
        elif [ "$RUNNER_OS" == "Windows" ]; then
          echo "OS: $env:RUNNER_OS"
          echo "Hostname: $env:COMPUTERNAME"
          echo "User: $env:USERNAME"
        fi
      shell: bash
```
<img width="1024" height="768" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/ab0d1d2b-c988-4d52-8738-23ee932b8f50" />
