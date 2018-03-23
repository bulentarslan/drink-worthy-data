# Drink Worthy Data
Exploring the Iowa Liquor Sales dataset.

# Table of Contents
- [Exploratory data analysis](#exploratory-data-analysis)
    * [Taking a closer look at the data](#taking-a-closer-look-at-the-data)
        + [Who drinks the most?](#who-drinks-the-most)
        + [Who are the top 10 vendors in Iowa?](#who-are-the-top-10-vendors-in-iowa)
        + [What are Jim Beam's top selling liquors?](#what-are-jim-beam-top-selling-liquors)
        + [What is the price-response for Jim Beam 1750ml?](#what-is-the-price-response)
        + [Log-log price-response?](#log-log-price-response)
    * [Taking a closer look at demand (our response)](#taking-a-closer-look-at-demand)
        + [How has demand for Jim Beam 1750ml varied over time?](#how-has-demand-varied-over-time)
        + [How has change in demand varied over time?](#how-has-change-in-demand-varied-over-time)
        + [Comparing demand, % change, and log diff distributions.](#comparing-demand-change-and-log-diff-distributions)
        + [How do demand and change in demand vary month-to-month?](#how-do-demand-and-change-in-demand-vary-month-to-month)
    * [Taking a closer look at price (our predictor)](#taking-a-closer-look-at-price)
        + [How has price for Jim Beam 1750ml varied over time?](#how-has-price-varied-over-time)
        + [How has change in price varied over time?](#how-has-change-in-price-varied-over-time)
        + [Comparing price, % change, and log diff distributions.](#comparing-price-change-and-log-diff-distributions)
        + [How do price and change in price vary month-to-month?](#how-do-price-and-change-in-price-vary-month-to-month)
- [Developing a demand model](#developing-a-demand-model)
    * [Modeling approach](#modeling-approach)
    * [Hyperparameter tuning](#hyperparameter-tuning)
    * [Residual analysis](#residual-analysis)
    * [Error](#error)
- [Inferring seasonality and price elasticity](#inferring-seasonality-and-price-elasticity)
    * [Seasonality coefficients](#seasonality-coefficient)
    * [Price elasticity coefficient](#price-elasticity-coefficient)
- [Optimizing promotions to maximize profit](#optimizing-promotions-to-maximize-profit)
    * [Optimization approach](#optimization-approach)
    * [Profit curves](#profit-curves)

<a name="exploratory-data-analysis"></a>
## Exploratory data analysis

<a name="taking-a-closer-look-at-the-data"></a>
### Taking a closer look at the data

<a name="who-drinks-the-most"></a>
#### Who drinks the most?

<img src="./img/county_consumption_choropleth_map.png">

<a name="who-are-the-top-10-vendors-in-iowa"></a>
#### Who are the top 10 vendors in Iowa?

| ID  | Sales (Millions of $) | Vendor                             | 
|-----|-----------------------|------------------------------------| 
| 260 | 307.54                | Diageo Americas                    | 
| 370 | 103.29                | Pernod Ricard USA/Austin Nichols   | 
| 65  | 100.22                | Jim Beam Brands                    | 
| 434 | 96.61                 | Luxco-St Louis                     | 
| 115 | 85.89                 | "Constellation Wine Company, Inc." |
| 85  | 80.92                 | Brown-Forman Corporation           | 
| 421 | 79.48                 | "Sazerac Co., Inc."                | 
| 35  | 67.17                 | "Bacardi U.S.A., Inc."             | 
| 395 | 47.44                 | Proximo                            | 
| 55  | 46.03                 | Sazerac North America              | 

<a name="what-are-jim-beam-top-selling-liquors"></a>
#### What are Jim Beam's top selling liquors?

| ItemID | Sales (Millions of $) | VendorID | Item                  | Volume (ml) | 
|--------|-----------------------|----------|-----------------------|-------------| 
| 19068  | 5.39                  | 65       | Jim Beam              | 1750        | 
| 19067  | 4.9                   | 65       | Jim Beam              | 1000        | 
| 34578  | 4.33                  | 65       | Pinnacle Vodka        | 1750        | 
| 15248  | 3.97                  | 65       | Windsor Canadian Pet  | 1750        | 
| 19066  | 3.9                   | 65       | Jim Beam              | 750         | 
| 19476  | 3.88                  | 65       | Maker's Mark          | 750         | 
| 19477  | 3.82                  | 65       | Maker's Mark          | 1000        | 
| 24458  | 3.26                  | 65       | Kessler Blend Whiskey | 1750        | 
| 82847  | 3.09                  | 65       | Dekuyper Peachtree    | 1000        | 
| 10628  | 2.63                  | 65       | Canadian Club Whisky  | 1750        | 

<a name="what-is-the-price-response"></a>
#### What is the price-response for Jim Beam 1750ml?

<a name="log-log-price-response"></a>
#### Log-log price-response?

<a name="taking-a-closer-look-at-demand"></a>
### Taking a closer look at demand (our response)

<a name="how-has-demand-varied-over-time"></a>
#### How has demand for Jim Beam 1750ml varied over time?

<a name="how-has-change-in-demand-varied-over-time"></a>
#### How has change in demand varied over time?

<a name="comparing-demand-change-and-log-diff-distributions"></a>
#### Comparing demand, % change, and log diff distributions.

<a name="how-do-demand-and-change-in-demand-vary-month-to-month"></a>
#### How do demand and change in demand vary month-to-month?

<a name="taking-a-closer-look-at-price"></a>
### Taking a closer look at price (our predictor)

<a name="how-has-price-varied-over-time"></a>
#### How has price for Jim Beam 1750ml varied over time?

<a name="how-has-change-in-price-varied-over-time"></a>
#### How has change in price varied over time?

<a name="comparing-price-change-and-log-diff-distributions"></a>
#### Comparing price, % change, and log diff distributions.

<a name="how-do-price-and-change-in-price-vary-month-to-month"></a>
#### How do price and change in price vary month-to-month?

<a name="developing-a-demand-model"></a>
## Developing a demand model

<a name="modeling-approach"></a>
### Modeling approach

<a name="hyperparameter-tuning"></a>
### Hyperparameter tuning

<a name="residual-analysis"></a>
### Residual analysis

<a name="error"></a>
### Error

<a name="inferring-seasonality-and-price-elasticity"></a>
## Inferring seasonality and price elasticity

<a name="seasonality-coefficient"></a>
### Seasonality coefficients

<a name="price-elasticity-coefficient"></a>
### Price elasticity coefficient

<a name="optimizing-promotions-to-maximize-profit"></a>
## Optimizing promotions to maximize profit

<a name="optimization-approach"></a>
### Optimization approach

<a name="profit-curves"></a>
### Profit curves
