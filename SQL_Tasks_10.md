## Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
```
SELECT country.country, city.city FROM country
LEFT JOIN city ON country.country_id = city.country_id;
```

2. customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
```
SELECT customer.first_name, customer.last_name, payment.payment_id FROM payment
RIGHT JOIN customer ON payment.customer_id = customer.customer_id;
```

3. customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.
```
SELECT rental.rental_id, customer.first_name, customer.last_name FROM customer
FULL JOIN rental ON customer.customer_id = rental.customer_id;
```
