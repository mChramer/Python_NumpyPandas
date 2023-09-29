# Python_NumpyPandas
Assignment for school in Python using Numpy and Pandas, handed in 2023.02.10

# Instructions for the assignment:

Inlämningsuppgiften är uppdelad i 3 delar; 
1. Numpy 
2. Pandas 
3. Analys
Varje del har sina egna instruktioner som följer.

Betygsättning
Godkänt: För Godkänt gäller:
Klara av Numpy delen
Klara av Pandas delen

Väl Godkänt: För Väl Godkänt gäller:
Allt under Godkänt
Klara av Analys delen

## Part 1 - Numpy
I den här delen gäller det att konstruera och manipulera numpy arrays. Referenshjälp: https://numpy.org/doc/stable/reference/routines.html
Först behöver ni importera numpy.
In [1]:import numpy as np
1. Konstruera en array med 10 kolumner och 5 rader av float-tal. Inget tal får vara samma.
2. Konstruera en ny array till med 10 kolumner och 7 rader av float-tal. Den skall inte innehålla samma tal som den från förra uppgiften.
3. Gör om de två arrayerna från föregående uppgifter så att de har 5 kolumner, med som så många extra rader som behövs.
4. Ta nu de två arrayerna från de föregående uppgifterna och stapla ihop dem till en array som fortfarande har fem kolumner.
5. Ändra ordningen på kolumnerna så att de kommer i ordningen kolumn5, kolumn3, kolumn4, kolumn1, kolumn2.

## Part 2 - Panda
I den här delen gäller det att ladda in en panda dataset och undersöka denna.
In [1]:import pandas as pd
In [2 ]:assults = pd.read_csv('assults.csv')
Efter att ha läst in datan ta reda på från dataframe nedan saker och skriv ut.
1. Hur många regioner finns med i data? Regionerna finns under ”Region_2013_label”.
2. Lista regionerna i bokstavsordning.
3. Vad var invånarantalet i varje region i mitten på år 2015? Använd Pandas för att visa.
4. Hur många brott begicks i varje region år 2015? Ni hittar brotten i kolumnen ”Victimisations_calendar_year_2015”.
5. Visa de 10 områden med de högsta antalet överfall. Områden är ”Area_unit_2013_label”.
6. Lägg till en kolumn i dataframen som visar % antal överfall i området jämfört med invånarantal i området. Varje rad är ett område.
7. Skapa en ny dataframe som innehåller antalet områden (Area_unit_2013_label) som finns av de olika typerna av urban area (Urban_area_2013_label).
8. Ta reda på hur många områden (varje rad är ett område) hade population men inga överfall. Jämfört totala populationen i dessa med totala populationen i deras region (Region_2013_label).
9. Räkna per kolumn hur många rader det är som inte innehåller någon data.
10. Skapa en ny dataframe med 10 rader. Den innehåller de 10 rader med lägsta antalet överfall per invånare (Rate_per_10000_population), men mer än 5000 invånare.
11. Skapa en ny dataframe ”regions” som innehåller sammansatt data per region(Region_2013_label). Lägg till en ny kolumn som innehåller ”Rate_per_10000_population”fast för hela regionen.
12. Lägg till en ny kolumn i dataframen med regionerna som visar i % hur många av alla överfall som sker i den regionen.

## Part 3 – VG: Analys
I den här delen gäller det att ladda en valfri panda dataset och undersöka denna. Dokumentation skrivs i Markdown celler i din Inlämnings.ipynb

Din inlämning kommer värderas på: 

● Minst 500 rader, 5 Kolumner i ditt valda dataset

● Fråga och besvara minst 4 frågor om ditt dataset.

● Minst 4 grapher (kanske representerande ovan frågor) med annoteringar så att man kan förstå dem. 

● Dokumentation i Markdown celler.

● Ingen plagiat.

Dataset repositories: 
UCI repository - https://archive.ics.uci.edu/ml/index.php
Public datasets - https://github.com/awesomedata/awesome-public-datasets
Google dataset search - https://datasetsearch.research.google.com/
Kaggle datasets - https://www.kaggle.com/datasets

Step-by-step guide

Step 1: Välj dataset
Hitta ett intressant dataset. Det valda datasettet måste vara i CSV format, ha minst 500 rader och 5 kolumner. Ladda ner datasetet med pandas read_csv funktion och en url (se nedan). Alternativt i inlämningen skicka med datasettet.
In [1]: import pandas as pd
url = 'https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv'
data = pd.read_csv(url)

Step 2: Data preparation och Cleaning
Ladda in dataset in i en dataframe med pandas. 
Behandla missade data, icke-korrekt data och fel data.
Gör andra steg som behövs (gör om sträng datum till riktiga datum, skapa fler kolumner, slå ihop datasets osv).
Summera hur datasetet ser ut i nuvarande läge i dina markdowns. Storlek, kolumner, kategori typer (qualitative vs. quantitative), kvalitet på data, fång osv.

Step 3: Undersökande analys och visualisering
Undersök data genom analysera (mean, sum, range osv) intressant statistik i numeriska kolumnerna.
Undersök distributions av numeriska kolumner.
Undersök relationen mellan kolumner.
Notera intressanta upptäckter i din markdown.

Step 4: Fråga och svara på 4 intressanta frågor om datan
Fråga minst 4 intressanta frågor om ditt utvalda dataset. Vad kan du göra för analyser på den valda datan?. Svara på frågorna med antingen resultat från Numpy/Pandas eller skapa plottar med Matplotlib. Skapa nya kolumner, slå ihop datasets och skapa grupper när det behövs.
Dokumentera din användande av Pandas/Numpy/Matplotlib funktioner och vad de gör i din markdown.

Step 5: Summera dina slutsatser & Skriv ett avslut.
Skriv en summering vad du lärt dig av din analys. Inkludera intressanta insikter och grafer från föregående sektioner. Ge dina tankar på vad man kan göra i framtiden inom samma område. Länkar till Resources du funnit användbara under uppgiften.
