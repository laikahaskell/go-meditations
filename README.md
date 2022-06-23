# go-meditations
A Go program that outputs a random passage from the Meditations by Marcus Aurelius. 
The TUI interface is from [Bubbletea](https://github.com/charmbracelet/bubbletea/) by Charmbracelet.

## Usage and Dependencies
A `go.mod` file is provided with all used packages. Run `go run main.go` or compile with `go build` and run the executable (`medi`).

## About

### The Code
The implementation of the Bubbletea model and Bubbles interface are largely borrowed from the [Pager](https://github.com/charmbracelet/bubbletea/blob/master/examples/pager/main.go) example from the bubbletea repository, but I added text wrapping, from [Reflow](https://github.com/muesli/reflow).

### The Text
I used the [1944 translation by Arthur Spenser Loat Farquharson](https://en.wikisource.org/wiki/The_Meditations_of_the_Emperor_Marcus_Antoninus), which is in the public domain. 
In order to be processed cleanly, I edited the text myself by removing everything except Aurelius's text, 
numbering every line with a bible-style `chapter:line` system (including breaking long packages into sub-lines) 
and eliminating all other extraneous text and empty lines.

## TODO
* "Start page" to select chapter/passage.
* Make the wrapping respond to terminal text resize
