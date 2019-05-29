HTML & CSS, Chapters 10 & 11: Introducing CSS - Duckett

# Introducing CSS: Thinking Inside the Box
* key is to imagine that there is an invisible box around every HTML element
* block and inline elements - block start new line, inline flow with text
* with CSS you can create rules to control presentation of each individual box
* styles - boxes, text, specific lists, tables and forms
* CSS associates style rules with HTML elements and affects how elements are displayed
* selectors indicate which element the rule applies to - e.g. "p" for paragraph
* declarations indicate how the elements should be styled - e.g. `font-family: Arial;`
* declarations sit inside {} curly brackets and have tow parts - property & value - property "font-family" and value "Arial" for example
* you can use CSS internally (within the HTML) and externally as a separate "style.css" file
* CSS selectors - there are many - pp 238 of Duckett - universal, type, class, ID, child, descendant, adjacent sibling, general sibling
* CSS - rules cascade - latter takes precedence, specific takes precedence, "!important" takes precedence (not suggested)
* CSS properties will be inherited by child elements
* browser quirks - you can check it out using sites listed on p 242

# Color
* color helps bring life and convey mood in your site
* you can specify colors using RGB, hex codes and color names
* color pickers are a great way to find colors
* contrast is critical to making the site readable and comfortable to read without straining
* CSS3 allows for RGB to indicate a level of opacity - RGBA
* CSS3 lets you specifi colors as HSL values too, with the option to use opactiy - HSLA