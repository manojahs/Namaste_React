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
4)File watching algorithm- thats why refresh rate will be high
5)Caching- faster builds
6)Image optimization
7)Minification
8)Bundling
9)Compress

npx parcel index.html
npx is the executing the installed packages so above command it will be helpful for creating the own server 

Browserlist
-------------
Helpful for providing the browsers list that react app needs to be run

JSX
-------
jsx is the html/xml like syntax

const jsxheading = <h1>Namaste React</h1>
console.log(jsxheading);
It will print object bcz
JSX will be converting into Reactelement which is handled by Babel
so this jsxheading it works as a createElement later Js-object once render it will convert into HTMl

Rendering Jsx component
-------------------------
There are 2 types for component
1) Functional component
2) Class component

1)Function component
--------------------
A function that returns jsx code is called as functional component

 const Header = () =>{
 return (<div><h1 id="react">Namaste React</h1>
     <h2>Manoj</h2>
     </div>
 )}

or

 const Header = () =>
  (<div><h1 id="react">Namaste React</h1>
     <h2>Manoj</h2>
     </div>
 )



const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<Header/>);

Rules
-------
1)Function name must be Capital letter
2) If function is using more than 2 lines of code then make inside the angular bracker
ex: return ( 1.......
2.......);
3)While rendering the component component name must be under <Component_Name/>.

Inserting One component inside another (Component Composition)
---------------------------------------
const Title = () =>(
    <div>
    <h1>This is the Title</h1>
    <h1>By Manoj</h1>
    </div>
)
 
 const Header = () =>
  (<div>
   <Title/>              //anything is fine in below 3
   <Title><Title/>
   {Title()}
    <h1 id="react">Namaste React</h1>
     </div>
 )

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<Header/>);

if you want use javascript inside the function component (jsx) u can use with curley braces {}

exam:
let a =100;

 const Header = () =>
  (<div>
   <Title/>
    {a}
    <h1 id="react">Namaste React</h1>
     </div>
 )

This is standard
const Heading = () => {
    return (
     <div>
        <Title/>
        {a}
        <h2>Hi Brother</h2>
        </div>
    );
};



React Element
-------------

const title = (
    <div>
    <h1>This is the Title</h1>
    <h1>By Manoj</h1>
    </div>
);

Props
--------------
Passing a props to a component. its like normal arguments to a function
It will help for dynamic data binding

 <RestaurantCard resName="Megana Food" Cuisine="biriyani" rating= "5"/>

const RestaurantCard = ({resName,Cuisine,rating}) => {
  return (
    <div className="restaurant-card">
        <img className="manis" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQHZHhaFT7rualJfwxrlfAWo16h8Z6xKWAbOA&s"/>
      <p>{resName}</p>
      <p>{Cuisine}</p>
      <p>{rating}</p>
    </div>
  );
};

or 

const RestaurantCard = (props) => {

const {resName,Cuisine,rating} = props
  return (
    <div className="restaurant-card">
        <img className="manis" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQHZHhaFT7rualJfwxrlfAWo16h8Z6xKWAbOA&s"/>
      <p>{resName}</p>
      <p>{Cuisine}</p>
      <p>{rating}</p>
    </div>
  );
};


Config driver UI
----------

Config which drives the UI its depend on data each places it will show different data bcz thats why config are being made


```

