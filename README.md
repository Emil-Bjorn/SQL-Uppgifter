# SQL-Uppgifter
## 1
1. Detta görs med INSERT INTO()
2. Det är möjligt att man skriver fel uppgifter. Databasen blir stor med onödig data vilket tar upp mer plats på hårddisken och försämrar prestandan. 
3. Primärnyckel används för att identifiera unika rader i en tabell. En sekundär nyckel är en kolumn i en tabell som pekar mot en primärnyckel som finns i en annan tabell. Detta skapar en till många relationer. 
4. Personnummer kan vara en bra val till primärnyckel då varje personnummer är unikt. 
5. Sekundärnyckeln kan vara unikt om man vill ha en en till en relation mellan tabellerna. Men annars behöver inte sekundärnyckeln vara unikt. 
6. Information är data som har fått mening
7. En till en: Person till personnummer. Person till födelseort. En till många: Person till telefonnummer. Person till bilar. Många till många. Länder till språk. Skädespelare till filmer.
<img width="681" height="356" alt="Screenshot 2026-11-17 at 06 35 58" src="https://github.com/user-attachments/assets/e27910bf-b5ee-47f5-8467-4a9d16e456c2" />
<img width="398" height="175" alt="Screenshot 2026-11-17 at 06 35 41" src="https://github.com/user-attachments/assets/84832002-6a75-47e3-a0cd-6f0c526dea43" />
<img width="820" height="106" alt="Screenshot 2026-11-17 at 06 35 20" src="https://github.com/user-attachments/assets/df5d904c-f21a-4bf5-abbd-36b3e9c42af1" />

## 2
<img width="422" height="103" alt="Screenshot 2026-11-17 at 06 51 06" src="https://github.com/user-attachments/assets/a671ccf2-7d8f-4aac-908e-df26f2ed7f63" />

## 3
1. Lastbalansering gör det möjligt att dela en last mellan flera delar vilket gör att man kan bättre utnyttja resurser och höja prestandan.
2. Du kan till exempel dela upp nätverkstrafik
3. Man får bättre prestanda. Minskar chansen att flaskhalsar uppstår. Läger också till redundans i fall en server skulle gå ner. 
4. Med SQL Server replication kan man kopiera databas-objekt från en databas till en annan synkronisera dem. 
5. Mirroring liknar replication men till skillnad från replication så går det inte att läsa/skriva till kopian eftersom det är inte aktiv och används bara som backup. 
6. Liknar mirroring men med mer funktionalitet som tex. flera kopior, och läs funktionalitet för kopian.

## 5
CREATE PROC getMarkOrAstrid
AS
SELECT FirstName, LastName, City
FROM Customer
Where FirstName = ‘Mark’ OR FirstName = ‘Astrid’
ORDER BY FirstName DESC;

EXEC getMarkOrAstrid

## 6
CREATE PROC getCity
@city VARCHAR(40) = ‘Stockholm’
AS
SELECT FirstName, LastName, City
FROM Customer
WHERE City = @city;

EXEC getName ‘Paris’;

CREATE PROC getP
SELECT FirstName, LastName
FROM Customer
WHERE FirstName LIKE ‘P%’;

EXEC getP;

## 7
<img width="396" height="99" alt="Screenshot 2026-11-17 at 08 12 32" src="https://github.com/user-attachments/assets/43db80d2-dd78-4467-92b6-1b1a5c64f6e7" />


## 8
<img width="802" height="632" alt="Untitled Diagram drawio" src="https://github.com/user-attachments/assets/7f957c6a-4f11-493a-846e-589ed8a646f0" />

