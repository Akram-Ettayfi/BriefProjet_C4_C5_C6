## question 1
```sql
. SELECT Name FROM Pieces;
 ```



## question 2
```sql
. SELECT * FROM Providers;
  ```


## question 3
```sql
.  SELECT Piece, AVG(Price) FROM Provides GROUP BY Piece; 
 ```


## question 4
```sql
. SELECT Name FROM Providers 
  WHERE Code IN 
   (SELECT Provider FROM Provides WHERE Piece = 1); 
  ```



## question 5
```sql
. SELECT Name 
   FROM Pieces 
   WHERE Code IN 
     (SELECT Piece FROM Provides WHERE Provider = 'HAL');
 ```


## question 6
```sql
. SELECT Pieces.Name, Providers.Name, Price 
   FROM Pieces INNER JOIN Provides ON Pieces.Code = Piece 
               INNER JOIN Providers ON Providers.Code = Provider 
   WHERE Price = 
   ( 
     SELECT MAX(Price) FROM Provides 
     WHERE Piece = Pieces.Code 
   );
 ```


## question 7
```sql
. INSERT INTO Provides  VALUES (1, 'TNBC', 7);
  ```


## question 8
```sql
. UPDATE Provides SET Price = Price + 1; 
 ```

## question 9
```sql
. DELETE FROM Provides WHERE Provider = 'RBT' AND Piece = 4;
 ```
__
## question 10 
```sql
. DELETE FROM Provides WHERE Provider = 'RBT'
 ```