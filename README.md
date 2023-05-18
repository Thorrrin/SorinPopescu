# SorinPopescu
**Aplicatie de management a campaniilor de strangere de fonduri**     
#Student: Popescu Sorin; Grupa 1120 An1 SIMPRE

#Link deployment in Vercel:        
      - MainPage: https://sorin-popescu-mg3sktsis-thorrrin.vercel.app/    
      - Insertpage: https://sorin-popescu-mg3sktsis-thorrrin.vercel.app/insert     
      - ChatPage: https://sorin-popescu-mg3sktsis-thorrrin.vercel.app/chat     
#GitHub repository: https://github.com/Thorrrin/SorinPopescu    
#Link prezentare aplicatie: https://youtu.be/6o0bwE2fLC4       
#Link AWS: http://3.74.8.85/        
#Link AWS: http://3.74.8.85/insert       
#Link AWS: http://3.74.8.85/chat

**Introducere:**      
Aplicația noastră de campanii de strângere de fonduri vă permite să vizualizați campanii de strângere de fonduri și să faceți donații la acestea. În plus, puteți să vă înregistrați ca utilizator și să creați campanii proprii de strângere #de fonduri.

**Descriere problema:**    
Când accesați aplicația, veți fi întâmpinat de pagina principală, care conține o listă cu toate campaniile disponibile. Fiecare campanie este reprezentată de o casetă care conține informații despre titlu, descriere și suma donată până în prezent. În partea de jos a fiecărei campanii sunt două butoane - un buton de ștergere a unei campanii și un buton pentru adăugarea unei donații de 100 RON.    
Aplicația de fundraising este construită folosind următoarele **tehnologii și servicii**:    
•	Frontend: aplicația folosește Next.js - un framework React pentru construirea paginilor web dinamice, care facilitează server-side rendering și generarea de pagini statice.    
•	Backend: aplicația folosește Express.js - un framework Node.js pentru construirea serverelor web. Acesta furnizează #API-ul pentru comunicarea dintre frontend și baza de date MongoDB.     
•	Baza de date: aplicația utilizează MongoDB - o bază de date NoSQL care stochează datele campaniilor de fundraising.     
•	Deployment: aplicația este gazduită pe platforma VERCEL - o platformă cloud care oferă servicii de hosting, scalabilitate și administrare pentru aplicații web.


**Descriere API**:     
API-ul pentru aplicația cloud de campanii de strângere de fonduri include următoarele endpoint-uri:   

#GET /api/records - acest endpoint va returna toate campaniile de strângere de fonduri existente în baza de date. #Rezultatele pot fi returnate sub forma #unui array de obiecte JSON, fiecare obiect reprezentând o campanie de strângere #de fonduri.     

#GET /api/records/:id - acest endpoint va returna o singură campanie de strângere de fonduri, specificată prin ID-ul său #unic. Rezultatul poate fi #returnat sub forma unui obiect JSON, reprezentând campania specificată.      

#POST /api/records - acest endpoint va permite crearea unei noi campanii de strângere de fonduri. În cadrul cererii HTTP #POST, se va trimite un obiect #JSON cu detaliile campaniei de strângere de fonduri. După ce obiectul este validat și #adăugat cu succes în baza de date, se va returna un răspuns cu #status code 201 Created, alături de un obiect JSON #reprezentând campania nou creată.      

#PUT /api/records/:id - acest endpoint va permite actualizarea unei campanii de strângere de fonduri existente în baza #de date. În cadrul cererii HTTP #PUT, se va trimite un obiect JSON cu detaliile actualizate ale campaniei, împreună cu #ID-ul unic al campaniei care trebuie actualizată. După ce obiectul #este validat și actualizat cu succes în baza de #date, se va returna un răspuns cu status code 200 OK, alături de un obiect JSON reprezentând campania #actualizată.      

#DELETE /api/records/:id - acest endpoint va permite ștergerea unei campanii de strângere de fonduri existente în baza #de date. În cadrul cererii HTTP #DELETE, se va specifica ID-ul unic al campaniei care trebuie ștersă. După ce campania #este ștearsă cu succes din baza de date, se va returna un răspuns #cu status code 204 No Content.      

#PATCH /api/records/:id - o metoda PATCH pentru a actualiza suma donata pentru o anumita campanie     

#Fișierele MainPage.jsx și InsertPage.jsx sunt responsabile pentru interfața utilizatorului și interacțiunea cu utilizatorul.    
#1.	MainPage.jsx - Acest fișier este responsabil pentru afișarea campaniilor existente de strângere de fonduri. Pentru fiecare campanie, se afișează titlul, descrierea și suma donată până în acel moment. Utilizatorul poate să șteargă o campanie sau să doneze bani pentru o campanie.     
#2.	InsertPage.jsx - Acest fișier este responsabil pentru inserarea unei noi campanii de strângere de fonduri în baza de date. Utilizatorul poate introduce un titlu, o descriere și o sumă inițială.
#În ambele fișiere, comunicarea cu serverul este realizată prin apelarea API-urilor create în records.js.    

#Am adugat si o componenta de chat de tip OpenAI este o funcționalitate adăugată în aplicația noastră cloud pentru #campanii de strângere de fonduri. Aceasta oferă utilizatorilor posibilitatea de a purta conversații cu un model de limbaj artificial dezvoltat de OpenAI, numit GPT-3.5. Pentru a adăuga o notă de umor conversațiilor, am configurat #modelul OpenAI pentru a răspunde conform rolului de Comedian. Mai exact, am pregătit modelul pentru a #răspunde la fraza "knock knock" (bătaie în ușă, în traducere liberă) cu o glumă.      
#Cream un API key in contul OpenAI - il introducem in .env in aplicatia noastra      
#Adaugam o ruta /chat in aplicatie     
#Adugam o componenta: ChatComponent - stilizare      
#Mesajele vor veni asincron, deci adaugam un state si o componenta care va afisa mesajele si le va redesena de fiecare data cand avem unul nou     
#Adaugam un endpoint care se va ocupa de comunicarea cu OpenAI - /answer        
#Install openai (npm i openai)    
#Configure openai connection in lib/openai.js     
#Configuram endpoint-ul    
#Testam in Postman     
#Adaugam logica de trimitere mesaje     
#Actualizam env variables in productie     


**Flux de date**:             
#Fluxul de date pentru aplicația de fundraising este următorul:     

#Un client trimite o cerere HTTP la server utilizând una dintre metodele HTTP (GET, POST, PUT, PATCH sau DELETE) pentru a accesa, adăuga, actualiza sau șterge date despre o campanie de strângere de fonduri.      

#Serverul primește cererea și o procesează utilizând informațiile din corpul cererii și parametrii din URL. Serverul #poate verifica autorizarea #clientului și dacă cererea este validă.

#Serverul accesează baza de date pentru a obține sau actualiza informațiile despre campania de strângere de fonduri.

#Serverul trimite un răspuns HTTP către client, care conține informațiile solicitate sau un mesaj de confirmare.

**Capturi de ecran**: image.png vezi documentul pdf incarcat pe online.ase la sectiunea Proiect   
![image](https://github.com/Thorrrin/SorinPopescu/assets/131694342/25bf5397-45de-44c8-8aa0-1150be4c0839)    
![image](https://github.com/Thorrrin/SorinPopescu/assets/131694342/d7ac806c-e26b-415a-a30f-f4e2d7b8d844)    
![image](https://github.com/Thorrrin/SorinPopescu/assets/131694342/4bb39d83-892b-4830-b5fa-55c91d6bd05f)
![image](https://github.com/Thorrrin/SorinPopescu/assets/131694342/26d630da-b7ed-47e9-9581-6cb07a7c7eda)     
![image](https://github.com/Thorrrin/SorinPopescu/assets/131694342/679458d6-bd5a-43eb-9f8b-3b2f838c1847)


**Referinte:**

#Vercel. (2021). Vercel Documentation. Retrieved from https://vercel.com/docs         
#React. (2021). React Documentation. Retrieved from https://reactjs.org/docs/getting-started.html    
#Node.js. (2021). Node.js Documentation. Retrieved from https://nodejs.org/en/docs/             
#Express.js. (2021). Express.js Documentation. Retrieved from https://expressjs.com/      
#MongoDB. (2021). MongoDB Documentation. Retrieved from https://docs.mongodb.com/         
#Postman. (2021). Postman Documentation. Retrieved from https://learning.postman.com/docs/getting-started/introduction/   
#JWT. (2021). JWT.io Documentation. Retrieved from https://jwt.io/       
#OBS Studio. (2021). OBS Studio Documentation. Retrieved from https://obsproject.com/wiki/       
#Stack Overflow. (2021). Retrieved from https://stackoverflow.com/      
#GitHub. (2021). GitHub Documentation. Retrieved from https://docs.github.com/en

