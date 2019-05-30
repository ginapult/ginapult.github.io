#Web Site Development 

Summary: This page summarizes learnings from Duckett's Chapters on HTML Process & Design (C. 18), Structure (C. 1), HTML5 Layout (C. 17), and Extra Markup (C. 8)

## HTML Process & Design (Duckett C. 18)
+ Users/audience
+ Organize information
+ Design theory
+ Design tips

### Summary
+ understand your target audience - why they come to your site, what they want to find and when they're likely to return
+ site maps allow a pln for the stucture of the site
+ wireframes allow for organizing the info on each page
+ design is about communicating - visual hierarchy helps visitors understand what you're trying to tell them
+ differentiate through size and color and style
+ use grouping and similarity to help simplify info

### Who's the site for? (Target Audience)
+ "the entire world" doesn't work
+ Target audiences
  + Individuals
    + Age range
    + Appeal to men/women? mix?
    + Country
    + Urban/rural
    + Average income
    + Education
    + Marital/family status
    + Occupation
    + Hours they work per week
    + Frequency of web usage
    + Devices used to access web
  + Companies
    + Size
    + Department
    + Position
    + For selves or others
    + Budget

User Personas - fictional visitors from typical target audience; you can come back to these "friends" while asking questions thorugh teh deveopment process.

### Why are the users coming to the site? (Key motivations > Specific goals)
+ General entertainment or specific goal?
+ If specific, personal or professional?
+ Essential or luxury?
+ Specific goals
  + general info or specific fact or product
  + need intro or already familiar
  + time sensitive info
  + info to know whether to buy
  + need to contact you or physically visit you

### What are the users try ing to achieve? (Key tasks and motivations)
+ Create a list of reasons users would come to the site
+ Then assign tasks to the user personas

### What information do your users need?
+ Use reasons list above to determine what is needed to achieve their goal
+ Prioritize info from key points down to non-essential or background info

#### Questions to help decide on what info to provide:
+ Are users familier with subject area/brand/product/service or need intro?
+ What are the most impo features you're offering?
+ What is special/differentiates you from others similar?
+ Once people have achieved goal of site, what common questions are there?

### How often do users visit the site?
+ Gives an idea of how often to update, and what parts when
+ Goods/services
  + how often do the same people return?
  + how often is your stock updated or service changed?
+ Information
  + How often is the subject updated?
  + What % of users would return for regular updates vs just once?

## Site Maps
Use **card sorting** to create site maps
+ ask target audience to help you group related info together
+ remember to focus on the goals of the users - what they're wanting to achieve

## Wireframes
+ focuses on function, not design
+ helpful to start here with client so not distracted by how the site looks
+ should show how you've prioritized the information
+ can use Photoshop, Illustrator, and InDesign
+ insert wireframe image here

## Visual Design = Communication
Communication = organizing and prioritizing information/content
+ **Visual hierarchy** - where attention is drawn - created by adding **visual contrast**
  + Size, color, style
  + Images
+ Grouping & Similarity
  + Headers help with screen readers

### Designing Navigation
+ No more than eight links at primary nav - one word each - sections of site, not ancillary like logins, search, legal etc.
+ concise - no more than eight links
+ clear - predictable info should beon the page - choose single descriptive words rather than phrases
+ selective - logins and search and legal information should not be on the nav, best on other places on the page
+ context - use visual marker to indicate the current page
+ interactive - big enough to click on, link change when hovered over or clicked on, visually distinct from other content
+ consistent - secondary nav can change, but primary should remain exactly the same throughout the site

## HTML Structure (Duckett C. 1)
+ HTML pages are text documents
+ HTML uses tags that sit inside <> (angled brackets)
+ tags referred to as "elements"
+ tags come in pairs usually - opening and closing tags
+ opening tags carry attributes - tell us more about the content of the element - require a NAME and a VALUE

+ pages use structure - think of it like a newspaper
  + each story has a headline, text and images
  + subheadings for long articles
  + quotes
  + HTML code is made of characters within angled brackets - "elements" e.g. `<body></body>` - tags act like containers - tags we add are the markup
  + attribute name (e.g. `<p lang=`) and attribute value (e.g. `"en-us"`)
  + body, head, title

## HTML5 Layout (Duckett C. 17)
+ <div> elements are often used as containing elements to group sections of a page together
+ browsers display pages in normal flow unless you specify relative, absolute, or fixed positioning
+ The "float" property moves content to the left or right of the page and can be sused to create multi-column layouts - they require a defined width
+ Pages can be fixed width or liquid (stretchy) layouts
+ designers keep pages within 960-1000 pixels wide, and indicate what site is about within top 600 pixels
+ grids help create professional and flexible designs
+ CSS frameworks provide rules for common tasks
+ you can include multiple CSS files in one page

### Positioning

#### Key Concepts
+ HTML elements are like building blocks and CSS treats each element as if it's in its own box; 2 types:
  + block-level - start on a new line - e.g. h1, p, ul, li; if one is inside another, the outer box is the parent, inner box the child
    + <div> - common to group related elements inside a div - e.g. elements inside the header of a site like logo and main nav - the div is called in this case the "containing element"
  + inline - flow in between surrounding text - e.g. img, b, i

#### Controlling Element Position
+ positioning schemes (relative to containing element)
  + normal flow - all bclock-level element appears on a new line going down the page
  + relative positioning - shifts the position to the top, right, bottom or left of where it would have been placed
  + absolute positioning - move as users scroll up and down
+ box offset properties - tell the browser how far fromt he top ro bottom and left oright to place it
  + fixed positioning - this si about the element in relation to the browser window (vs the containing element) - do not move when user scrolls
  + floating elements - position the element to the far left or right of containing box - it becomes a blcok level  element around whichother content can flow
  + n.b. when you move any element from normal flow, boxes can overlap - use `z-index` property to control which box appears on top
+ position:
  + static - normal flow - don't need syntax because browser default
  + relative - `{position: relative; top: 10 px; left: 100px;}`element moved in relation to where it would have been in normal flow - top, bottom in pixels or % to normal
  + absolute - `{position: absolute; top: 0px; left: 500 px; width: 250 px;}` - box taken out of normal flow, not longer affects the position of other elements - they act like it's not there
  + fixed - `{position: fixed; top 0px; left: 0px; padding: 10px; margin: 0px, width: 100%; background-color}` - a type of absolute that requires property to have a value of fixed - positions in relation to the browder window - it stays in the same place
+ overlapping elements - z-index - `{position: fixed; width: 100%; z-index: 10;}` - this will appear over a lower z-index number and under a higher one
+ float - float and width must be used together to show how wide the floated element should be - `float: right; width: 275px;`
  + use this to pace elements side-by-side - `p { width: 230px; float: left: margin: 5px; padding: 5px; background color: #efefef;}`
  + clearing floats - no element shoud touch the left or right hand sides of the box - left, right, both, none - `p {float: left;} .clear {clear: left;}`
  + parents of only floated elements can "collapse" in some browsers; the fix is to add CSS rules to the containing element - `div { border: 1px solid #665544; overflow: auto; width: 100%;}
  + creating multi-column layouts - do this by using a div element to represent each column - see p 375!
+ layouts
  + fixed width - do not change size as the size of the browser window is changed by user - see page 383-384!
  + liquid layouts - stretch and contract as the user changes size of window - tend to use percentages - see page 385-386!
  + layout grids - designers use grids to help them arrange visual elements - consisten proportions and spaces - professional looking design - see pages 389-390 - 960.GS
+ stylesheets - some designers use separate stylesheets for layout vs font and colors etc. - some more odular - typography, layout, forms, tables

## Extra Markup (Ducket C. 8)
+ DOCTYPES - tell browsers which version of HTML
+ add comments using <!-- and --> markers
+ id (e.g. `<p id="pullquote">`) and class (e.g. `<p class+"important">` attributes allow for identifying particular elements - used to then assign format within CSS
+ div and span allow for grouping block-level and inline elements together
+ iframes cut windows on web pages through which other pages can be displayed
+ the meta tag allows to supply all kinds of info for the page
+ escape characters are used to include special characters such as >,<, and copyright  - pp 193-194!
+ block and inline elements
