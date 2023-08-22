# Installation

## Compatibility

- Pug
- Bootstrap 5
- Gulp

Demo: [Octavia Pug Demo](https://octavia-vue.netlify.app/landingpage).

## Manual installation

> :warning: you have to use any type of npm, yarn or gulp command inside "customer-src/build-tools/"

```shell
npm install
```

Or:

```shell
yarn
```

Now to run development server of Octavia run below command:

## Gulp Quick Start

1. Download Octavia latest source files form Themeforst

2. Download and install Node.js from [nodejs.org](https://nodejs.org/en/download/)
   & Git from [git-scm.com](https://git-scm.com/downloads)

3. Open your command prompt or terminal at <code>downloaded_folder/html/build-tools</code>

4. Install the latest version of npm <code>npm install --global npm@latest</code>

5. Install gulp to automate your SCSS and js code compilation. <code>npm install --global gulp</code>

6. Verify the gulp is installed and it's version.<code>gulp -v</code>

7. Install yarn globally. <code>npm install --global yarn</code>

8. Install dependencies. <code>yarn</code>

9. Complile all the assests(SCSS, JS, Images, fonts, icons etc). <code>gulp build --layout1 --prod</code>

<code>--layout1</code> determines the layout and <code>--prod</code> compress and minifies assets.
Assets will be compiled & saved to <code>Octavia/layout[x]/dist/assets</code>

10. Start localhost(Dev Server) and watch file change. <code>gulp --layout1</code>

## Troubleshooting

For jquery missing path issue Error: File not found with singular glob: <code>/build-tools/node_modules/jquery/dist/jquery.min.js</code>

Run

## For common npm issues

- Re-install dependencies: <code>rm -Rf node_modules && npm install</code>
- Run <code>gulp --layout1</code>
- If this did not work, try running <code>npm cache clean</code> and repeat the above step
