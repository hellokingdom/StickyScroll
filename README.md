#jQuery StickyScroll

Make elements stick to browser window as you scroll

## UPDATE

<del>Stickyscroll performs *very* badly in the current versions of Chrome and Firefox
at the time of this writing, and I'm not sure I'm capable of fixing it without
stripping it down to next to nothing. So, development is not very active right
now. If you'd like to see an example of the problem stripped down to its most
basic case, see the `demo-basic.html` file. Look at the source in that file and
see if you have any ideas to make it work again. It looks to me like the
`window.onscroll` function just doesn't fire enough to make this a viable option
anymore.</del>

Fork using CSS classes instead of positioning elements, should fix issues on browsers that support position fixed.

##Usage:
- `$('selector').stickyScroll({ container: .container, offset: 20 })`


Adds the following classes to the selected element:

`.fixed-top`
`.fixed`
`.fixed-bottom`

Example CSS:

      .fixed {
	      position:fixed;
	      top:20px; // Offset height
		  width:100%;
  	  }
  	  .fixed-bottom {
	      position:absolute;
		  top:auto;
	      bottom:0;
		  width:100%;
  	  }
	  .container {
		  position:relative;	  
	  }