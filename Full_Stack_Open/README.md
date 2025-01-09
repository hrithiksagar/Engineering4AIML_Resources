### Full Stack Open Course

https://fullstackopen.com/en/about

```markdown
Status:

[x] Part 0
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
- Document Object Model, or [DOM](https://en.wikipedia.org/wiki/Document_Object_Model), is an Application Programming Interface (*API* ) that enables programmatic modification of the *element trees* corresponding to web pages.
-
