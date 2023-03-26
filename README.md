# install-playwright
install playwright on rpm linux distros

## Download latest version of VSCode
- https://code.visualstudio.com/download
- copy .rpm to `roles/playwright/files`

## Download latest version of VSCode Playwright extension
- https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright
- copy .vsix to `roles/playwright/files`

## Run the role to install Playwright
`sudo ansible-playbook playbooks/install-playwright.yml -i inventory.yml -k -K --ask-vault-pass`