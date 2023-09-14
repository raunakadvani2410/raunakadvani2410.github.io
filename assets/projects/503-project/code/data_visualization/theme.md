**Project Theme**

For an effective project, we want to make sure our theme is consistent throughout our visualizations to ensure cohesion. If visualizations were to use different yet similar versions of the same color, it may create confusion for the user as to what this difference may signify even if it is actually meaningless. Consequently, we have allocated several colors by hex code to ensure that color difference only exist if by intent.

*Background*

Before picking the colors of our dataset, we first want to use a general white theme, ('plotly_white', seaborn's "white", or ggplot's "theme_light" for example). This will allow our other color selections to be most visible whereas a gray background could make a green or red difficult to see.

*Money Green*

These colors were selected to fit with our dataset involving banks. There are a couple of common intuitions for colors in banking that we wanted to remain consistent with. First, when people think money, they think green, particularly dark green. For cumulative money totals, we will therefore use a "money green" as represented by the hex code #118C4F. Other color codes for this green can be found at https://www.color-name.com/money-green.color.

*Gold*

The other color that people associate with money is gold. A truly metallic gold would look unprofessional on a data visualization. Instead, the gold has to be more yellow and matte to match with the other colors that might be used. For any golds, we will use the hex code: #FFB90D. This is also R's "darkgoldenrod1". Other color codes can be found at https://www.color-name.com/hex/ffb90d.

*Electric Green*

Finally, there may be analyses where we look to compare positives and negatives. For these, people again would commonly think of green for positive, but we want to distinguish it from our money green. This green will be brighter in the same way you see green for positive stocks as a brighter green. For these greens, we will use an "electric green" or what in R is simply "green", with hex code: #02ff00. Other color codes for electric green can be found at https://www.color-name.com/hex/02ff00.

*Red*

For the red to contrast this green, we will use a similarly bright red to show that these colors are associated with one another. Fortunately, R's "red" works quite well for this as represented by the hex code: #FF0000. Other color codes for red can be found at https://www.color-name.com/hex/ff0000.

*Other*

More colors may be added as they come up throughout this project; these colors only serve as a basis for our first visualizations. Similarly, we have yet to pick a color to be the primary color for the elements of our project that are not in visualizations such as headers or a page sidebar. Quarto's default blue would likely be the leading candidate. 

**Bank Colors**

*Citigroup*

Citigroup uses a darker blue represented by the hex code of: #003A72. More information can be found here:https://www.schemecolor.com/citigroup-logo-colors.php 

*JP Morgan Chase*

JP Morgan's primary blue is a very similar dark blue to Citigroup and Bank of America, therefore we will use Chase Bank's light blue to make it clear. The hex code for this is #117ACA and more information can be found here: https://www.schemecolor.com/chase-bank-logo.php 

*Bank of America*

Bank of America also has the common dark blue that makes it difficult to identify. Therefore we will use its secondary color, a candy red represented by hex code: #E61030. More information can be found here: https://www.schemecolor.com/bank-of-america-logo-colors.php 

*Wells Fargo*

Wells Fargo has perhaps the most distinct colors of the four major banks, using red and yellow as its primary colors. We will use its yellow since the red is too similar to other banks. The yellow we will use is hex code: #ffcc02 as found here: https://www.color-hex.com/color-palette/109504 