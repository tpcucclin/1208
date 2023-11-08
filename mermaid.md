#### Mermain

- [Mermaid: Generate diagrams from markdown-like text.](https://github.com/mermaid-js/mermaid/blob/develop/README.md)
- [Mermaidv10.5.0 Live Editor](https://mermaid.live/)
- [A Mermaid User-Guide for Beginners](https://mermaid.js.org/intro/getting-started.html)

```mermaid
graph LR
   A --> B
   A -->C
   C -->D
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
