# README

Todo-demo Tutorial 

Scrtch Pad

1.
Issue:  somewhere around Chapter 9 code as is here stopes rendering to browser.
Misc.  Seems to be related to using jQ wrapper, but this may be co-incidental.  Logs seem to without error codes until a SysErr 500 appears.  Running with 

In EditItem
#	after_mount { jQ[dom_node].focus }   doesn't seem to work
    jQ[dom_node].focus
