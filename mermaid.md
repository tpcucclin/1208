## Mermain

- [Mermaid: Generate diagrams from markdown-like text.](https://github.com/mermaid-js/mermaid/blob/develop/README.md)
- [Mermaidv10.5.0 Live Editor](https://mermaid.live/)
- [A Mermaid User-Guide for Beginners](https://mermaid.js.org/intro/getting-started.html)
- [How to Create Diagrams as Code with Mermaid, GitHub, and Visual Studio Code (SEPTEMBER 6, 2023)](https://www.freecodecamp.org/news/diagrams-as-code-with-mermaid-github-and-vs-code/)

#### [Flowcharts - Basic Syntax](https://mermaid.js.org/syntax/flowchart.html)
```mermaid
---
title: Node
---
flowchart LR
    id
```

#### [A node with text](https://mermaid.js.org/syntax/flowchart.html)
```mermaid
flowchart LR
    id["This ❤ Unicode"]
```

#### [Markdown formatting](https://mermaid.js.org/syntax/flowchart.html)
```mermaid
flowchart LR
    markdown["`This **is** _Markdown_`"]
    newLines["Line 1
    Line 2
    Line 3"]
    markdown --> newLines
```

### [An invisible link](https://mermaid.js.org/syntax/flowchart.html#an-invisible-link)

LR vs. TD 隱藏的鏈結線 

```mermaid
flowchart LR
    A ~~~ B ~~~ C
    D ~~~ E ~~~ F
```

```mermaid
flowchart TD
    A ~~~ B ~~~ C
    D ~~~ E ~~~ F
```

### [Chaining of links](https://mermaid.js.org/syntax/flowchart.html#chaining-of-links)
###
```mermaid
flowchart LR
   A -- text --> B -- text2 --> C
```
```mermaid
flowchart LR
   a --> b & c--> d
```

```mermaid
graph LR
   A --> B
   A -->C
   C -->D
```

```mermaid
graph LR;
    A--> B & C & D;
    B--> A & E;
    C--> A & E;
    D--> A & E;
    E--> B & C & D;
```

```mermaid
flowchart LR
    A --o B
    B --x C
```

#### [State diagrams](https://mermaid.js.org/syntax/stateDiagram.html)
```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]
%% this is a comment
    Still --> Moving
    Moving --> Still %% another comment
    Moving --> Crash
    Crash --> [*]
```

#### [Apply classDef styles to states](https://mermaid.js.org/syntax/stateDiagram.html#apply-classdef-styles-to-states)
```mermaid
   stateDiagram
   direction TB

   accTitle: This is the accessible title
   accDescr: This is an accessible description

   classDef notMoving fill:white
   classDef movement font-style:italic
   classDef badBadEvent fill:#f00,color:white,font-weight:bold,stroke-width:2px,stroke:yellow

   [*]--> Still
   Still --> [*]
   Still --> Moving
   Moving --> Still
   Moving --> Crash
   Crash --> [*]

   class Still notMoving
   class Moving, Crash movement
   class Crash badBadEvent
   class end badBadEvent
```

```mermaid
flowchart TD
  A[Christmas] -->|Get money| B(Go shopping)
  B --> C{Let me think}
  C -->|One| D[Laptop]
  C -->|Two| E[iPhone]
  C -->|Three| F[fa:fa-car Car]
``` 

```mermaid
pie title Pets adopted by volunteers
  "Dogs" : 386
  "Cats" : 85
  "Rats" : 35
```

```mermaid
flowchart TD
A[Deploy to production] --> B{It is Friday};
B -- Yes --> C[Do not deploy!];
B -- No --> D[Run deploy.sh to deploy!];
C ----> E[Enjoy your weekend!];
D ----> E[Enjoy your weekend!];
```

```mermaid
gitGraph
       commit
       commit
       branch develop
       commit
       commit
       commit
       checkout main
       commit
       commit
```

```mermaid
graph TD
A[1*1=1] -->|" "| B[1*2=2]
A -->|" "| C[1*3=3]
A -->|" "| D[1*4=4]
A -->|" "| E[1*5=5]
A -->|" "| F[1*6=6]
A -->|" "| G[1*7=7]
A -->|" "| H[1*8=8]
A -->|" "| I[1*9=9]

B -->|" "| J[2*2=4]
C -->|" "| K[3*3=9]
D -->|" "| L[4*4=16]
E -->|" "| M[5*5=25]
F -->|" "| N[6*6=36]
G -->|" "| O[7*7=49]
H -->|" "| P[8*8=64]
I -->|" "| Q[9*9=81]
```

```mermaid
classDiagram
    class Animal {
        +name: string
        +age: int
        +makeSound(): void
    }

    class Dog {
        +breed: string
        +bark(): void
    }

    class Cat {
        +color: string
        +meow(): void
    }

    Animal <|-- Dog
    Animal <|-- Cat
```

```mermaid
gantt
    title Project Schedule
    dateFormat YYYY-MM-DD
    axisFormat %m/%d

    section Planning
    Define Project : 2023-01-01, 7d
    Research : 2023-01-08, 14d
    Define Requirements : 2023-01-22, 7d

    section Development
    Design : 2023-01-29, 21d
    Implementation : 2023-02-19, 28d

    section Testing
    Unit Testing : 2023-03-19, 14d
    Integration Testing : 2023-04-02, 14d

    section Deployment
    Deploy : 2023-04-16, 7d
    User Training : 2023-04-23, 14d

    section Maintenance
    Ongoing Support : 2023-05-07, 30d

```


```mermaid
flowchart TD;
 A[開始] -->B[/讀入 硬幣數量, 期望金額 /]
 B --> C[/讀入 硬幣種類/]
 C --> D[/"建立 dp list 大小為期望金額+1,<br> dp[i] 代表達成金額的方法數, 且dp[0]=1"/]
 D --> E("for 針對每種硬幣面額 <br> for 金額 0 to 期望金額")
 E --> 結束
 F --> |條件為真| H("dp[金額] +=  dp[金額 - coin]")
 E --> F{金額 - count >=0}
 F -->  |條件為否| E
 H --> E
```

```mermaid

 graph TD
 id1[方框] -->
 id2(帶有圓角的方框) -->
 id3([體育場形狀]) -->
 id4[[子例程]] -->
 id5[(圓柱狀)]-->
 id6((圓形))
 id7>非對稱形狀] -->
 id8{菱形} -->
 id9{{六角形}}
 id10[/平行四邊形1/] -->
 id11[\平行四邊形2\] -->
 id12[/梯形1\] -->
 id13[\梯形2/]
```
