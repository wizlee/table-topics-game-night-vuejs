## Summary

This repo is bootscrap by using [create-vue](https://github.com/vuejs/create-vue), then modifying it into a layout and content that suits to be presented for [Toastmaster's Table Topics session](https://www.toastmasters.org/Membership/Club-Meeting-Roles/Table-Topics-Speaker). 

## History

> Steps in creating completing this repo
1. Run `npm init vue@latest`
    - After typing project name, choose no for the rest of the questions by pressing enter.
2. Test out the scaffolded project by running the following commands
    ```bash 
    > cd <your-project-name>
    > npm install
    > npm run dev
    ```
3. Remove any unnessary boilerplate content.
    - Mostly rewording the landing page
    - Renaming component files and variables to suit the toastmaster table topic content
4. Changing the icons into graphics that looks more compelling.
5. Install SASS to incoorperate [this card flipping effect example](https://codepen.io/alphardex/pen/ExaZgxp). 
    - To enable SASS, follows the steps [in the offical vite guide](https://vitejs.dev/guide/features.html#css-pre-processors).
        - npm install -D sass
        - Use SASS in component as such `<style lang="scss"></style>`
    - Remove the reflection effect of the card in the example.


## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
