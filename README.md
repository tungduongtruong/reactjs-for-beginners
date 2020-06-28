# reactjs-for-beginners
React JS for Beginners

> React JS - A JavaScript library for building user interfaces

[](https://techfinally.com/wp-content/uploads/2020/06/reactjs-logo.svg =150x) (React JS - A JavaScript library for building user interfaces)

React (also known as React.js or ReactJS) is an open-source JavaScript Library for building User Interfaces. It is maintained by Facebook and a community of individual developers and companies.

React is used to build Single Page Applications and React allows us to create reusable UI components.

## 1. History

React was created by Jordan Walke, a software engineer at Facebook, who released an early prototype of React called "FaxJS". It was first deployed on Facebook's News Feed in 2011 and later on Instagram in 2012. It was open-sourced at JSConf US in May 2013.

Current version of React is V16.13.0 (26 February 2020).

## 2. Virtual DOM

[What is the DOM?](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

A Web page is a document. This document can be either displayed in the browser window or as the HTML source. But it is the same document in both cases. The Document Object Model (DOM) represents that same document so it can be manipulated. The DOM is an object-oriented representation of the web page, which can be modified with a scripting language such as JavaScript.

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/220px-DOM-model.svg.png "Tree Structure of the Document Object Model")

Each time you make a change in the code, DOM will be completely updated and rewritten. This is an expensive operation and consumes lots of time. That's why, React provides a solution call is Virtual DOM.

What is the benefit of Virtual DOM?
- React first creates an exact copy of the DOM
- Then React figures out which part is new and only updates that specific part in the Virtual DOM
- Finally, React copies only the new parts of the Virtual DOM to the actual DOM, rather than completely rewriting it.

## 3. JSX

What is JSX? JSX stands for JavaScript XML, allows us to write HTML in React. JSX is basically used to write HTML tags inside JavaScript.

You don’t have to use JSX with React, but it is strongly recommended. JSX simplifies React and makes it easier to read.

```
import React from 'react';

class App extends React.Component {
   render() {
      return (
         <div>
            Hello World!!!
         </div>
      );
   }
}
export default App;
```

## 4. Components, Props and State

What are props?

Props is short for Properties and they are used to pass data between React components. React’s data flow between components is uni-directional (from parent to child only).
Props are Read-Only. The simple rule of thumb is props should not be changed.

```
class ParentComponent extends Component {    
    render() {    
        return (        
            <ChildComponent name="First Child" />    
        );  
    }
}

const ChildComponent = (props) => {    
    return <p>{props.name}</p>; 
};
```

What is state? 

Unlike props, State is internal to a component, while props are passed to a component. When state changes, the component responds by re-rendering.

State shouldn’t be modified directly – the setState(...) should be used

```
import React from 'react'

class Form extends React.Component {

  constructor(props) {
    super(props)
    this.state = {
      input: ''
    }
  }

  handleChangeInput = (text) => {
    this.setState({input: text})
  }

  render() {
    const {input} = this.state

    return (
      <View>
        <TextInput style={{height: 40, borderColor: 'gray', borderWidth: 1}}
                   value={input} onChangeText={this.handleChangeInput}/>
      </View>
    )
  }

}
```

## 5. Lifecycle


## Let’s Get Started!

React requires Node.js and if you don’t have Node.js on your computer, you can download it from [https://nodejs.org/en/download/](https://nodejs.org/en/download/).

After installing Nodejs, open your Terminal or Command Prompt and type the following command to create your React app and start.

```
npx create-react-app my-app
cd my-app
npm start
```
