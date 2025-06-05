```
# Namaste_React

<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
This is the core element of React
Example:
React.createElement("h1",{},"Namaste")

<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
This is the DOM create a root and render all the element to Root
example:
ReactDOM.createRoot("root")

crossorigin is helpful for getting When a browser requests a resource from a different domain (e.g., CDN), it’s considered a cross-origin request.

//  <div id="parent">
//     <div id="child">    
//         <h1></h1>
//     </div>
//  </div>
 
 
 App.js
--------------
 const header = React.createElement(
       "div",{ id: "parent" },
       React.createElement(
           "div",{id:"child"},
           React.createElement("h1", {}, "I am h1 tag"))
   );

   const root = ReactDOM.createRoot(document.getElementById("root"));
   root.render(header);

Here header is the React Element which is will create the object and once u call the render it will converts it to HTML

NPM is repo for all the packages and it is usefull for installing the package
package.json is the configuration for npm

npm install -D parcel

| Purpose            | Command                 | Saved In          |
| ------------------ | ----------------------- | ----------------- |
| Dev Dependency     | `npm install -D parcel` | `devDependencies` |
| Regular Dependency | `npm install parcel`    | `dependencies`    |

Parcel
 is a web application bundler that automatically compiles and bundles your JavaScript, HTML, CSS, and other files into optimized output for the browser.
1)dev build 
2)Local Server
3)HMR (hot module replacement)

npx parcel index.html
npx is the executing the installed packages so above command it will be helpful for creating the own server 










```

