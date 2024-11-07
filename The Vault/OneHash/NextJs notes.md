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
	- It can be done using type script, which comes with great support for inside of app Router out of the box 
	- type Repository = {id : number; 
		name : string;
		full_name : string;
		}; 
		export default async function Page () {
		 const res = await fetch ('link');
		 const data : Repository = await res. json();
		 return <h 1> {data.full_name} </ h 1> 
		}
	- With this my editor gives me that functional feedbacks! This only calls data at data.full_name
	- This code can be structured anyway, but breaking is recommended for making things easier to read and work with and it feels natural. 
- In next JS the data can also be fetched to not only pages but even to any server components. If we make this data is essentially up one layer and can be shared when we navigate to different routes.  


## Caching 
- Support for static data, dynamic data or data that gets revalidated .By default all of the data fetches in Next JS is cached static, to emulate the behavior with the help of webfetch api,
  const res = await fetch ('link', {
	  cache : 'no-store' //On every request we bypass caching and 
                    // fetch new data  
  });
- This also supports the data that you want to revalidate (also known as incremental static regeneration)
	const res = await fetch ('link', {
		{
			next : {
			revalidate : 5, 
			} 
		}, // with this the data is fetched only after 5 sec.  
  });    
- We can combine 2 examples : previously in the pages directory our data fetching strategy whether it's static dynamic or incremental static regeneration can be combined under the same route like : 
	async funciton getTiime () : Promise<Time> { 
		const res = await fetch ('link', {
			next : {
				revalidate : 5; 
			},
		});
		Return res.json();
	}
	 Async function getRepo () :  Promise<Repository> {
		 Const res = await fetch ('link');
		 return res. json
	 }