## Functional Componets

Basic Structure : 
```JS
import  React ,{useState} from 'react';

const Xcomp = props {
  //blah blah
  }
 export deafault Xcomp;
 ```
 - Can access to State (using useState method)
 - Can't manage Lifecycle Hooks 
 
 ## Class-based Compnents
 
 Basic Structure :
 
 ```JS
 import React ,{component} from 'react' ;
 
 class Xcomp extends componet {
  constructor(props) {
    super(props)
   }
  //blah blah
  }
  export deafult Xcomp
 ```
 
 - Can access to State (using setState method)
 - Can manage Lifecycle Hooks 
 
 
  ## Component Lifecycle
  
  Benefit for handling Lifecycle : In applications with many components, it’s very important to free up resources taken by the components when they are destroyed so we can have better performance

 **It can be optimized your application especially if it is big application**
  
  ### Component Creation Lifecycle 
  
  1) Constructor executes : Basic Initialization of values
  2) getDerivedStateFromProps(props, state) : It should return an object to update the state, or null to update nothing.
  3) render() : rendering JSX code
  4) Redering Child Components
  5) componentDidMount() : can have `HttpReqeust` or some `API` call but it shouldn't update the `state`
  
  
  ### Component Update Lifecycle
    
  1) getDerivedStateFromProps(props, state) : Update components based on outside props
  2) **shouldComponentUpdate(nextProps, nextState)** : It can control which component will be updated whether depends one their returning values so it can be used for performance optimization
  3) render()
  4) Update Child Components
  5) getSnapShotBeforeUpdate(prevPros, prevState) : can be used for update the DOM
  6) componentDidUpdate(prevProps, prevState, snapshot) : can have `HttpReqeust` or some `API` call

  
  
  
