# js-prettier-format-script
prettier-format-script

```
echo """
// @trivago/prettier-plugin-sort-imports
module.exports = {
  tabWidth: 2,
  printWidth: 100,
  bracketSpacing: true,
  jsxBracketSameLine: true,
  singleQuote: true,
  trailingComma: 'all',
  arrowParens: 'always',
  importOrder: ['^[a-zA-Z0-9]+$', '^[@]', '^[a-zA-Z]', '^[./]'],
};
""" > '.prettierrc.js' && \
echo """
npx prettier --write src/**/*.{ts,tsx,scss} && \
npx prettier --write *.md && \
npx prettier --write --parser json *.json && \
echo 'Done formatting'
""" > format.sh && chmod +x format.sh && \
npm i --save-dev @trivago/prettier-plugin-sort-imports && \
echo """
Done bootstraping - Adding this to your package.json
================================================
"format": "sh format.sh",
"""
```


### Minor sass path
```
SASS_PATH=./node_modules:./src
```
