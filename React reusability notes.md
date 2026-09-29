In react there is something known as as a rest operator, while destructuring if an object contains a lot of key/value pairs and you want some of them but want the rest to remain in the object a rest is used e.g ({children,text,...rest}). This causes the children and text to be destsrucured but the rest of the objects are part of the object.

If there a lot of props being passed down a {...props} can be used if all values of props are valid attributes.

There is a npm package by the name of classnames which can be used to give multiple classes to an element if they are variable className = {class1 class2} doesnt work as both are variables so instead classnames is used i.e const allClasses = classname(class1,class2); this is then used in className attribute

Children can be used and are part of props for components

You can pass in components as children as well to flatten out the structure. e.g <Menu> If this components takes in 10 props but it is being used to pass down props to other components than you can just <Menu> <MenuButton> <MenuDropdown> <Menu/>. In the inner components the props can be passed for better code structure

You can use React.Children to pass down props to a component within a parent component,basically in a child component. for example in a parent component <div>{React.Children.map((childre //ARray to manipulate),(child)=>{return React.cloneElement(child,{//Pass props here})})}</div>

React.Children works only for children not grand child so it is not very effective

Context API is the solution to prop drilling it can be setup by using React.useContenxt() and assigning it to a variable and then wrapping all the components needing that prop with it it is created by const hey = React.createContext()  e.g

<ContextVar.Provider value="light">{components}<ContextVar.Provider/> Value of ligth will be passed to all components export{ContextVar} //It needs to be exported as well

useContext(name of context) can be used to get value of passed prop but it needs to be imported first

you need to use {} while exporting context like export {themeContext};

refs can also be used in react they are like state because they remember their previous values but they donot cause a rerender like state does. They have a current property so in order to access them you need to use a current property e.g const newRef = React.useRef(0);// This 0 is stored in current property of new ref newRef.current will display zero not newRef

There is something called as a no-op function if you pass a function as a prop you can set it is as a no-op so if it had an empty value it wouldnt be undefined but be considered an empty function. function Component({someFunction=()=>{}}) .This will set the function as a no-op

renderProps can be used to access child states from a parent element e.g passing a function as a prop takes takes the child state as a parameter and returns an html element depending on the value

Custom hooks allow you to combine different hooks for example useState and useEffect

split and spread operator dont work on boolean array

Custom hooks are basically functions that take in parameters and apply hooks on those parameters, custom hooks function start with use e.g useStateafterfirsttry