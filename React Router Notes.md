React router can be used to create multipage applications using a single page to use it <BrowserRouter> should close the app component

<Routes> should be used in it and then <Route> should be used in it

Route has a path prop and an element prop which takes them to that element when the path is entered as an url and also link element can be used to change the path without refresh

<Link to="/Home"> is used to change the path to the to property whenever a thing enclosed in link is clicked

<Route path="/Vans/:id"> can be used to take you to pages with paths like /Vans/1 or any other after second slash

route component only takes in route components as children

useParams can be used to extract the id or whatever stored  in the url it will return an object like id:12 you can use it by storing in any variable for example params and use it by writing params.id or just declassify it 

There is no need to add / on paths in child routes react automatically puts /parent/child in it

index prop could be passed to route element if you want to display the child element automatically when the parent element is open 

The outlet is only required if the parent has an element in it else if the path changes the ui will also change without the outlet if there is no element in the parent

NavLink can be used instead of link and it works basically like link but it can take in className and style props and they can take in functions the isActive built in property can be used to change classes or styles 

end can be used as a prop that will stop underlining more than one elements 

Links can be relative too no need to pass /host/van as a path if your link is in /host just pass van as a path.

There can be two type of relativity in Links route and path if path is chosen it will go back one path if to=".." and if route is chosen it will go back one route

useSearchParams() is a hook just like useState that returns an object with values of params (The things that appear after ? in url) These values can be used to filter/sort things in a shareable state unlike useState

useSearchParams causes a re render if the search params is changed. Also link could be used to change them

you can get search params by using params.get("val");

the setter function initialized in useSearch params can also be used to change searchparams it can take in a string or an object

If a new search param is set it deletes the old search param in order to fix it using hard coded links a function can be used in that function initialize a new URLSearchParams object with the old search params as argument take in key,value pairs as arguments of the bigger function and use .set to set them and also return it and now the search param will be concatenated use ? before sp.toString()

for the setter function to do the same thing take in a key value pair to return to url sp.delete(key) can be used to concatenate sp.set(key,value) can be used sp is the previous search params like we do it in state

Link can pass a state forward this state can be used to e.g get back to the filtered page instead of the whole page state={{search:searchParams.toString()}} now the whole searchParams has been passed and if there is a return button on the other side of the string the filters in the searchParam will be preserved

The useLocation() hook can be used to access state passed through link it is in .state.search search is the name of the object passed as state if no state is passed it is null and a function can be used to return a str corresponding to the to prop of Link 

The path="*" can be used in your routes to represent a page that has no valid path

res.ok can be used to throw errors try and catch can be used to handle them the later being used to display something on screen

const [searchParams,setSearchParams] = useSearchParams(); this is how you use useSearchParams.

setSearchParams({query:12}) will change the url ?query=12

searchParams.get("query") will return value of query

state can be passed in the link as an object and useLocation can be used to access it it has a state key with ann object in it in that the state passed through is stored