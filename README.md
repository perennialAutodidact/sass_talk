# Sass Example

<img src="https://raw.githubusercontent.com/keegangood/sass_talk/master/sass-logo.png" width=200/>

This project was created to demonstrate the basics of the Sass CSS Preprocessor for a Tech Talk presented by the PDX Code Guild in Portland, Oregon on March 18, 2021.

The Sass shown in this example is by no means an exhaustive collection and is intended to get folks started with Sass.

Watch the presentation [here](https://www.youtube.com/watch?v=RhX2rb10AC4)!

Final Demo Result:
<br/>
<img src="/sass-demo.gif" width=800>

## Install

Install the Sass Javascript CLI

```bash
npm install -g sass
```

## Syntax

This example uses the SCSS syntax, which looks very similar to CSS. It uses curly brackets and semicolons to separate different selectors. According to the Sass docs, "With a few small exceptions ... essentially all CSS is valid SCSS"

## Compile Sass stylesheets into CSS

Sass runs entirely in the command line and can compile either a single Sass file or a whole directory of Sass files.

The following command will read `index.scss` and compile CSS into `index.css`.

```bash
sass index.scss:index.css
```

The following command will read all the files in the `scss/` directory and output CSS into the project directory, represented with dot notation. Any `.scss` files not labeled as a partial with a leading underscore will produce their own `.css` file.

```bash
sass ./scss:./
```

## Flags

### --no-source-map

By default, Sass will generate `.map.css` files when compiling. These help to keep track of the `.scss` files and line numbers where the compiled CSS originated. These are used by the browser's dev tools to assist in debugging styles.

If no `.css.map` files are desired, the `--no-source-map` can be added to the `sass` command

```bash
sass ./scss:./ --no-source-map
```

### --watch

To avoid the need to run the `sass` command after every change to your styles, the `--watch` flag can be added. This will cause `sass` to watch for changes to your Sass file/directory and recompile on each save.

```bash
sass ./scss:./ --watch
```

## Resources
[https://sass-lang.com/](https://sass-lang.com/)

[Sass-guidelin.es](https://sass-lang.com/)
