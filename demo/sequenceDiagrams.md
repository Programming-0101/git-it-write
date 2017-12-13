# Sequence Diagrams

[Sequence Diagrams](https://mermaidjs.github.io/sequenceDiagram.html) can be rendered using the [mermaid](https://mermaidjs.github.io/) library as an in-browser transformation of the markdown code block to an SVG image.

```mermaid
sequenceDiagram
    Alice ->> Bob: Hello Bob, how are you?
    Bob-->>John: How about you John?
    Bob--x Alice: I am good thanks!
    Bob-x John: I am good thanks!
    Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

    Bob-->Alice: Checking with John...
    Alice->John: Yes... John, how are you?
```
