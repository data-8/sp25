# DATA 8 Spring 2025

Managed by Spring 2025 #TeamContent: 
* Leads: Ella DeGuzman and Brandon Su
* Members: TBD

[![Pages Deployment](https://github.com/data-8/sp25/actions/workflows/jekyll.yml/badge.svg)](https://github.com/data-8/sp25/actions/workflows/jekyll.yml) •
[![a11y specs](https://github.com/data-8/sp25/actions/workflows/rspec.yml/badge.svg)](https://github.com/data-8/sp25/actions/workflows/rspec.yml)

The https://www.data8.org/sp25/ website.

## Installation

Prerequisites:

- You have everything that [Jekyll requires](https://jekyllrb.com/docs/installation/)
- You have installed [Bundler](https://bundler.io/): Run `gem install jekyll bundler`

1. [Fork](https://github.com/berkeley-eecs/berkeley-class-site/fork) the repository.
2. Clone your fork (replace `YOUR_GITHUB_USERNAME` and `YOUR_REPO` accordingly).
```
git clone git@github.com:YOUR_GITHUB_USERNAME/YOUR_REPO.git
```
3. Install dependencies:
```
cd sp25
bundle install
```

## Usage

To run the site locally, run:

```
bundle exec jekyll serve
```

Search throughout the repository for TODO items called `TODO(setup)` and complete them to customize the site for your course.

## Deployment

The easiest way to deploy your site is with [GitHub Pages](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll).

## License

[MIT](LICENSE)
