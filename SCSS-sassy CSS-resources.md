## SCSS 
 SCSS (Sassy CSS)

There are two syntaxes available for Sass. The first, known as SCSS (Sassy CSS) and used throughout this reference, is an extension of the syntax of CSS. This means that every valid CSS stylesheet is a valid SCSS file with the same meaning. This syntax is enhanced with the Sass features described below. Files using this syntax have the .scss extension.

The second and older syntax, known as the indented syntax (or sometimes just “Sass”), provides a more concise way of writing CSS. It uses indentation rather than brackets to indicate nesting of selectors, and newlines rather than semicolons to separate properties. Files using this syntax have the .sass extension.


The difference is syntax. Underneath the textual exterior they are identical. This is why sass and scss files can import each other. Actually, Sass has four syntax parsers: scss, sass, CSS, and less. All of these convert a different syntax into an Abstract Syntax Tree which is further processed into CSS output or even onto one of the other formats via the sass-convert tool.

Use the syntax you like the best, both are fully supported and you can change between them later if you change your mind.