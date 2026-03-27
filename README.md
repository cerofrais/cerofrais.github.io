# cerofrais.github.io

Personal resume website built with Hugo using the DevResume theme.

## Prerequisites

- [Hugo](https://gohugo.io/installation/) (Extended version recommended)
- Git

## Installation

To install Hugo on macOS:
```bash
brew install hugo
```

For other platforms, visit: https://gohugo.io/installation/

## Project Structure

- `config.toml` - Main configuration file containing all resume content
- `themes/hugo-devresume-theme/` - Hugo theme for the resume
- `public/` - Generated static site (deployed to GitHub Pages)
- `static/assets/images/` - Images like your avatar

## Updating Your Resume

All resume content is managed through the `config.toml` file. Edit the various sections:

### Profile Information
Edit the `[params.profile]` section to update your name, tagline, and avatar.

### Contact Details
Modify the `[params.contact]` section and `[[params.contact.list]]` items.

### Skills
Update the `[params.skills]` section to add/modify technical and professional skills.

### Experience, Education, Projects, etc.
Add or modify the corresponding sections in `config.toml` following the TOML format.

## Hugo Commands

### Local Development

Start a local development server with live reload:
```bash
hugo server -D
```

The site will be available at `http://localhost:1313/`

To include draft content:
```bash
hugo server -D --buildDrafts
```

To see future-dated content:
```bash
hugo server -D --buildFuture
```

### Building the Site

Generate the static site in the `public/` directory:
```bash
hugo
```

Clean and rebuild:
```bash
rm -rf public/
hugo
```

Build with specific environment:
```bash
hugo --environment production
```

### Testing

Check for broken links and issues:
```bash
hugo server --renderToDisk
```

### Deployment

1. Build the site:
   ```bash
   hugo
   ```

2. Commit and push changes:
   ```bash
   git add .
   git commit -m "Update resume content"
   git push origin dev
   ```

3. Merge to master branch for GitHub Pages deployment:
   ```bash
   git checkout master
   git merge dev
   git push origin master
   ```

## Theme Customization

The theme is located in `themes/hugo-devresume-theme/`. To customize:

### Colors
Edit `primaryColor` and `textPrimaryColor` in `config.toml`:
```toml
primaryColor = "#54B689"
textPrimaryColor = "#292929"
```

### Layout
Modify theme templates in `themes/hugo-devresume-theme/layouts/`

### Styles
Edit SCSS files in `themes/hugo-devresume-theme/assets/scss/`

## Troubleshooting

### Theme not found
```bash
git submodule update --init --recursive
```

### Changes not reflecting
Clear Hugo cache:
```bash
hugo --gc
rm -rf resources/
```

### Port already in use
Use a different port:
```bash
hugo server -p 1314
```

## Useful Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [DevResume Theme](https://github.com/cowboysmall-tools/hugo-devresume-theme)
- [Hugo Command Reference](https://gohugo.io/commands/)

## License

This project uses the hugo-devresume-theme. See `themes/hugo-devresume-theme/LICENSE.md` for theme license details.
