React opens components recursively i mean if there are two components and eeach of them open three other components it will open all the components of first one first then second

A component like App could be wrapped in <React.StrictMode> to find out about any bugs as it double renders all functions even react.useEffect

You can cleanup setInterval in React.useEffect by setting set interval to a var and return clearInterval(var)

React.lazy can be used to use dynamic imports which will import something when it is needed not always const ProductLists = React.lazy(()=>{return import(file.jsx)}). If it is conditionally rendered it will only import when needed.

React will throw an error if this is done alone on slow internets so we use React.suspend and wrap it around the thing to be conditionally rendered it receives a prop with the name fall back which has an html element in it which is displayed while the thing is loading.

The lazy component should be created outside the component to be rerendered when the state changes

React.useMemo() takes in a callback function and a dependency array and is set equal to something. This is different from useEffect as it remembers the value from render to render. It is used for performance and big calculations to only take place when something changes but also be remembered from one render to the next

React.memo(comp) takes in a component as an argument and returns the componenet but now the component has the property to only get re rendered once its props changes.

if an object,array or function is passed down as a prop react.memo wont work because js doesnt treat 2 different objects to be the same even if they are

so react.useMemo() could be used so that the value of objects remain same between renders

useCallback() basically does the same thing that useMemo() does for objects and arrays it does for functions

In aria-label you write what you want the screen reader to say out loud

Dialog in react can be use in a declarative way the open attribute can be used and if it is true the dialog will show else it will not