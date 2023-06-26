# README.MD
## Question 1
-- Who use the website most frequently on 2014-10-01?

```sql
SELECT id_user,
count(id_user) as Times_used
FROM datasets.airbnb_searches
Where ds = '2014-10-01'
group by id_user
order by count(*) DESC
```
![README.md](Visualization/ICA4-1.png)
## Question 2
--How many nights are most people staying on 2014-10-01?

```sql
SELECT
n_nights,
count(n_nights)
FROM datasets.airbnb_searches
Where ds = ‘2014-10-01’
group by n_nights
order by count(*) DESC
```
![README.md](Visualization/ICA4-2.png)


## Question 3
--Where are most customer from?

```sql
SELECT
origin_country,
count(origin_country)
FROM datasets.airbnb_searches
group by origin_country
order by count(*) DESC
```
![README.md](Visualization/ICA4-3.png)

## Question 4
--What’s the lowest price people accepted?

```sql
SELECT
filter_price_min,
count(filter_price_min)
FROM datasets.airbnb_searches
group by filter_price_min
order by count(filter_price_min) DESC
```
![README.md](Visualization/ICA4-4.png)

## Question 5
--What is the most popular room types?

```sqp
SELECT
filter_room_types,
count(filter_room_types)
FROM datasets.airbnb_searches
group by filter_room_types
order by count(*) DESC
```
![README.md](Visualization/ICA4-5.png)



