# remix-sandbox

This project is initiated to simply remove the hassle of setting up a sandbox on Codesandbox container sandbox or Stackblitz WebContainer running Remix.

* Codesandbox - https://codesandbox.io/s/github/edmundhung/remix-sandbox
* Stackblitz - https://stackblitz.com/github/edmundhung/remix-sandbox

All the templates are bootstrapped using `npm init remix` with typescript setup and using Remix App Server as the deployment target at the moment.

## Specifying remix version

We published each template using the remix version as the branch name. The supported versions are listed here: [List all branches](https://github.com/edmundhung/remix-sandbox/branches/all)

If you would like to kickstart a sandbox with a specific remix version, you can specify it as follow:

- Codesandbox - `https://codesandbox.io/s/github/edmundhung/remix-sandbox/:version`
- Stackblitz WebContainer - `https://stackblitz.com/github/edmundhung/remix-sandbox/tree/:version`

## Required setup

> This setup is required only for versions before v1 as everything is now published to NPM and available to everyone

As most of the remix packages are served from a private NPM registry. Codesandbox cannot install the required packages without your `REMIX_TOKEN`. Here is how you can set it up:

1. Look for the **server control panel** on the left sidebar. If you couldn't find it, you are properly not looking at your own sandbox. Fork it first.
2. On the **Server Control Panel**, look for the **Secret Keys** section. Add a new secret with the name `REMIX_TOKEN` and put your license on the value field. Submit it by clicking **Add Secret**.
3. On the **Terminal** view, add a new terminal by clicking `+`. Type `npm ci` or `npm install` and close the terminal when the installation complete
4. Finally, back to the **Server Control Panel**, look for the **Control Container** section. Click `Restart Server`. Wait for the terminal to kickstart the dev server again. Refresh the browser view and you should see Remix running!

## FAQ

### 1. The terminal view is showing `/bin/sh: 1: remix: not found`

Please check the [Required setup](#required-setup) for details.

### 2. The browser view is showing `502: Bad Gateway`

This usually happens when the dev server fails to start. Please make sure you follow the steps listed on the [Required setup](#required-setup) and restart the server afterwards.
