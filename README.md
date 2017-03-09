# core-scss

How the SCSS is organised for the Eredivisie Profcoach games made by Chroma.

### Structure

Please note that the app and static directories are include here for illustration and reference only. They are not intended for use 'as is' in other projects.

#### core

Base set of SCSS variables, mixins and OOCSS base helper classes. These are designed to be super generic and intended to be used across all games and to form the basis for the SCSS in the white label platform product. These styles may be used as the basis for other style frameworks.

#### app  

SCSS variables, mixins and OOCSS helper classes that are brand, and possibly game specific. The preferred pattern is to include and extend named stylesheets from the core set. A master 'theme' stylesheet collates these extensions. Because the theme stylesheet will be imported into all components, it is important not to include any literal CSS/SCSS rules. Any literal CSS/SCSS should only be imported into the top level stylesheet (the convention is to attach this top level stylesheet into BaseContainer). As a guide, the naming convention is to precede a stylesheet filename with an underscore which indicates that the stylesheet contains no literal CSS/SCSS, and can therefore be safely imported anywhere.

#### static

The default place for static assets and webfont files. Variables in app/variables set the css font and image base paths to this directory.

### Credits

- Bootstrap 4 for the organisation of variables and the MQ mixins and best practice inspiration

- @tigt and @jakob-e for the inline SVG helper functions (https://codepen.io/tigt/post/optimizing-svgs-in-data-uris)
