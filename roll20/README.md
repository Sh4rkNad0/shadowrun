These macros were designed for use with the following Shadowrun 3rd Edition sheet available on Roll20.

https://github.com/Roll20/roll20-character-sheets/blob/master/Shadowrun3e/shadowrun3e.html

These macros use the template:x files found withing that sheet type, as such they could change as the owner updates his sheet.

Technical detail on macros:
1. These macros utilize the "re-use rolls" technique discovered and described here. If this behavior is adjusted by the Roll20 platform these macros will fail.
    - https://wiki.roll20.net/Reusing_Rolls
    - https://app.roll20.net/forum/post/9091992/reusing-rolls-megathread
2. There is no native support for rounding up or down to 0. Details here on how to do this.
    - https://app.roll20.net/forum/post/874726/rounding-solutions-not-problems
3. A number of the scripts are "hacky" in that roll20 Macro's do not natively support calcuating actual damage levels. So you will see in many places
    I've done something like <Damage Level>(staging value). This is because you cannot do math (easily) on re-used rolls. You have to do it in the actual
    original calculation and then grab the roll $[[x]] later. Someone with more patience than me might be able to figure out the syntax to do calculations
    with a reused roll.
4. Optimal way to determine damage would be to use the summation equation (n^2 + n)/2=d; where n is successes/2 and d is boxes of damage. 
    n being the number of boxes to soak d damage or vice versa. But again I lost patience with trying to do that in a macro. 
