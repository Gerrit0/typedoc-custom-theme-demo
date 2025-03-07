# typedoc-custom-theme

Example of creating a custom TypeDoc theme, see
[src/index.tsx](https://github.com/Gerrit0/typedoc-custom-theme-demo/blob/main/src/index.tsx)
for code & comments.

## Notes:

- Do not specify typedoc as a dependency, but as a peer dependency. Specifying
  it as a dependency would result in multiple TypeDoc instances being loaded,
  which will probably break your theme.

- If your package specifies `typedoc-theme` in the keywords, your plugin will
  automatically show up at https://typedoc.org/documents/Themes.html.

- You don't have to create a npm package to use a custom theme. You can also
  specify TypeDoc's
  [plugin](https://typedoc.org/documents/Options.Configuration.html#plugin)
  option to load a local `.js` file. When loading a non-npm package, you must
  specify either an absolute path, or a path starting with `./` as TypeDoc will
  treat paths without a leading `./` as specifying a npm module.
