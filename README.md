# Proiect_final_python
Referințe: 

Tkinter: https://docs.python.org/3/library/tkinter.html 

Geopy: https://geopy.readthedocs.io/en/stable/ 

TimezoneFinder: https://pypi.org/project/timezonefinder/ 

OpenWeatherMap API: https://openweathermap.org/api 

 

Pentru a rula codul este nevoie de librariile: tk, geopy, timezonefinder, requests. Care se instaleaza prin comanda in cmd: pip install tk geopy timezonefinder requests 

Codul se ruleaza folosind IDLE, open file si run. 

 

Descriere funcțională + Backend: 

Aplicația are o interfață grafică simplă cu un câmp de căutare pentru orașe. 

Utilizatorul introduce numele unui oraș și apasă butonul de căutare. 

Orașul este geolocat folosind Geopy pentru a obține coordonatele și TimezoneFinder pentru a afla fusul orar. 

Ora actuală pentru ora locală a orașului este afișată în partea de sus a ferestrei. 

Se face o cerere către API-ul OpenWeatherMap pentru a obține informații despre vreme pentru orașul respectiv. 

Informațiile despre vreme (temperatura, condiția, vântul, umiditatea, presiunea) sunt afișate pe ecran. 

Funcția getWeather:  

Această funcție este activată atunci când butonul de căutare este apăsat. 

Obține numele orașului introdus în widget-ul de intrare (textfield) și utilizează Geopy pentru a obține coordonatele geografice (latitudine și longitudine) ale acelui oraș. 

Apoi utilizează biblioteca TimezoneFinder pentru a găsi fusul orar al coordonatelor date. 

Cu informațiile despre fusul orar, obține timpul curent în acea locație și actualizează eticheta cu ceas. 

Construiește apoi URL-ul de cerere API pentru OpenWeatherMap folosind numele orașului, face cererea și interpretează răspunsul JSON pentru a extrage informațiile meteorologice. 

Informațiile meteorologice extrase (temperatură, condiție, descriere, presiune, umiditate și viteză a vântului) sunt apoi afișate în etichetele corespunzătoare (t, c, d, p, w, h). 


Widget-uri (Etichete, Intrare, Buton, etc.): 


textfield: Widget de intrare în care utilizatorul introduce numele orașului. 

myimage_icon: Buton cu un icon de căutare. Când este apăsat, declanșează funcția getWeather. 

logo: Etichetă care afișează o imagine de logo. 

name, clock: Etichete care afișează vremea și ora curentă. 

label1, label2, label3, label4: Etichete pentru afișarea vitezei vântului, umidității, descrierii și presiunii. 



 

Note: 

Imaginile trebuie să fie disponibile în directorul curent pentru a asigura afișarea corectă a interfeței grafice. 

Cheia API de la OpenWeatherMap este necesară pentru a obține datele meteorologice și trebuie înlocuită în cod. 

 
