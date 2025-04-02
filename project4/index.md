---
title: "Apple's Duration/Convexity Bond Analysis"
nav_order: 4
---
<iframe width="700" height="700" frameborder="0" scrolling="no" src="https://1drv.ms/x/c/bc42f51f77b4ccbd/IQSpj4-85F1rQp9vfK9W9odSAelbSZFfS3pFA9_ftI33NJU?em=2&wdAllowInteractivity=False&wdHideGridlines=True&wdHideHeaders=True&wdDownloadButton=True&wdInConfigurator=True&wdInConfigurator=True"></iframe>

Bond issued by Apple with CUSIP: 037833AT7, maturity in 5/6/2044

Duration is a linear approximation of the bond’s price sensitivity to interest rate changes, calculated by taking the first derivative of the bond's price with respect to yield. However, the relationship between price and yield is not linear; it is a convex shape. The duration linear approximation will always overstate decreases of bond prices when rates increase, and understate increases in bond prices when interest rates fall. The linear approximation only works well for small changes in interest rates, since the gap between the price/yield relationship and duration is small, but for large changes in interest rates, you need to account for convexity (the curvature) to get a better approximation of the bond's price sensitivity. This is done by taking the second derivative of the bond's price with respect to the yield. Convexity is a benefit to bondholders as it means bond prices fall less and rise more than a straight line would suggest. 

The excel file below graphs the price/yield relationship of an Apple security maturing in 5/6/2044. In the graph, duration and convexity are calculated and graphed. Typing any number into the yellow cell or moving the pink slider will show the sensivity changes of rising/falling interest rates and will show the corresponding duration/convexity/price movement on the graph. This gives a better understanding on how bond prices react to interest rate changes, and how duration and convexity together provide a more accurate estimate of price sensitivity—especially for larger rate movements.


