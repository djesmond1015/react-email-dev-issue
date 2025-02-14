## React Email Build Fails on Ubuntu 24.04 but Works on Windows  
When running `email dev` in a newly created **React Email Starter** project, the build fails with errors while rendering email templates. The same setup **works fine on Windows 11** with the same versions of PNPM (`10.4.0`) and Node.js (`23.5.0`).  


![Image](https://github.com/user-attachments/assets/89533c19-8aac-4a66-a3f8-3b31ff9a2b60)

## System Information  

```sh
❯ pnpm -v && node -v
10.4.0
v23.5.0

❯ cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
```

## Run Create Email Command & Install Package

```sh
❯ pnpm create email && cd react-email-starter && pnpm install && pnpm dev
✔ React Email Starter files ready  
react-email-starter
├── emails
│   ├── static
│   │   ├── notion-logo.png
│   │   ├── plaid-logo.png
│   │   ├── plaid.png
│   │   ├── stripe-logo.png
│   │   ├── vercel-arrow.png
│   │   ├── vercel-logo.png
│   │   ├── vercel-team.png
│   │   └── vercel-user.png
│   ├── notion-magic-link.tsx
│   ├── plaid-verify-identity.tsx
│   ├── stripe-welcome.tsx
│   └── vercel-invite-user.tsx
├── package.json
└── readme.md

Packages: +198
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Progress: resolved 243, reused 199, downloaded 0, added 198, done

dependencies:
+ @react-email/components 0.0.33
+ react 19.0.0
+ react-dom 19.0.0

devDependencies:
+ @types/react 19.0.1 (19.0.8 is available)
+ @types/react-dom 19.0.1 (19.0.3 is available)
+ react-email 3.0.7
```

## Run Email Dev

```sh
> react-email-starter@0.1.9 dev /home/desmond/project/react-email-starter
> email dev

    React Email 3.0.7
    Running preview at:          http://localhost:3000

  ✔ Ready in 0.4s

  ✖ Failed while rendering notion-magic-link.tsx
  ✖ Failed while rendering notion-magic-link.tsx
  ✖ Failed while rendering plaid-verify-identity.tsx
  ✖ Failed while rendering stripe-welcome.tsx
  ✖ Failed while rendering vercel-invite-user.tsx
```
