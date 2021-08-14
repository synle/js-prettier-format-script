# js-prettier-format-script
prettier-format-script


```
echo `
// @trivago/prettier-plugin-sort-imports
module.exports = {
  tabWidth: 2,
  bracketSpacing: true,
  jsxBracketSameLine: true,
  singleQuote: true,
  trailingComma: 'all',
  importOrder: ['^[a-zA-Z0-9]+$', '^[@]', '^[a-zA-Z]', '^[./]'],
};
` > '.prettierrc.js' && \
echo `
npx prettier --write src/**/*.{ts,tsx,scss} && \
npx prettier --write *.md && \
npx prettier --write --parser json *.json && \
echo 'Done formatting'
` > format.sh && chmod +x format.sh && \
npm i --save-dev @trivago/prettier-plugin-sort-imports
```
