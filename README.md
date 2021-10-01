## Introduction
This application test the [Nomics Cryptocurrency & Bitcoin API](https://nomics.com/docs) end points. Currently it list currencies, list currencies with dynamic params and fetching a currency with specific fiat.
## Project Setup
1. Download the code using git or UI webapp
2. Goto the project directory
```
 cd project_name
 # run following cmd
 bundle install
 yarn install --check-files
 
```
3. Start local server
```
 rails s
```
4. Visit link (perform testing)
```
http://localhost:3000/
```
### End Points used
1. List Currencies
```
# End point tested with different ids & attribute values
https://api.nomics.com/v1/currencies/ticker?key=#{API_KEY}&ids=BTC,ETH,XRP&attributes=id,name,log
```
2. Currency with specific fiat

```
# End point tested with different id values [BTC, ETH, XRP] & conversion value(fiat) [USD, EUR, ZAR]
# End point test with hard coded default time span (&start=2018-04-14T00%3A00%3A00Z&end=2018-05-14T00%3A00%3A00Z)

https://api.nomics.com/v1/currencies/sparkline?key=#{API_KEY}&ids=BTC&start=2018-04-14T00%3A00%3A00Z&end=2018-05-14T00%3A00%3A00Z&convert=EUR
```

