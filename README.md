# repo

A simple Vue 2.0 web page, providing CoderBot images and update packages details and download links. The website is live at [coderbot.org/repo](http://www.coderbot.org/repo/index.html).

Uses [Element]() as UI library, [Axios]().

The development is done on the `dev` branch, since `master` is hosting the production build, served by GitHub pages (automatically deployed by an npm script, see `package.json`).

### Deploy

``` bash
# Clone the repo
git clone https://github.com/coderbotorg/repo

# cd into the folder
cd repo

# Install dependencies
npm install

# Serve with hot reload at localhost:8010
npm run dev

# Build for production with minification
npm run build

# Deploy on GitHub pages
npm run deploy
```
