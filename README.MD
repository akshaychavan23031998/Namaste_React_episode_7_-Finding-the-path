# **Episode 07:-**

### **useEffectHooks:-**

the default nature of useeffect hooks is to be called after render every time.

it takes2 parameters1st is call back function which is must and2nd is dependancy array which is not mandatary we can and we can not use it according to our use case.

#### **Case1:-** No dependancy array, this will be called after each render the component is rendered.

ex:-useEffect ({} => {

  console.log("useEffect Called");

})

#### **Case2:- empty dependancy array, this will be called only once in the start of page refresh means in initial render.**

ex:-useEffect ({} => {

  console.log("useEffect Called");

}, []);

#### **Case3:- dependancy array with value, this will be called when ever the value changes, for ex login/logout btn.**

ex:- useEffect ({} => {

  console.log("useEffect Called");

},[btnName]);

# **Routing:-**

so there are2 steps, in routing1st creating router and to use this created routing we need to use it by provider,

**so to create routing we use createBrowserRouter and use this we use RouterProvider.**

ex:-

import { RouterProvider, createBrowserRouter } from"react-router-dom";

constappRouter =**createBrowserRouter**([

  {

    path:"/",

    element:`<AppLayout/>`

  },

  {

    path:"/about",

    element:`<About/>`

  }

])

constroot =ReactDOM.createRoot(document.getElementById("root"));

root.render(<**RouterProviderrouter**={appRouter}/>); // this is how we render react component.
