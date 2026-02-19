


### Nivell 1: Unions directes (2 taules)
> [!NOTE]
> L'objectiu és unir dues taules que tenen una relació directa (Clau Primària - Clau Forana).

#### 1. **Pel·lícules i Idiomes:** 
Selecciona el títol de la pel·lícula (`film.title`) i el nom de l'idioma (`language.name`).
```sql
SELECT film.title, language.name
FROM film
JOIN language ON film.language_id = language.language_id;
```

#### 2.  **Ciutats i Països:** 
Selecciona el nom de la ciutat (`city.city`) i el nom del país al qual pertany (`country.country`).
```sql

```

#### 3.  **Adreces i Ciutats:** 
Selecciona l'adreça (`address.address`) i el nom de la ciutat (`city.city`) de la taula `address`.
```sql

```

#### 4.  **Clients i Adreces:** 
Selecciona el nom i cognom del client (`customer`) i la seva adreça (`address`).
```sql

```

#### 5.  **Empleats i Adreces:** 
Selecciona el nom de l'empleat (`staff`) i la seva adreça.
```sql

```

#### 6.  **Pel·lícules en anglès:** 
Mostra els títols de les pel·lícules, però només aquelles on l'idioma sigui 'English'.
```sql

```

#### 7.  **Pagaments i Clients:** 
Mostra la data del pagament (`payment_date`) i l'import (`amount`), juntament amb el nom complet del client que l'ha fet.
```sql

```

#### 8.  **Inventari i Pel·lícules:** 
Mostra l'ID de l'inventari (`inventory_id`) i el títol de la pel·lícula que correspon a aquest ítem.
```sql

```

#### 9.  **Lloguers i Empleats:** 
Mostra l'ID del lloguer (`rental_id`) i el nom de l'empleat (`staff`) que va processar el lloguer.
```sql

```

#### 10. **Clients i Botigues:** 
Mostra el nom del client i l'ID de la botiga (`store_id`) a la qual està assignat, però assegura't de mostrar l'adreça de la botiga (necessitaràs unir `customer` i `store`, i després `store` i `address`).

##### *Versió 1*: Mostra només la relació del client amb la botiga
```sql

```

##### *Versió 2*: Mostra client, botiga i adreça
```sql

```

##### *Versió 3*: Mostra client, botiga, adreça del client i adreça de la botiga
```sql

```

### Nivell 2: Camins de 3 taules o taules intermèdies
> [!NOTE]
> Aquí sovint necessitem una taula "pont" (com film_actor) o saltar de A a B i de B a C.
```sql

```

#### 11. **Pel·lícules i Categories:** 
Mostra el títol de la pel·lícula i el nom de la seva categoria (`category.name`). *Pista: `film` -> `film_category` -> `category`.*
```sql

```

#### 12. **Pel·lícules i Actors:** 
Mostra el títol de la pel·lícula i el nom i cognom dels actors que hi surten. *Pista: `film` -> `film_actor` -> `actor`.*
```sql

```

#### 13. **Clients i Ciutats:** 
Volem saber de quina ciutat és cada client. Mostra el nom del client i la ciutat. *Pista: `customer` -> `address` -> `city`.*
```sql

```

#### 14. **Inventari, Pel·lícula i Botiga:** 
Mostra l'ID de l'inventari, el títol de la pel·lícula i l'ID de la botiga on es troba.
```sql

```

#### 15. **Lloguers detallats (Client):** 
Mostra la data de lloguer, el títol de la pel·lícula llogada i el nom del client. *Pista: `rental` -> `inventory` -> `film` (per al títol) i `rental` -> `customer` (per al client).*
```sql

```

### Nivell 3: Múltiples Joins i Lògica de Negoci

> [!NOTE]
> Combinem 4+ taules o afegim filtres específics (`WHERE`) sobre les taules unides.

#### 16. **Clients i Països:** 
Volem un llistat dels clients indicant el seu país de residència. Mostra: Nom Client, País.
```sql

```

#### 17. **Actors de "ACADEMY DINOSAUR":** 
Mostra només els noms dels actors que han actuat a la pel·lícula titulada "ACADEMY DINOSAUR".
```sql

```

#### 18. **Qui ha llogat què? (Filtre per nom):** 
Mostra els títols de les pel·lícules que ha llogat la clienta 'MARY SMITH'.
```sql

```

#### 19. **Pagaments detallats:** 
Mostra la data del pagament, l'import, el nom del client i el nom de l'empleat que ha cobrat.
```sql

```

#### 20. **Informació completa de la Botiga:** 
Mostra l'ID de la botiga, la ciutat on està i el país.
```sql

```
