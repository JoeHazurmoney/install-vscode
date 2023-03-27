# install-vscode
ansible role to install vscode and any desired extensions on air-gapped rpm linux distros

## Download latest version of VSCode and any desired VSCode extensions
- Download VSCode rpm from: https://code.visualstudio.com/download
- copy .rpm to `roles/vscode/files`

- Download desired extensions from https://marketplace.visualstudio.com/
  - e.g. Playwright extension from: https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright
- copy extension .vsix files to `roles/vscode/files`
- update `extension_vars.yml` with names of .vsix files

- symlink the role to /etc/ansible/roles or copy the role to /etc/ansible/roles
  - `sudo ln -s /home/<user>/github/install-vscode/roles/vscode /etc/ansible/roles`

- run playbook
  - `ansible-playbook playbooks/install-vscode.yml -i inventory.yml -k -K -tag install-vscode`


## Run the role to install VSCode and extensions
`ansible-playbook playbooks/install-vscode.yml -i inventory.yml -k -K --tags install`
