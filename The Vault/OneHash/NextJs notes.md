## Routing  
- Layouts : Built in support for layouts and nested layouts, 
	- It's composing diff react components
	- It can compose another page! (Page is nothing but it marks the Ui that u can navigate to inside of my browser). 
	- The code only runs on the server, we have client components for interactivity.  
	- The nextjs has file system based router, still remains and is enhanced. 
	- Dynamic paths 
		- Can also be created with the help of [] brackets to denote that its a dynamic route segment.
		- We can access this path using the params key, inside props of my component. Then for example this params.id can be used in our jsx to render out Id of this segment.
		- We can also access the URL searchParams as well inside props for pages.

## Data Fetching 
- To fetch data inside of our index route, mark your component as async component. Now component is able to support awaiting sum promise inside our body. 
- Let's assume we go with <font color="#00b0f0">const res = await fetch ('Link to repo/server');</font>  Then we can take input in the json as <font color="#00b0f0">const data = await res. json ();</font> and the data can be represented on page like return <h 1> {data. id} < /h1 >
- To make this process smother : 
	- 