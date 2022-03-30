## Value at Risk 

An example showing how RAW can be used as Calculation-as-a-Service for resource intensive data products

The associated blog post can be found here:
http://raw-labs.com/blog/resource-intensive-data-products-calculation-as-a-service-value-at-risk/


THIS MAY TAKE A FEW SECONDS TO RUN

https://api.raw-labs.com/examples/1/public/value-at-risk/index-var. (No param defaults to ^DJI)

Returns the VaR of a portfolio of 1 million stocks for a given index (I have just 3 indexes), 
over a 5 year horizon with 99% confidence. The stocks are then grouped up into Industry sectors 
so you can see relative risks of investing in sectors



https://api.raw-labs.com/examples/1/public/value-at-risk/index-var?index=^DJI - Dow Jones 30 stocks

https://api.raw-labs.com/examples/1/public/value-at-risk/index-var?index=^GSPC - S&P 500 stocks

https://api.raw-labs.com/examples/1/public/value-at-risk/index-var?index=^IXIC - Nasdaq 100 stocks

(Currently only these 3 are supported because I don’t have more index weights)

 Multiple parameters are supported... index, confidence and horizon 
e.g. https://api.raw-labs.com/examples/1/public/value-at-risk/index-var?index=^IXIC&confidence=95 
 
