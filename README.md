# Urban Infrastructure Inspection System

A console-based Java system for urban infrastructure inspection, featuring sorting benchmarks and Dijkstra-based route planning.

## Academic Context

| Field | Details |
| --- | --- |
| University | Xi'an Jiaotong-Liverpool University (XJTLU) |
| Module | CPT204 — Advanced OO Programming |
| Project type | Group coursework |
| Portfolio owner | Junyan He (team member) |

This project was developed collaboratively as a group coursework submission.

## Run

Compile from the project root on Windows PowerShell:

```powershell
javac -d out (Get-ChildItem -Recurse src -Filter *.java).FullName
```

Compile from the project root on macOS/Linux:

```sh
javac -d out $(find src -name "*.java")
```

Run the final experiment with the default `Data` folder:

```sh
java -cp out app.Main Data
```

The default run uses 30 measurement rounds and 5 warm-up rounds for each sorting algorithm. Optional arguments can still provide the data folder, measurement rounds, and warm-up rounds:

```sh
java -cp out app.Main Data 30 5
```

The program prints report-ready evidence for:

- Bubble Sort, Quick Sort, and Merge Sort runtime comparison with mean, median, standard deviation, minimum, maximum, and CV.
- Extra explainability sections for Dataset Profile, cross-dataset stability, Time and Space Decision Support, graph edge-weight assumptions, and Path Metrics.
- Top 10 selected locations from candidates A, B, and C.
- The four required shortest-path cases using Dijkstra on the full undirected graph.
- Validation checks for dataset size, unique ids, sorting agreement, graph construction, selected target existence, path endpoints, waypoint order, and path cost.

