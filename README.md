# Strudel Cycle

A small web page for seeing and editing one [Strudel](https://strudel.cc) cycle.

Strudel plays patterns on a loop where one cycle lasts 2 seconds by default. This page
shows that cycle as a timeline with four half-second steps. Each step has two note slots
that can be switched on or off, and the page turns your choices into Strudel mini-notation
and plays it.

## Running it

Open `index.html` in a browser. There is no build step and nothing to install; the Strudel
library is loaded from a CDN, so you need an internet connection.

## How the grid maps to Strudel

Each step becomes one entry in a `note("...")` string:

| Slots on | Result   | Meaning                                  |
|----------|----------|------------------------------------------|
| one      | `c4`     | the note fills the whole step            |
| both     | `[c4 e4]`| the two notes share the step evenly      |
| none     | `~`      | silence for that step                    |

Pick "rest" as a slot's note to shorten the other one: `[c4 ~]` plays C4 for a quarter
second, then nothing.

The code being played is shown under the grid, and a list of example patterns can be
loaded with one click.

## License

AGPL-3.0, matching the license of Strudel itself. See `LICENSE`.
