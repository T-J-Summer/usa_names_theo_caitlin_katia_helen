# This is a small project that shows how the popularity of some names changed in the USA!

You can see the [Jupyter notebook here](https://deepnote.com/workspace/t-j-summer-378b-a69dcfb9-9ce8-41e5-8992-039412d23981/project/Untitled-project-Duplicate-0009537c-10f1-4fdb-9a85-f684514c2288)

## The source of data

The project started with the following SQL queries run on [Google BigQuery](https://console.cloud.google.com/bigquery) 

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

The resulting graph is here:
![Graph](https://github.com/T-J-Summer/usa_names_theo_caitlin_katia_helen/blob/master/caitlin_theo_katia_helen_in_usa.png)
