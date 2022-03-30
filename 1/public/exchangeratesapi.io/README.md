# exchangeratesapi.io
# Exchange rates

##This folder contains rql code that can be used if you need currency rate operations

Based on https://exchangeratesapi.io/
which provides up to 1.000 free calls per month

You need to register to get your own API key

Endpoints :
## convert
convert(`amount`:double, `src`:string, `dest`:string)

amount: value to convert<p>
src: source currency<p>
dest: destination currency<p>

Available currencies are: "USD", "EUR", "GBP", "CAD", "CNY", "AUD"

Example: https://api.raw-labs.com/demos/1/public/exchangeratesapi.io/convert?amount=100&src=EUR&dest=USD

