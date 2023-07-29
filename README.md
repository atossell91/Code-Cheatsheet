# Code-Cheatsheet
## NPM/NPX
### Make an Electron App with React and Typescript:
1. Open the Powershell at the directory that the project will live in
2. Create a Typescript+Webpack Electron project with the following command:

       npm init electron-app@latest app-name -- --template=webpack-typescript
       cd app-name
       npm install --save react react-dom
       npm install --save-dev @types/react @types/react-dom

3. Inside the newly created directory, open the `tsconfig.json` file.
4. Inside the `tsconfig.json` file, under `compilerOptions` add the following line:

       "jsx": "react-jsx"

5. Add the file `app.tsx` to the `src` directory inside the `app-name` directory
6. Inside the newly created `app.tsx` file, add the following code:

       import * as ReactDOM from 'react-dom';
       
       function render() {
           ReactDOM.render(<h2>Hello from React!</h2>, document.body);
       }
        
       render();

8. Add the followinng line of code to the end of the `render.ts` file (still in the `src` directory):

       import './app';
   
* Sources:
    * https://www.electronforge.io/templates/typescript-+-webpack-template
    * https://www.electronforge.io/guides/framework-integration/react-with-typescript
