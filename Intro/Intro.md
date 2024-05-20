## DOM -  Document Object Model

### Standardized interface that describes a web page

- Fundamental building block of a website
- Cross language and cross platform
- All frameworks build on top of DOM
- Gives you insight in to higher level abstraction you may use
- Pre requisite to learn any front end frameworks and tools.

### Three main parts associated with the window object in JavaScript.

- The window object is a global object in the browser environment that represents the window or tab in which the script is running.

| Part        | Description                                                                 | Key Components                                                                                                                                                   |
|-------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BOM         | Browser Object Model, provides methods and properties for interacting with the browser window. | `window`, `navigator`, `screen`, `location`, `history`, `alert()`, `confirm()`, `prompt()`                                                                       |
| DOM         | Document Object Model, a programming interface for HTML and XML documents.   | `document`, elements (e.g., `div`, `span`, `a`), methods for traversing and modifying the document (e.g., `getElementById()`, `querySelector()`, `createElement()`) |
| JavaScript  | The programming language used to manipulate the BOM and DOM.                 | Core language features (variables, functions, loops, conditional statements), built-in objects (`Array`, `Date`, `Math`, `RegExp`), event handling               |


### What can the DOM do ?
- Create, Read, Update and Delete HTML and CSS on webpage.
- Change attribute of elements on webpage.
- Create, Read, Update and Delete Events that are on webpage.
- Create our own Custom Events to add to the webpage.
- Create our own Custom Elements to put on the webpage

# Types of Nodes in the DOM

| Node Type              | Description                                                            | Node Type Value | Example                                       | Additional Information                                                                  |
|------------------------|------------------------------------------------------------------------|-----------------|-----------------------------------------------|-----------------------------------------------------------------------------------------|
| Element Nodes          | Represent HTML or XML elements                                         | 1               | `<div>`, `<p>`, `<a>`                         | Most common node type; can have attributes, styles, and child nodes.                    |
| Text Nodes             | Represent the text content inside elements                             | 3               | Text "Hello, world!" in `<p>Hello, world!</p>`| Contain only text data; cannot have child nodes.                                        |
| Attribute Nodes        | Represent the attributes of elements                                   | 2               | `class` in `<div class="example">`            | Modern DOM APIs handle attributes as properties of elements rather than separate nodes. |
| Comment Nodes          | Represent comments in the document                                     | 8               | `<!-- This is a comment -->`                  | Useful for leaving notes in the source code; not visible in the rendered document.      |
| Document Nodes         | Represent the entire document                                          | 9               | `document` object                             | The root node of the document tree; provides access to the entire document.             |
| Document Type Nodes    | Represent the document type declaration                                | 10              | `<!DOCTYPE html>`                             | Declares the document type and version (e.g., HTML5); affects document parsing.         |
| Document Fragment Nodes| Represent a minimal document object used as a lightweight container    | 11              | `document.createDocumentFragment()`           | Used to build and manipulate parts of a document offscreen before adding them to the DOM|
| CDATA Section Nodes    | Represent a CDATA section in XML, used to include unparsed text        | 4               | `<![CDATA[Some unparsed content]]>`           | Primarily used in XML documents to include data that should not be parsed.              |

### Example of Node Types in JavaScript

```javascript
// Creating an element node
const elementNode = document.createElement('div');
console.log(elementNode.nodeType); // Output: 1

// Creating a text node
const textNode = document.createTextNode('Hello, world!');
console.log(textNode.nodeType); // Output: 3

// Creating a comment node
const commentNode = document.createComment('This is a comment');
console.log(commentNode.nodeType); // Output: 8

// Accessing the document node
console.log(document.nodeType); // Output: 9

// Creating a document fragment
const fragmentNode = document.createDocumentFragment();
console.log(fragmentNode.nodeType); // Output: 11

