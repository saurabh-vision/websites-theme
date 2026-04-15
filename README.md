# Chirpy Starter

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

A minimal, ready-to-use template for creating a blog with the [**Chirpy**][chirpy] Jekyll theme. Get up and running in minutes with all critical files pre-configured.

## Why This Starter Exists

When installing Chirpy through [RubyGems.org][gem], Jekyll can only read a subset of theme files (`_data`, `_layouts`, `_includes`, `_sass`, `assets`) and limited `_config.yml` options from the gem. As a result, users cannot enjoy the full out-of-the-box experience that Chirpy offers.

To unlock all features, the following files must be present in your Jekyll site:

```shell
.
├── _config.yml
├── _plugins
├── _tabs
└── index.html
```

This starter bundles those files from the latest **Chirpy** release along with a [CD][CD] workflow, so you can start writing immediately.

## Saurabh Audit Customization

### 1. How to update the Origin (About) page
The "Origin" tab is located at `_tabs/origin.md`. Edit this file to share your founder story, vision, and mission. It is configured as Order 1 in the sidebar.

### 2. How to manage the Archive
- **Storage**: Upload your PDF, checksheets, or resources to `/assets/archive/`.
- **Linking**: Add the link to your file in `_tabs/archive.md`. 
  - Example: `[Market Checklist](../assets/archive/my-file.pdf)`

### 3. How to add a new Tool
This section is fully automated and designed for speed.
- **Save Tool**: Save your standalone HTML/JS tool file into the `/tools/` directory (e.g., `my-new-tool.html`).
- **Register**: Add an entry to `_data/tools.yml`.
  - **Required fields**: `name`, `slug`, `description`, `tags` (array), `featured` (boolean), `icon`.
- **Display**: The Tools Library page will automatically detect the new file and render a styled card for it.

### 4. How to add a new Post
To keep the site organized, posts are categorized by folder within `_posts/`.
- **Location**: Place your Markdown file in the corresponding subfolder:
  - `_posts/case-studies/`
  - `_posts/build-in-public/`
  - `_posts/brutal-ai-reviews/`
  - `_posts/projects/`
- **Naming**: Use the strict Jekyll convention: `YYYY-MM-DD-title.md`. 
  - *Example*: `2026-05-01-saas-pricing-failure.md`
- **Categorization**: Ensure the `categories` field in your front matter matches the section (e.g., `categories: [Case Studies]`).

### 5. Automated Content Listing
The site uses automated loops to keep the Home page and Sidebar Tabs fresh.
- **Home Page**: The "Latest Audit & Build Updates" section shows the 5 most recent posts from all categories combined.
- **Section Tabs**: Each sidebar tab (e.g., Case Studies) automatically filters and lists posts that are stored in its corresponding `_posts/` subfolder.
- **Workflow**: Just drop a new file in the correct folder with the correct naming, and it will appear everywhere automatically!

## Pre-flight Check
Before deploying, run the local test script to check for broken links:
```shell
./tools/test.sh
```

## Contributing

This repository is automatically updated with new releases from the theme repository. If you encounter any issues or want to contribute to its improvement, please visit the [theme repository][chirpy] to provide feedback.

## License

This work is published under [MIT][mit] License.

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE
