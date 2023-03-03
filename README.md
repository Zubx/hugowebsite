# Hugo Theme Bootstrap Skeleton

The starter template for [Hugo Bootstrap Theme](https://github.com/razonyang/hugo-theme-bootstrap) that install the theme as a Hugo module.

## Demo

| Platform | URL |
|---|---|
| Netlify | https://hbs-skeleton.netlify.app/ |
| GitHub Pages | https://projects.razonyang.com/hugo-theme-bootstrap-skeleton/ |
| Cloudflare Pages | https://hbs-skeleton.pages.dev/ |
| Docker image | See also [Dockerfile](Dockerfile) |

@Zub i am using Netlify here

## Usage

Please make sure you have install the [build tools](https://hbs.razonyang.com/v1/en/docs/getting-started/prerequisites/#build-tools) prior to using this template.

**1. Clone this repository**

It's recommending cloning the repo by clicking the `Use this template` button, if you're hosting your code on GitHub.
@Zub : this is a must. i do it 03/03/2023

**2. Modify the `go.mod`**

Replace the following line to yours, such as `module github.com/user/repo`.

```text
module github.com/razonyang/hugo-theme-bootstrap-skeleton
```

**3. Commit and push changes to your repository**

```shell
$ git add -A
$ git commit -m 'First commit'
$ git remote set-url origin github.com/user/repo
$ git push origin main
```


## Server

**1. Install dependencies**

```shell
$ npm i
```

Generally, this step only needs to be performed once for each local project.

**2. Start server**

```shell
$ hugo server
```

## Upgrade theme

```shell
$ hugo mod get github.com/razonyang/hugo-theme-bootstrap@master
$ hugo mod npm pack
$ npm update
$ git add go.mod go.sum package.json package-lock.json
$ git commit -m 'Update the theme'
```

You can also replace the `master` with stable [releases](https://github.com/razonyang/hugo-theme-bootstrap/releases).

## Deployment

> The `baseURL` is very important, the CSS, JS and Sitemap require it to be set.

**Please make sure you've change the `baseURL` on `config/production/config.yaml` before deploying your site.**

**Please also remove the `-b {url}` from the following files if you're using this template.**

- `.github/workflows/gh-pages.yml`

This template supports GitHub Pages, Docker image, Netlify out-of-box. See also [Deployment](https://hbs.razonyang.com/v1/en/docs/deployment/) for getting more detail.

The following parameters also need to be tweaked.

- Replace the `utterances.repo` with your own to get notified when someone comments.
- Modify the `repo` to your own, or delete it if it's unused.
- `contact.endpoint`.

There are some hooks under the `layouts/partials/hooks` folder for showing how to use them, please feel free to delete them.

## Documentations

- [English](https://hbs.razonyang.com/v1/en/)
- [简体中文](https://hbs.razonyang.com/v1/zh-hans/)
- [繁體中文](https://hbs.razonyang.com/v1/zh-hant/)
