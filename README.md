# web_witness

> A minimalist online web version of a popular puzzle game (grid puzzles only)

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

## The To-do List:
### The Front End
- [ ] HTML (Vue)
	- [ ] Load scripts
		- [ ] p5 for canvas drawing
	- [ ] Title Bar
		- [ ] Logo in the center
			- [ ] Different logo depending on current page?
		- [ ] Menu drawer on right side for navigation
	- [ ] Home 
		- [ ] Size canvas to screen
		- [ ] Draw special linear maze with multiple exits
		- [ ] Label exits (log in sign up, about, etc)
		- [ ] Depending on the exit chosen, redirect to corresponding page
	- [ ] Game
		- [ ] Size canvas to fit screen/window
		- [ ] Draw cursor
		- [ ] Draw maze from data
			- [ ] Draw points as circles
			- [ ] Draw connection as rects between points
			- [ ] Entrance is big circle on a point
			- [ ] Exit extends out of maze
		- [ ] Draw path through maze
			- [ ] Path follows cursor
			- [ ] Must must start from an entrace
			- [ ] If path reaches an exit, check that all rules have been satisfied
				- [ ] idk how rules are going to be implemented honestly
			- [ ] If path starts at entrance, ends at exit, all rules are satisfied, then maze is "solved", transition to next maze
			- [ ] Path color
				- [ ] Being drawn (usually soft white)
				- [ ] Reached exit (pulses brighter)
				- [ ] Solution correct (usually a lighter shade matching the background)
				- [ ] Solution incorrect (turn black and fade out)
				- [ ] Path cancel (fade out)
		- [ ] Transition between mazes
			- [ ] Unload/Load animation
		- [ ] Audio
			- [ ] Monitor on/off
			- [ ] Panel focus
			- [ ] Entrance pulse
			- [ ] Exit pulse
			- [ ] Draw start
			- [ ] Draw cancel
			- [ ] Exit reached
			- [ ] Solution correct
			- [ ] Solution incorrect
	- [ ] Make it look pretty
		- [ ] CSS
		- [ ] Nice transitions between puzzles
		- [ ] Color transitions
	- [ ] User interaction
		- [ ] Mouse
		- [ ] Touch
	- [ ] Pre-load maze data
		- [ ] Eventually replace with requesting maze data from server
	- [ ] Audio would be a nice touch
- [ ] CSS
	- [ ] I really like Materialize

### The Back End
- [ ] Express server
	- [ ] User requests new maze
	- [ ] Respond with maze data
	- [ ] Rate limiting?
	- [ ] Log in accounts with stats?
- [ ] MongoDB
	- [ ] Maze data stored as json
		- [ ] Array of points/nodes
		- [ ] Array of connections
			- [ ] Different types of connection (unbroken/broken/deadend)
			- [ ] Array of rules
				- [ ] All rules must be satisfied for maze to be "solved"
			- [ ] Entrance(s)/Exit(s)
			- [ ] Color

### Future
- [ ] Add new rules?
- [ ] New game modes
	- [ ] User-made mazes
		- [ ] Client maze editor
		- [ ] User can share their mazes with others
			- [ ] Store on server?
				- [ ] Makes req/res simple
				- [ ] Requires storage 
			- [ ] Encode maze data in URL?
				- [ ] No storage required
				- [ ] Mazes are generated from URL on the fly
	- [ ] Auto-generated mazes (infinite mode)
	- [ ] The Gauntlet 
		- [ ] Complete a set number of puzzles within a time limit

