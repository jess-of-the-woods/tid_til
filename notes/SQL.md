[databases](databases.md)

## SQL - Structured Query Language
**[Knex](javascript/knex.md)**

Not case-sensitive. Statement always end in `;`

- CREATE
- READ
- UPDATE
- DELETE
- INSERT

c.f. [Express.js](javascript/express.md)

e.g.
```sql
SELECT * FROM celebs;
```

```sql
CREATE TABLE table_name (
    column_1 data_type,
    column_2 data_type,
    column_3 data_type
  );
```
```sql
INSERT INTO celebs (id, name, age) VALUES (4, 'Taylor Swift', 26);
SELECT name FROM celebs;
```
```sql
UPDATE celebs
SET age = 22
WHERE id = 1;
```
### SQL Joins & relationships
relationships between data, modelling data

##### People table
id, email, password (id is primary key)

##### Shoes table
size, color, owner_id (foreign id)

one to many relationship. one person, many shoes

`LEFT INNER JOIN`: most commonly used join

```sql
SELECT * FROM shoes INNER JOIN people ON people.id = shoes.owner_id
```

#### Many to many relationship
- Shoe-sharing household
- Many people wear the shoes, the shoes are worn by many
- wear event table in middle.. ( join tables )

twitter project.. one person can follow many people, a person can be followed by many people.


```sql
SELECT * FROM MassiveTable
LIMIT 10 ( return 10 items )
OFFSET 20 ( start at 20th )
```

---

### Links
- [SQL Tutorial](http://www.tutorialspoint.com/sql/) - Tutorialspoint

See also noSQL
