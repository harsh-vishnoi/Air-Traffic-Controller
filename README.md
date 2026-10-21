# Air Traffic Controller

A console program that treats eleven Indian airports as a weighted graph. `airport` stores the network. `planes` extends it with seat inventory, a waiting list, and reservation records.

Distances are fixed edge weights. Ticket price follows the shortest-path distance. Every airport is not linked to every other airport.

## Airports

| Id | Name | Id | Name |
| --- | --- | --- | --- |
| 0 | Srinagar | 6 | Hyderabad |
| 1 | Delhi | 7 | Goa |
| 2 | Ahmedabad | 8 | Chennai |
| 3 | Bhopal | 9 | Thiruvananthapuram |
| 4 | Kolkata | 10 | Port Blair |
| 5 | Mumbai | | |

The names are printed by `display()` in `ATC/Air_traffic_controller.cpp`. A few spellings in that menu differ from the table above.

## Menu

1. Shortest path between two airports (Floyd–Warshall).
2. Minimum ticket price on that shortest path.
3. The airports along the path.
4. How many walks exist between two airports when the number of stops is limited.
5. Reserve seats, with a waiting list when the flight is full.
6. Cancel a seat.
7. List booked passengers (name, age, seat).
8. Launch `ATC/timetesting.cpp` in a new GNOME terminal. This option is hard-coded to a local Desktop path and only applies on that machine.

## Build

The program uses POSIX `unistd.h` and ANSI color codes.

```bash
g++ ATC/Air_traffic_controller.cpp -o atc
./atc
```

`timetesting.cpp` is a separate binary used by menu option 8. It is not linked into `atc`.
