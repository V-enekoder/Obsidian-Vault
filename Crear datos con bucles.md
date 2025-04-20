A pesar de lo que parece muchas veces, [[SQL]] es un lenguaje de programación en toda regla. Y dependiendo del gestor, puede poseer más o menos características. En este caso, [[PostgreSQL]] ofrece *generate_series*: 

```sql
generate_series(start, stop [, step])
```

Que se encarga de generar una lista de datos, parecido a como haría un bucle en python. Y se puede utilizar en casos como 

```sql
INSERT INTO actividad_persona(actividad_id,persona_id)
SELECT 21, num
FROM generate_series(209,225) AS num;
```

Donde el retorno de generate_series será el retorno de start y stop. E>n este caso en entero, pero puede ser también una fecha