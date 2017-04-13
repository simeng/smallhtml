# smallhtml

# Trix

 * Use byte order mark to set utf8 instead of meta charset (16 bytes)
 * JS code in onload= (10 bytes)
 * Skip all use of " in html (2 bytes)
 * Fetch element by global js-variable set by id= (27 bytes)
 * Set m=Math (<num_uses - 1>*3-2 bytes)
 * Set font to "4 a" instead of "4px arial", but since we skip " in onload we can't have space so replace with \r (5 bytes)
 * Set and update varibles right in the "for (;;)" to save having to use {} and some ";" (~3 bytes)
 * Count down to 0 in condition part so it autostops and we save condition check (3 bytes)
 * Make sure ending newline is killed (1 byte)
 * Reuse any numeral value as many places as possible, possibly making subtle changes to the effect
 * = has higher priority than +=, allow you to assign static base values and add in the same step
 * use <condition>&&<code> instead of if ()
 * setInterval takes a string
 * Use approximate values to get away with fewer decimals
 * Try to reuse any drawing function as a clearing function as well
 * Use canvas and onclick to execute all code to avoid needing <body>-tag

