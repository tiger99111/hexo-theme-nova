
## Introduction ##

The nova is a [hexo](https://hexo.io) theme using swig template aimed to build your github project site conveniently.

The theme provided three layouts to demonstrate the page.

 1. `post` for blog
 2. `project` for github project
 3. `page` for other pages

Nova also provided lots of helper scripts as plugins to co-work with the theme, e.g. donate, toc, project side bar. 
Welcome to visit [My blog](http://ieclipse.cn) (http://ieclipse.cn) to see the demo.

## layouts ##
### post
Similar to most hexo theme, nova has index, archive, widgets layout. The difference is nova rewrite archive list helpers and provided two paginator helpers.

### project
Project layout is aimed to demonstrate the github projects info. For project layout, a `gh` front-maker is nessary in your page.

- gh.user the github user, default is the user in theme <var>_config.yml</var>
- gh.repo the github repo, default is fetched from url
- gh.type 
    - get_repos get repositories from github
    - get_contents get markdown file under repository
    - get_releases get releases under repository

The projects sidebar is configurated in <var>_data</var>/<var>projects.yml</var>

### page
A `type` front-maker is used to mark special pages.

- categories: Categories page
- donates: Donate list page

### other
- comment: Page comment, default is uyan comment
- toc: Table of contents suffix
- share: Baidu share component
- analytics: Baidu analytics component
- donate: page donate component

## Config
First, change site <var>_config.yml</var> set `theme: nova` to use the theme

### js_css
Add global js and css sample:
```yml
js_css:
- url: css/nova.css
- url: js/script.js
```
### menu
Configurate the site menus
```yml
menu:
- name: home
  url: /
- name: project
  url: /p/
- name: category
  url: /categories/
- name: archive
  url: /archives/
- name: about
  url: /about/
- name: donate
  url: /donate/
```
**the <var>name</var> will be translated.**
### gh
Github info.
```yml
# github
gh:
  user: Jamling
  # Keep private to others
  token:
  repos: 
    - Android-ORM
    - QuickAF
    - adt-extensions
    - eclipse-explorer
    - hexo-theme-nova
    - jarsigner
```

## helpers

Please see [nova helpers](https://github.com/Jamling/hexo-theme-nova/blob/master/helpers.md)