# </> Tasca S2.04. MongoDB queries

## 📝 Introducció

Les dades no estructurades comencen a tenir valor quan les podem consultar de manera flexible i eficient. Amb **MongoDB**, entres al món de les bases de dades **NoSQL**, on el model relacional dóna pas a una estructura basada en **documents JSON** que permet adaptar-se fàcilment a dades canviants i escenaris àgils de desenvolupament.

Aquesta tasca et convida a practicar com fer **consultes precises** i **expressives** en MongoDB utilitzant la seva sintaxi basada en JavaScript.  
Treballaràs amb una col·lecció de documents de **restaurants** de Nova York, on aplicaràs filtres, ordenacions, projeccions i operadors avançats per extreure informació rellevant.

No només aprendràs a fer les consultes correctes, sinó també a **interpretar les estructures no normalitzades**, a **entendre els avantatges del model documental** i a **comparar-ho amb l’enfoc relacional** quan sigui pertinent.

---

## 💡 Bases de dades NoSQL: per què i quan?

MongoDB és un exemple típic de base de dades NoSQL. A diferència de les bases relacionals, on tot es distribueix en taules estrictament definides, MongoDB emmagatzema la informació en documents (tipus JSON o BSON), més propers a com es representa la informació en aplicacions modernes.

### **Punts forts de MongoDB:**
- 🔄 **Flexibilitat en l’estructura:** cada document pot tenir camps diferents, útil en entorns on l’esquema evoluciona sovint.
- 🚀 **Rendiment en consultes amb grans volums de dades no estructurades.**
- 🌐 **Escalabilitat horitzontal:** fàcilment escalable amb particionament (*sharding*).
- 📦 **Integració natural amb aplicacions JavaScript o Node.js**, ja que utilitza JSON.

### **Quan és recomanable usar NoSQL?**
- Quan els requisits de l’esquema canvien amb freqüència.
- Quan cal emmagatzemar grans volums de dades semi-estructurades o sense estructura.
- Quan es prioritza la velocitat i la flexibilitat davant la integritat referencial estricta.

---

## 🛠️ Com fer la tasca

1. Importa la col·lecció JSON de restaurants a la teva base de dades MongoDB local (col·lecció `restaurants` dins la base de dades `nyc`).

   🔧 **Opcions per fer-ho:**
   - Pots fer-ho utilitzant una instància local de MongoDB.
   - O bé pots utilitzar **Docker**, amb la configuració ja preparada al [repositori](https://github.com/IT-Academy-Back/S2.4-MongoDB-Evaluator).

2. Per cada enunciat numerat, escriu la consulta MongoDB corresponent (`db.restaurants.find(...)`, etc.).
3. Executa les consultes i comprova que retornen el resultat esperat.
4. Revisa si es poden optimitzar (per exemple, amb **índexs** o usant correctament projeccions i operadors).

📌 En aquest [repositori](https://github.com/IT-Academy-Back/S2.4-MongoDB-Evaluator) també trobaràs les instruccions per fer servir el corrector automàtic. Un cop fetes, envia l’enllaç del teu repositori mitjançant Moodle al teu mentor/a.  
     👉 [Instruccions d'ús](https://github.com/IT-Academy-Back/S2.4-MongoDB-Evaluator/blob/main/query/README.md)


## Enunciat 
Per aquesta tasca tenim una col·lecció d'Objectes Restaurant a la ciutat de Nova York, i necessitem algunes consultes... pots ajudar-nos?

### ❕ Important
> **Totes les consultes han d’excloure l’_id.**

1. Mostrar tots els documents en la col·lecció Restaurants.  
2. Mostrar el restaurant_id i name per tots els documents en la col·lecció Restaurants.  
3. Mostrar el restaurant_id, name, borough i cuisine.  
4. Mostrar restaurant_id, name, borough i zip code.  
5. Mostrar tots els restaurants que estan en el Bronx.  
6. Mostrar els primers 5 restaurants que estan en el Bronx.  
7. Mostrar el pròxims 5 restaurants després de saltar els primers 5 del Bronx.  
8. Trobar els restaurants amb un score de més de 90.  
9. Trobar els restaurants amb un score de més de 80 però menys que 100.  
10. Trobar els restaurants amb longitud menor que -95.754168.  
11. Trobar restaurants que no preparen 'American', amb qualificació > 70 i longitud < -65.754168.  
12. El mateix que l'anterior però sense usar operador $and.  
13. Trobar restaurants que no són 'American', grau 'A', i no són de Brooklyn. Ordenats per cuisine descendent.  
14. Trobar restaurant_id, name, borough i cuisine on el nom comença amb 'Wil'.  
15. Trobar restaurant_id, name, borough i cuisine on el nom acaba en 'ces'.  
16. Trobar restaurant_id, name, borough i cuisine on el nom conté 'Reg'.  
17. Trobar restaurants del Bronx que preparen cuina americana o xinesa.  
18. Trobar restaurant_id, name, borough i cuisine per a Staten Island, Queens, Bronx o Brooklyn.  
19. Trobar restaurant_id, name, borough i cuisine per a restaurants que NO són d'aquests barris.  
20. Trobar restaurant_id, name, borough i cuisine amb marcador no superior a 10.  
21. Trobar restaurants que preparen peix, no 'American' ni 'Chinees', o nom comença amb 'Wil'.  
22. Trobar restaurant_id, name, i grades per grau "A", score 11, i data "2014-08-11T00:00:00Z".  
23. Trobar restaurant_id, name i grades on el 2n element té grau "A", score 9 i data "2014-08-11T00:00:00Z".  
24. Trobar el restaurant_id, name, street, zipcode i coordenades dels restaurants a menys de 5 km de [-74, 40.7].  
25. Ordenar els noms dels restaurants en ordre ascendent, mostrant totes les columnes.  
26. Ordenar els noms dels restaurants en ordre descendent, mostrant totes les columnes.  
27. Ordenar cuisine ascendent i borough descendent.  
28. Mostrar direccions que no contenen el carrer.  
29. Seleccionar documents on el valor de coordinate és de tipus Double. Mostrar el name, restaurant_id i coordinades.  
30. Mostrar restaurant_id, name i grade per restaurants amb marcador divisible per 7 (resta 0).  
31. Trobar name, borough, longitud, latitud i cuisine per noms que contenen 'mon'.  
32. Mostrar restaurant_id, name i grade i score de més de 80 però menys que 100.  

## ⭐Nivell 1
> Certificaràs el teu nivell 1 si construeixes 17 consultes correctes.

## ⭐⭐Nivell 2
> Tindràs nivell 2 si construeixes entre 17 i 25 consultes correctes.

## ⭐⭐⭐Nivell 3
> Si aconsegueixes construir correctament més de 25 consultes correctes!!!