# WSB Scraping

Credits: https://www.youtube.com/watch?v=CJAdCLZaISw&t=1710s

## Personal project to scrape data from r/wallstreetbets 



Created using PostgresSQL and Python

APIs used include Alpaca API (for ticker symbols) and Reddit API 




1. Run search_wsb.py to insert tickers mentioned in reddit submissiosn into the database 


2. To see the most mentioned stock tickers, run the following in postgresSQL: 
```
select count(*) as num_mentions, stock_id, symbol from mention join stock on stock.id == mention.stock_id 
group by stock_id, symbol order by num_mentions DESC
```
