### Full Stack Open Course

https://fullstackopen.com/en/about

```markdown
Status:

[x] Part 0
    [x] 0.1: HTML
    [x] 0.2: CSS
    [ ] 0.3: HTML Forms
    [ ] 0.4: New note diagram
    [ ] 0.5: Single page app diagram
    [ ] 0.6: New note in single page app diagram
[ ] Part 1
[ ] Part 2
[ ] Part 3
[ ] Part 4
[ ] Part 5
[ ] Part 6
[ ] Part 7
[ ] Part 8
[ ] Part 9
[ ] Part 10
[ ] Part 11
[ ] Part 12
[ ] Part 13
```

---

# 1. Part 1

### RULE 1: Always keep developer console open. (Network Tab) (Disable Cache)

- command: cmd+opt+i/fn+F12
- server and browser communicate using "HTTP Protocol"
- Steps for loading image in a webpage that happen in backend:

  - Broser sends HTTP GET request to server
  - server fetches HTML Code pf page
  - img tag in html prompts broseer to fet image
  - browser renders HTML page + image to screen
- The [head](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head) section of the HTML contains a [script](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script) tag, which causes the browser to fetch a JavaScript file called *main.js* . Immediately after fetching the *script* tag, the browser begins to execute the code.
- This output on the console is caused by the *console.log* command in the code:
- ```html
  const data = JSON.parse(this.responseText)
  console.log(data)
  ```
- We can think of HTML pages as implicit tree structures.
- ```html
  html
    head
      link
      script
    body
      div
        h1
        div
          ul
            li
            li
            li
        form
          input
          input
  ```

  - The same treelike structure can be seen on the console's *Elements* tab.
- [AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) (Asynchronous JavaScript and XML)

  - Introduced in 2005 (20 years back 🤯)
  - Fetching content to webpages using JS included within HTML
- [Single-page application](https://en.wikipedia.org/wiki/Single-page_application) (SPA) style of creating web applications has emerged in these days.

  - Comprise only one HTML page fetched from the server, the contents of which are manipulated with JavaScript that executes in the browser.
- JavaScript Libraries:

  - ever-so-popular [jQuery](https://jquery.com/).
    - has cross-browser compatibility.
  - Facebook's [React](https://react.dev/) library

### Course Tech Stacks:

- Backend -> JavaScript using Node.js runtime environment
- Frontend -> JavaScript

## Exercises

The exercises are submitted **one part at a time** . When you have submitted the exercises for a part, you can no longer submit any missed exercises for that part.

#### 0.1: HTML

Review the basics of HTML by reading this tutorial from Mozilla: [HTML tutorial](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics).

*This exercise is not submitted to GitHub, it's enough to just read the tutorial*

#### 0.2: CSS

Review the basics of CSS by reading this tutorial from Mozilla: [CSS tutorial](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics).

*This exercise is not submitted to GitHub, it's enough to just read the tutorial*

#### 0.3: HTML forms

Learn about the basics of HTML forms by reading Mozilla's tutorial [Your first form](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Your_first_HTML_form).

*This exercise is not submitted to GitHub, it's enough to just read the tutorial*

#### 0.4: New note diagram

In the section [Loading a page containing JavaScript - review](https://fullstackopen.com/en/part0/fundamentals_of_web_apps#loading-a-page-containing-java-script-review), the chain of events caused by opening the page [https://studies.cs.helsinki.fi/exampleapp/notes](https://studies.cs.helsinki.fi/exampleapp/notes) is depicted as a [sequence diagram](https://www.geeksforgeeks.org/unified-modeling-language-uml-sequence-diagrams/)

The diagram was made as a GitHub Markdown-file using the [Mermaid](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams)-syntax, as follows:

```text
sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: the css file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: the JavaScript file
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notescopy
```

**Create a similar diagram** depicting the situation where the user creates a new note on the page [https://studies.cs.helsinki.fi/exampleapp/notes](https://studies.cs.helsinki.fi/exampleapp/notes) by writing something into the text field and clicking the *Save* button.

If necessary, show operations on the browser or on the server as comments on the diagram.

The diagram does not have to be a sequence diagram. Any sensible way of presenting the events is fine.

All necessary information for doing this, and the next two exercises, can be found in the text of [this part](https://fullstackopen.com/en/part0/fundamentals_of_web_apps#forms-and-http-post). The idea of these exercises is to read the text once more and to think through what is going on there. Reading the application [code](https://github.com/mluukkai/example_app) is not necessary, but it is of course possible.

You can do the diagrams with any program, but perhaps the easiest and the best way to do diagrams is the [Mermaid](https://github.com/mermaid-js/mermaid#sequence-diagram-docs---live-editor) syntax that is now implemented in [GitHub](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/) Markdown pages!

#### 0.5: Single page app diagram

Create a diagram depicting the situation where the user goes to the [single-page app](https://fullstackopen.com/en/part0/fundamentals_of_web_apps#single-page-app) version of the notes app at [https://studies.cs.helsinki.fi/exampleapp/spa](https://studies.cs.helsinki.fi/exampleapp/spa).

#### 0.6: New note in Single page app diagram

Create a diagram depicting the situation where the user creates a new note using the single-page version of the app.

This was the last exercise, and it's time to push your answers to GitHub and mark the exercises as done in the [submission system](https://studies.cs.helsinki.fi/stats/courses/fullstackopen).
