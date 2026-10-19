Ove's very own personal blog.

Theme is based on Hyde and two days of his hundred percent effort to edit this base theme to make it as user friendly as possible which includes printing and reading UI-UX articles, pondering around Dribble and Behance, requesting people to use their ideas on variouos design platforms, asking for help here and there, taking recommendations from friends and most importantly, by googling HTML and CSS basics.

## Running Locally

### Prerequisites

Install Ruby and Bundler:

```bash
# Ubuntu/Debian
sudo apt install ruby-full build-essential zlib1g-dev
sudo gem install bundler
```

### Setup

Install the project dependencies (installs gems locally to avoid needing `sudo`):

```bash
bundle install --path vendor/bundle
```

### Serve

Run the site locally at [http://localhost:4000](http://localhost:4000):

```bash
bundle exec jekyll serve
```

To auto-reload on file changes (useful while editing):

```bash
bundle exec jekyll serve --livereload
```

The site will be available at `http://localhost:4000`. Press `Ctrl+C` to stop the server.
