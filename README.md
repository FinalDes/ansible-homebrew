# Homebrew Ansible Role

This role installs Homebrew on macOS and Linux in non-interactive mode.

## Requirements
- Ansible >= 2.9
- macOS >= 14.0 or Linux with glibc >= 2.13, Ruby >= 3.4, curl >= 7.41.0, git >= 2.7.0
- Sudo access for macOS (non-interactive, e.g., cached credentials or passwordless sudo)
- `POSIXLY_CORRECT` environment variable must be unset

## Role Variables
- `homebrew_brew_git_remote`: Hardcoded to `https://github.com/Homebrew/brew`
- `homebrew_core_git_remote`: Hardcoded to `https://github.com/Homebrew/homebrew-core`

## Example Playbook
```yaml
- hosts: localhost
  roles:
    - role: homebrew