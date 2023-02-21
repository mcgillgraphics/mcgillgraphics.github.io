# Lab Website

This is the main Jekyll code for building the lab website using [Jekyll](https://jekyllrb.com/).

## Installation

This website relies on [Jekyll](https://jekyllrb.com/), which is a [Ruby Gem](https://rubygems.org/) that can be installed on most systems. Instructions on how to install the system can be found on the [official website](https://jekyllrb.com/docs/installation/). 

In general, it is relatively straightforward to install Jekyll on most machines. However, for newer Mac machines running on Apple Silicon, some issues can arise due to clashes in Ruby environments. If you run into these issues, have a look at [Ruby on Mac](https://www.rubyonmac.dev/). We have purchased a version of this that can be shared between administrators; just [email us](mailto:joey.litalien@mail.mcgill.ca) for the installer.

## Build Instructions

Once installed, locally run:

```bash
bundle exec jekyll serve 
```

within the root directory. The templated code will be compiled into a *static website* into `_site`, which can then be exported to the main `public_html` directory. By default, the website can be visualize locally at `http://127.0.0.1:4000`.

## Core Development Guidelines

The code is fairly simple to use and heavily relies on the [Liquid](https://shopify.github.io/liquid/) template language, as well as [Collections](https://jekyllrb.com/docs/collections/) for data management. 


Below is a brief description of each directory for core development:

| Directory | Description |
|:-|:-|
|`_data`| Small YAML-based, serialized collections such as lab members, latest news, etc. Each needs to be added to `_config.yml`. |
|`_includes`| Modular templates for the main components of the website. Can be included in Liquid using `{% include <filename> %}` |
|`_layouts`| Page [layouts](https://jekyllrb.com/docs/step-by-step/04-layouts/) for different website pages. Can be inherited and modified easily.
|`_publications`| Collections for lab publications. Each file must be a Markdown file named `YYYY-author-acronym.md`.|
|`_teaching`| Collection of courses. Similarly to publications, can have their own page (not done yet).|
|`_site`| Static website files, generated automatically on build.|
|`pages`| Main files for webpages. Corresponds to the individual tabs in the navigation bar. Anything added there will exist at `{{site.url}}/{{page.permalink}}`.|
|`assets`| Website files (e.g., images, fonts) can be stored there. Only for the main website media, such as lab member profile pictures. Ideally lightweight.|
|`pub-assets`| Currently used for publication files (e.g., paper teaser, PDF). File naming convention follows `_publications`. Temporary as large files will be hosted somewhere else in the future.
|`css`|Custom stylesheets. Relies primarily on [Bootstrap 3.4](https://getbootstrap.com/docs/3.4/) where `custom.css` is used override styling.
|`js`|Custom Javascript functions.|


There are a few other files that require special attention:

| File | Description |
|:-|:-|
|`_confil.yml`|Main [configuration](https://jekyllrb.com/docs/configuration/) file. Can store global variables accessible via `site.{{my-variable}}`. Anything changed here will only be updated *after rebuild*. | 
|`index.html`| Website landing page.|
|`Gemfile/Gemfile.lock`|Description of [dependencies](https://bundler.io/guides/gemfile.html) for Ruby environment, do not edit.|

## Adding/Removing Entries

### Lab Members

Modify `_data/members.yaml` by adding/removing an entry. Make sure to add new members in the right category (e.g., grads, alumnis). Adding a member to the lab will automatically create a user card on the landing page and an entry at `{{site.url}}/people`.

### News

Add new entry in `_data/news.yaml` following the given format. The most recent news will be shown on the landing pages, all news will be available add `{{site.url}}/news`.

### Publications

To add a new publications, follow these simple steps:

1) Duplicate `.2023-author-acronym.md` and rename accordingly with main author's last name and publication acronym. Remove leading `.` to make it visible to Jekyll.
2) Modify the file by replacing relevant fields for the new paper. By default, the template have most fields filled to give a sense of what is expected, although most fields are optional.
3) Add hyperlinks to media files on remote servers or in `/pub-assets`. Create paper directory `/pub-assets/2023-author-acronym.md`, if necessary.
3) When done, delete unused field data by leaving the tag empty or with a comment symbol (e.g., `file: #`).

If done correctly, the paper will be automatically formatted and visible at `{{site.url}}/publications/acronym`.

### Courses 

Add a new entry in `_data/teaching.yaml` following the given format.

## Other Guidelines

### Permissions
__Only organization administrators__ can push modifications to the main public website. Other members can see the repository in read-only mode. If a student wants to contribute a change (e.g., new publication), another repository will be made available (e.g., `website-public`) to them where they can freely commit Markdown files and media. This repository will be added as a submodule to this repository, allowing seamless integration while retaining appropriate priviledges.

### Website Updates

__Users.__ We do not use pull requests on this repository as this would require every student to clone the main build in order to modify a handful of files. Instead, we will rely on a submodule which will allow users to use the GitHub web interface to add and modify Markdown files easily. Users can also use the Git command-line to push/pull from the public submodule repository.

__Administrators.__ To update the website following a recent change from a user, an administrator will need to:
1) Pull changes from the submodule `website-public`.
2) Recompile the static website locally to update `_site`.
3) Update `_site` in `public_html` using a tool like `rsync`.

Current administrators are Derek Nowrouzrezahrai, Marc-Antoine Beaudoin and Joey Litalien.

## TODOs
- [ ] Setup public submodule for non-admin users.
- [ ] Setup host directory for large files to eventually replace `/pub-assets`.