# arbatov.me

[![Build Status](https://travis-ci.org/vladzima/arbatovme.svg?branch=gh-pages)](https://travis-ci.org/vladzima/arbatovme)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Personal website on [Jekyll](https://jekyllrb.com]), hosted on Github Pages on `gh-pages` branch.

Uses [Commitizen](https://github.com/commitizen/cz-cli) for conventional changelog, [Imperavi Kube UI framework](https://github.com/imperavi/kubeframework) and [InterUI](https://rsms.me/inter/) font.

## Run locally
1) Check whether you have Ruby 2.1.0 or higher installed:

`ruby --version`

2) If you don't have Ruby installed, [install Ruby 2.1.0 or higher](https://www.ruby-lang.org/en/downloads/).

3) Install Bundler:

`gem install bundler`

4) Clone the repository, bundle and run:
```
git clone git@github.com:vladzima/arbatovme.git
cd arbatovme
bundle install
jekyll serve
```

5) If you plan to deploy:
```
npm i commitizen -g && npm i cz-customizable -g
```

## Post link
`rake new_link`

## Delete recent link
`rake delete link`

## Deploy
`bash deploy.sh`

TravisCI build will run automatically and site will be updated on Github Pages.
