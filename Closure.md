                                                 CLOSURE


                           A function that “closes over” some local variables is called a closure. 
                                                         (authors  definition eloquentjavascript)


A closure is a function that can have free variables together with the scope that binds those variables. We use inner functions, functions definitions and function expressions in JavaScript that are inside another function. The inner functions have an access to all of the local variables, parameters and declared inner functions within their outer function(s). When one of the inner function is accessed outside of the function in which it was contained, so that it may be executed after the outer function has returned, a closure is formed.

Function makeAdder(x){
      return function(y){
                   return x+y;
}
}

var add5= makeAdder(5);
var add10= makeAdder(10);

Console.log(add5(2));//7
Console.log(add10(2));//12

Here function makeAdder(x), takes argument x and returns a new function which further takes argument y and returns their sum(x+y). Here add5  & add10 are the closures

* A local variable for a function that is still alive after the function has returned is a closure.
* Furthermore, closure can be assumed as a stack frame which is not deallocated when the function returns.

In short, Closure has access to 3 things
* Its own scope
* Outer functions variables
* To global variables.

REFERENCES –
* https://developer.mozilla.org
* http://javascriptissexy.com/understand-javascript-closures-with-ease/
* http://javascriptissexy.com/understand-javascript-closures-with-ease/

