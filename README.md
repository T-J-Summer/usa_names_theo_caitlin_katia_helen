# This is a small project that shows how the popularity of some names changed in the USA!

The project started with the following SQL queries
```
SELECT
  year,
  SUM(number) AS number_of_theos
FROM
  `bigquery-public-data.usa_names.usa_1910_current`
WHERE
  name = "Theo"
GROUP BY
  year
ORDER BY
  year DESC;
```
  
```
SELECT
  year,
  SUM(number) AS number_of_Helens
FROM
  `bigquery-public-data.usa_names.usa_1910_current`
WHERE
  name = "Helen"
GROUP BY
  year
ORDER BY
  year DESC;
```

The resultin graph is here:
![Graph](https://github.com/T-J-Summer/usa_names_theo_caitlin_katia_helen/blob/master/caitlin_theo_katia_helen_in_usa.png)
