# React-History
A brief history on the development of React


Facebook, or as my friend, Kayla’s father liked to ask, “Why don’t you add me on Facebook?” Well I did not add you on Facebook because I deleted my profile, which is probably not true since your data is never truly deleted. But I could have replied, “Facebook is running too slow,” and this would have been true, but 2011 Asiah did not know that.  She just grew tired of Facebook, although many cool new features were being added like the “video calling feature” and the “Timeline feature” where you could see your friends Profiles in a nice tile view manner, 1-800 very cool. But as more and more users began to use Facebook, the development team needed more and more engineers to keep the code running flawlessly, we were past the days of AOL dial up and Facebooks code demanded an upgrade in order to run efficiently. 

Code maintenance became hard to keep up with for Facebook engineers and the application features slowed things down. Cascading updates- where new data flows in, some small changes lower in the code base tree were needed to re-render the entire application. You can imagine it would be hard to identify where those changes needed to be in order to re-render the application. 

That’s where Jordan Walke came in.  Jordan built a prototype to make the rendering process way easier. Initially it was called FaxJs, in fax this it were it all began. The inspiration for react came from XHP- which was an HTML component framework for PHP being used at Facebook at the time. XHP was great for creating reusable and custom HTML elements and composite components. In 2013 Jordan Walke introduced React to the world to be an open-sourced component framework. 

You may be asking what is React? All in all, React is a library, not a framework. It’s a JS library built for fast and interactive user interfaces. In fact, React is the most popular JS library and one of the most starred repositories on GitHub. React is constantly being updated. 

React works like views in the MVC(Model View Controller) model using a component based system. The views handle how data is being shown to the user. Because of the MVC model developers are able to work on different components without affecting each other. Developing teams are usually divided between back-end and front-end. The back-end developers can design the structure of the data and how the user interacts with it without requiring the user interface to be completed. And the front-end developers are able to design and test the layout of the application prior to the data structure being available. 

React uses a component architecture that provides a set of user interface (UI) elements. Each UI element is a single higher-level component that combines the 3 required MVC components into a single package. By creating these higher-level components that are independent of each other, developers are able to reuse components quickly and easily in other applications.

Components are specified as custom HTML tags, giving simple usability. Developers can build independent isolated reusable components, then reuse them to build complex UI. 

Root components represent the internal application and contain other child components so you can imagine it like a tree of components: Lets use Twitter as an example. 
EX: Twitter App Build split into components:
1. Nav bar 
2. Profile
3. Trends
4. Feed
*Within the feed there are components:
	-Tweet has component:
	-Likes
Like components can be reused on other pages or even different applications. Each component a piece of UI we could build this one in isolation then use components and put together to create complex UIs
In terms of implementation, components are typically implemented as a JS class that has some state and render method. EX: 

Class Tweet {
	state = {} // is the data we want to display when component is rendered 
	render() {  // render method responsible for describing what UI should look like 
        }
}

The output of this render method is a React Element which is a JS object that maps to a DOM element. It is not a real DOM element, just a JS object that represents that DOM element in memory. React keeps a representation of DOM in its short term memory or the “Virtual DOM”.  Not to get confused with the browser DOM. This Virtual DOM is effected when we change the stat of a component, a new react element is created, react will compare this element with its children with the previous one, it figures out what has changed and then updates a part of the browser DOM to keep it in isync with the Virtual DOM. We simply change the state of our components and react will automatically update the DOM. 

Why is this helpful? Developers don’t have to work with the DOM API in browsers. Developers no longer have to write code in query and manipulate the DOM or attach event handlers to DOM elements. NO more:

Const example = document.querySelector();
example.classList.add();
example.addEventListener();

React is very useful when it comes to protecting internal components or data flows. The subcomponents cannot be directly affected with external queries, making a good choice for front-end views development. It is also very efficient in updating the HTML document with new data, making it a perfect choice for data-driven web application

Wait…So that’s why it’s called React! When the state changes, react well, reacts to the state change and updates the DOM. Tada!  React only takes care of rendering the view and making sure the view and state are in sync. When building applications with react, developers need to use other libraries for calling HTTP elements, routing which means developers get to choose the libraries that they want to work with. Yay options. 

Another thing worth mentioning with react is the lifecycle methods. You can think of react lifecycle methods as a series of events that happen from the birth of a component to its death. Every component goes through a life cycle of events: birth, growth, death. A way of thinking about it is: 

Mounting- Birth of component 
Update  - Growth of component 
Unmounting - Death of component

Through lifecycle methods, developers can then control what happens when each tiny section of UI renders, updates, thinks about re-rendering, and then disappears entirely. Common React lifecycle methods are…

The render() is the most used lifecycle method.
It is a pure function.
You cannot set state in render()
The componentDidMount() happens as soon as your component is mounted.
You can set state here but with caution.
The componentDidUpdate() happens as soon as the updating happens.
You can set state here but with caution
The ComponentWillMount() 99% of your components should probably not use
Main usage for App configuration in your root component.
The componentWillUnmount() happens just before the component unmounts and is destroyed.
This is a good place to cleanup all the data.
You cannot set state here.
The componentWillReceiveProps() Acts on particular prop changes to trigger state transitions
If the props will change in a way that is significant, act on it
Checks which props will change- sometimes it’s called when nothing has changed; React just wants to check in
The shouldComponentUpdate() can be used rarely.
It can be called if you need to tell React not to re-render for a certain state or prop change.
This needs to be used with caution only for certain performance optimizations.
Always return as a boolean
The componentWillUpdate() basically the same as componentWillUpdate
Most common usage: Used instead of componentWillReceiveProps on a component that also has shouldComponentUpdate (but no access to previous props)
The two new lifecycle methods are getDerivedStateFromProps() and getSnapshotBeforeUpdate().
They need to be used only occasionally.
Not many examples are out there for these two methods and they are still being discussed and will have more references in the future.
In a utopia all rendering concerns would be controlled by the state and props. However, sometimes developers need control over how the component is updating, in that case it is useful to utilize Reacts lifecycle methods. 

Many developers all over the world have adopted the React library. In 2014, React developer tools became an extension of Chrome developer tools and React Hot Loader was released. React Hot Loader is a plugin that allows React components to be live reloaded without the loss of state. In 2014, React was mixing markup and display logic and beginning to expand.

Shortly after, in 2015 React released at the JSConf US, React Native which is a helpful framework for building mobile applications using React. This ensures that the same set of engineers can build applications for whatever platform they choose, without having to change the syntax.  That same year in October React library was split into two packages. React and React DOM. React began to get recognition from companies like Airbnb and Netflix! 

Today the latest version of React is 16.13.1, but an update is inevitable. For one thing is for sure the developers are always coming up with some solution for a bug, and new innovative ways to stay improving the usage. There is always something to be learned and I have no doubt that companies and developers will continue to use React technology to solve their problems. What started out as a small solution to a UI problem turned into one of the most downloaded and utilized libraries used by developers all around the world. So much effort has gone into developing React, hmm maybe I will re-activate that Facebook page. 


SOURCES:

Domes, Scott. “React Lifecycle Methods- How and When to Use Them.” 28 Mar. 2017, engineering.musefind.com/react-lifecycle-methods-how-and-when-to-use-them-2111a1b692b1.
Ravichandran, Adhithi. “React Lifecycle Methods - A Deep Dive.” Programming with Mosh, 17 Feb. 2019, programmingwithmosh.com/javascript/react-lifecycle-methods/.
Hámori, Ferenc. “The History of React.js on a Timeline: @RisingStack.” RisingStack Engineering - Node.js Tutorials & Resources, RisingStack Engineering - Node.js Tutorials & Resources, 10 Feb. 2020, blog.risingstack.com/the-history-of-react-js-on-a-timeline/.
Facebook. “Facebook/React.” GitHub, github.com/facebook/react/blob/master/CHANGELOG.md.
Dashbouquet Development. “The Evolution Of React.” Hacker Noon, 11 May 2020, hackernoon.com/the-evolution-of-react-48409fac2efd.
React.js Conf 2015, “https://www.youtube.com/watch?v=KVZ-P-ZI6W4&t=0s&list=PLb0IAmt7-GS1cbw4qonlQztYV1TAW0sCr&index=1”	
Hunt, Pete: Rethinking Best Practices JS Conf EU “https://www.youtube.com/watch?v=x7cQ3mrcKaY”
