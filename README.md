# Домашнее задание «SQL. Часть 1»  

## Задание 1  
Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.  

SELECT DISTINCT  district  
FROM address  
WHERE district like 'K%a' and district not like '% %';  

![sql1](https://github.com/user-attachments/assets/98925719-475a-47d8-890b-40a5084d0e60)

## Задание 2  
Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.  

SELECT* from payment  
WHERE payment_date BETWEEN '2005-06-15 00:00:00' AND '2005-06-18 23:59:59'
AND amount > 10;  

![sql21](https://github.com/user-attachments/assets/0371e075-251a-4f21-90de-3b9bf2eb413a)



## Задание 3  
Получите последние пять аренд фильмов.  

SELECT *  
FROM sakila.rental  
ORDER BY rental_id DESC  
LIMIT 5;  

![sql3](https://github.com/user-attachments/assets/00e1d50e-c8a0-4714-ae84-b06039e0e148)

## Задание 4  
Одним запросом получите активных покупателей, имена которых Kelly или Willie.  
Сформируйте вывод в результат таким образом:  
все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр,  
замените буквы 'll' в именах на 'pp'.  

SELECT lower(replace(first_name, 'LL', 'pp')), lower(last_name)  
FROM customer  
WHERE first_name like 'Kelly' or 'Willie';

![sql4](https://github.com/user-attachments/assets/b837005a-926f-4ad0-9a8d-885e42ded73c)
