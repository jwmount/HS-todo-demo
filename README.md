# README

Todo-demo Tutorial 

Scratch Pad


Issue:  somewhere around Chapter 9 started to render a blank white window (i.e. nothing).
Misc.  Seems to be related to using jQ wrapper, but this may be co-incidental.  Logs are clean until a SysErr 500 appears. 

In edit_item.rb the following line gets added and then nothing renders:

	```after_mount { jQ[dom_node].focus }   once added, crashes```
    
WHAT HAPPENED:  I did not see the .import 'hyperstack/componentjquery statement so I added it.  Doing so I should have cleared the rails cache before proceeding.  This was not a problem until a reference to jQ occured in /components/edit_item.rb (Chapter 9).  
    
SOLUTION:  Verify the .import statement for jquery is in effect in edit_item.rb.  Make sure the .import statement to include jquery is present and in effect (not commented out--a commented version was there, in line 21, but I missed it). Then clear the rails cache, this way:
    
    Stop the server
    ```rm -rf tmp/cache```
    Start the server 
    ``` bundle exec foreman start```
    
    
    


    
    
