## Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
```
SELECT COUNT(*) FROM film
WHERE length >
(
SELECT AVG(length) FROM film
);
```

2. film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
```
SELECT COUNT(*) FROM film
WHERE rental_rate =
(
SELECT MAX(rental_rate) FROM film
);
```

3. film tablosunda en düşük rental_rate ve en düşük replacement_cost değerlerine sahip filmleri sıralayınız.
```
(
	SELECT title FROM film
	WHERE rental_rate =
	(
		SELECT MIN(rental_rate) FROM film
	)
)
UNION
(
	SELECT title FROM film
	WHERE replacement_cost =
	(
		SELECT MIN(replacement_cost) FROM film
	)
)
```

4. payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
```
SELECT first_name, last_name FROM customer
JOIN
(
  SELECT count(*), customer_id
  FROM payment
  GROUP BY customer_id
  ORDER BY count(*) DESC
) as X ON X.customer_id = customer.customer_id;
  ```
