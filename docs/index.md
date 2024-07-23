# ME204 (2024) | Jon's project

## About

- I scraped data from three major supermarkets in the UK to compare the prices of different products. I created a data pipeline to automate the process of scraping and cleaning the data. In the end, all my analysis is saved in Jupyter Notebooks under this [GitHub repository](https://github.com/LSE-ME204/demo-repository).

## Data

The data I collected comes from three sources:

1. [Tesco](https://www.tesco.com/)
2. [Sainsbury's](https://www.sainsburys.co.uk/)
3. [Asda](https://groceries.asda.com/)

I wrote individual scrapers for each website and saved the data in CSV files. The data is stored in the `data/raw` folder of the repository.

In the end I created a SQLite database with the following tables:

- `product`: with the following columns:
    - `id`: unique identifier
    - `name`: name of the product
    - `price`: price of the product
    - `store`: store where the product was found
    - `data`: date when the data was scraped
- `nutrition`: with the following columns:
    - `id`: unique identifier
    - `product_id`: foreign key to the `product` table
    - `calories`: number of calories per 100g
    - `fat`: amount of fat per 100g
    - `carbs`: amount of carbohydrates per 100g
    - `protein`: amount of protein per 100g

## Analysis

This is what I discovered:

- Tesco is the cheapest supermarket overall and I can prove:

| Store    | Average price (£) |
|----------|-------------------|
| Tesco    | 1.20              |
| Sainsbury| 1.30              |
| Asda     | 1.40              |
