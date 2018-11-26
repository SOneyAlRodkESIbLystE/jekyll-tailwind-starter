# Jekyll Tailwind Starter

Welcome! Here you'll find a reasonable starter pack for using [Jekyll](https://jekyllrb.com) with [Tailwind CSS](https://tailwindcss.com), [Autoprefixer](https://github.com/postcss/autoprefixer), and [Purgecss](https://github.com/FullHuman/purgecss).

## About

This project uses [jekyll-postcss](https://github.com/mhanberg/jekyll-postcss) to manage compiling your Tailwind and Autoprefixer styles. You can use any [PostCSS](https://postcss.org) plugin by installing it with `yarn` or `npm` and adding it to your `postcss.config.js`.

[jekyll-purgecss](https://github.com/mhanberg/jekyll-purgecss) is used to integrate Purgecss (only in production).

## Install

```bash
git clone git@github.com:mhanberg/jekyll-tailwind-starter PROJECT_NAME

cd PROJECT_NAME

# Install your Ruby and JavaScript dependencies.
# Initialize your Tailwind configuration.
# Reinitialize your git repository.
bin/setup
```

## Usage

```bash
# Install new dependencies
bin/bootstrap

# Start the server 
bin/start

# Create a new post
bin/new POST_TITLE
```

## File Structure

```
+---_includes
    \---analytics.html // place your analytics tracking snippet in here
    \---components.css // Tailwind components CSS
    \---preflight.css // Tailwind preflight CSS
    \---syntax.css // Syntax highlighting CSS
    \---tailwind.js // Tailwind configuration. This is generated when by bin/setup
+---_layouts
    \---default.html
    \---page.html
    \---post.html
+---_posts
+---_bin
    \---bootstrap // Install dependencies
    \---new // Create a new post and open it in your $EDITOR
    \---setup // Initial site setup
    \---start // Start the server with the livereload, incremental, drafts, and future flags on port 5000
+---_css
    \---site.css // Entry point stylesheet. You can write your styles here or import them from the _includes directory
+---index.md // Front page. This can be changed to an HTML file if desired.
+---404.html 
+---_config.yml // Jekyll configuration
+---postcss.config.js // PostCSS configuration. All plugins should be registered here.
+---purgecss.config.js // Purgecss configuration 
```

## PostCSS plugins

- Tailwind CSS
- Autoprefixer
- postcss-import

## Deployment

This setup has been tested on [Netlify](https://www.netlify.com).
