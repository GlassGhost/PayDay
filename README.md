#The Never Ending PayDay
______________________________________________________________________

![](http://i.imgur.com/5wvH46g.jpg)

If you ever feel like the picture above or know someone who might, the problem is to **"know precisely how much money to use at a daily rate, while still leaving money for ALL the bills at the end of the month."** [The Spreadsheet](https://goo.gl/k6HAv4) in the picture below, lets one enter in their Income and Bills Each for each month and calculates everything so that you can, **"know precisely how much money to use at a daily rate, while still leaving money for ALL the bills at the end of the month."**:

[![The Spreadsheet](Monthly%20to%20Daily%20Billing%20scheme.svg)](https://goo.gl/k6HAv4)

Click the [The Spreadsheet](https://goo.gl/k6HAv4), then click file->"make a copy" will save a copy to your google drive profile, on your copy you enter in your list of monthly bills; when you're done you get a **MAGIC** number your "daily spending rate". To use the **MAGIC**, just make certain your "billing account" statement looks like your "billing spreadsheet" mixed with scheduled daily transfers of the magic number into your spending account(talk to your bank about how to do this), And you're done.

####Then hopefully ALL OF THE MONTH Will Be Smooth Sailing
![Alt text](smooth.jpg)

### **CAUTION**
[The Spreadsheet](https://goo.gl/k6HAv4) only calculates for the bills you enter, because of this I would also suggest you add a "miscellaneous bill" entry in the event of unforseen expenses.  
At the end of the month a final withdraw of whatever is unspent of the "miscellaneous bill" into your savings.

####Also 
To speed up writing your new sheet when starting a new month, you can to duplicate your previous month bills by right clicking the "template sheet" &  selecting "duplicate sheet" then right click and rename the duplicate sheet to the name of the new month, and to change the date in the `F4` cell.

______________________________________________________________________
##How it works
Through the Magic of Spreadsheets  

The total bills is calculated by adding them all up with: `=sum(B5:B)`

The spending money is calculated by subtracting total bills from the income: `=B2-B3`

The ENTIRE Daily column is controlled by the content of the 1st daily cell, it simply iterates over the entire column dividing the cell to its right by the number of days in the month:  
`=IFERROR(ARRAYFORMULA(B2:B/day(eomonth(F4,0))),"")`
