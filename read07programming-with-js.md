Read 07: Programming with JavaScript

JavaScript & JQuery (makes JS easier)

## How JS makes web pages more interactive
+ Access content, modify content, program rules, react to events
+ viewport = bottom of the viewable area in browser window
+ Access content - elements, text, attributes
+ Modify content - elements, text, attributes
+ Program rules - set steps for browser to follow
+ React to events - button pressed, link clicked or tapped, cursor hovers, info added to form, time passed, page finished loading

## Examples of JS in Browser
+ Slideshows
+ Forms - checking whether filled in correctly
+ Reload page part - faster and not whole thing needs refreshing
+ Filtering data

## Clarifying HTML & CSS
+ HTML elements
  + (opening closing tags + content)
  + opening tags can carry attributes
  + e.g. `<p class (attrib name)="fruit" (attrib value)>peach</p>`
+ CSS rules
  + how contents of elements should be displayed in the browser
  + each rule has a selector and declaration block
    + selector - indicates which element the rule applies to
    + declaration contains rules that indicate how the element should appear
      + property (aspect you want to control)
      + value (setting for the property)
  + e.g. `.fruit (selector) {color (property name): pink (property value);} ({} is declaration block)`

## Scripts
+ Define your goal - state your goal first, then list the tasks to achieve it
+ Design your script - flowchart
+ Code each step using js
+ vocabulary - words computers understand
+ syntax - how you put the words together to create insturctions computers can follow

## Functions
+ let you group a serioes of statement together to perform a specific task
+ "Calling the function" - ask the function to perform it's task
+ parameters - pieces of info passed to a function
+ return value - functions response or answer
+ name/value pairs
+ functions can be named or anonymous
+ functions like a recipe card for steps to be followed
+ function is any one of those recipes, program is made up of multiple functions executed or "called" to execute
+ declaring a function
+ calling a function
+ parameters used like variables within the function = ingredients (width, height)
+ parameters - what's in the function declaration
+ arguments used to run your code in your function
+ function name or anonymous - name of recipe
+ return value - output (food you make)
+ DRY - principle of Don't Repeat Yourself
+ variable scope - create a new function, create a new scope - a limitation to what's accessible, what you see
+ parenthesis invoke the function
+ functions can call functions, which can call oher functions etc.
+ prompts as method of input
+ assignment operator (= sign)
+ output += or output = output +
+ a function allows you to have multiple returns
+ assign what you are doing in each variable - KEY: even if you don't put in a return statement, it returns "undefined" - this is the return
+ JS - No, undefined, false, empty string, 0 - if you see "undefined" popping up good indicator that have a function not specifying a return value
+ Number() converts a number into a number
+ String() converts to a string
+ 'What\'s the time?' or "what's the time?" - single quotes minor processing speed faster
+ || double pike = "or"
+ '' - empty string is considered false, all other string true
+ 0 is always false