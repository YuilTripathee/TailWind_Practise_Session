# Reflections from this session

We used Tailwind CSS to design a simple page. It was a walkthrough sessions to explore the various properties and behaviors of Tailwind CSS.

## Some notes that might come handy

### Utility Commands

#### Building CSS file

Here's a sample command to build CSS file into usable format. It is better to keep within `package.json` if you need to run this continously.

```bash
tailwindcss build src/styles.css -o public/styles.css
```

#### Configuration

The configuration is managed using `tailwind.config.js` file. Here's the command to create it.

```bash
npx tailwindcss init # minimal version
npx tailwindcss init --full # extended version 
```

> It is recommended to leave the full version as it is (you can rename and keep that if you want). To introduce custom themes, initiate a basic version of tailwind config file and begin the work without overriding Tailwind class names.

#### Treeshaking

To remove unwanted CSS classes in your file, you just need to configure Node.js environment as production. Let's assume build command is given in `package.json` as `build-css`. Here's the command to do so. But, it is not recommended in development environment.

```bash
NODE_ENV=production npm run build-css
```

### Bonus tips

1. As you import `tailwind`, the brower's default styles to render HTML elements are overriden.
2. Get ready to browse Tailwind documentation continously.
3. Don't edit in `dist` or `public` section for CSS manipulation (e.g. Custom Font). Instead, use `src` section to do so.

## References

Here is the snapshot of the technical parameters within this source code during the time of this documetation.

```txt
TailWind CSS
============
Version: 2.0.1
```

Just checking out `package.json` might also help.

## Credits

This was made during the course session from The Net Ninja - YouTube.
