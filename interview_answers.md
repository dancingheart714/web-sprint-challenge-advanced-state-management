# Interview Answers

Be prepared to demonstrate your understanding of this week's concepts by answering questions on the following topics. These will not be counted as a part of your sprint score but will be helpful for preparing you for your endorsement interview, and enhancing overall understanding.

1. What problem does the context API help solve?
   I think the biggest issue it deals with is prop drilling. Since our data is passed down from the parent to the child through props it can become unmanageable if those levels start to get too deep. With prop drilling through layers and layers of code it can become near impossible to find bugs and such. Context API allows us to keep our State cleaner by providing us with a way to share that data between components without having to explicitly pass our props through every level of the family tree.

2. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

   Actions: Everytime some action happens in our apps there is some kind of a change. The action object takes a "type" property which informs the reducer about what actions are happening which in turn lets the reducer know what part of State needs to change.

   Reducers: The reducer function takes two arguments, the current state and action, and returns a new updated state object that is based on those two arguments. The reducer function is a pure function with no side-effects so it keeps immutability.

   Store: A single JS object..it brings together our State, actions and reducers...it's the home for the entire app's State. We only have one store in an application (making it the "single source of truth"). Because State is stored in this single application, debugging is easier.

3. What does `redux-thunk` allow us to do? How does it change our `action-creators`?

   Thunk is a middleware that makes the flow from our action to the reducer asynchronous. It's another word for function but not like any other function. When an action is called, thunk intercepts and checks to see if the action is returning an object or a function. If the action is returning a function, it will insert a dispatch which we can use to return which type of action we would like for it to do.

4. What is your favorite state management system you've learned and this sprint? Please explain why!

   As of right now, I'm really enjoying Redux...I think that Context API will be much easier to work with once I use it more and get more comfortable with it. One of the things I appreciate about Redux is that the steps seem clear to me and I can see where a good flow can be developed in using it.
