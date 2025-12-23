```mermaid
flowchart TD
    A@{ shape: circle, label: "Mulai" }
    B@{ shape: lean-r, label: "Input : r" }
    C@{ shape: diamond, label: "r % 7 == 0" }
    D@{ shape: rect, label: "π = 22/7" }
    E@{ shape: rect, label: "π = 3.14" }
    F@{ shape: rect, label: "luasLingkaran = π * r * r" }
    G@{ shape: lean-r, label: "Output : luasLingkaran " }
    H@{ shape: rect, label: "kelilingLingkaran = 2 * π * r" }
    I@{ shape: lean-r, label: "Output :  kelilingLingkaran" }
     J@{ shape: dbl-circ, label: "Selesai" }




    A --> B
    B --> C
    C -- True --> D
    C -- False --> E
    D --> F
    E --> F
    F --> G
    G --> H
    H --> I
    I --> J

```
