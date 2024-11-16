# Networking-
Learning Material

Rețele de calculatoare 

Host - orice dispozitiv parte din rețea ce poate primi/trimite date - fiecare host are o adresa unica 
Hub - împarte conexiunea rețelei la mai multe calculatoare
Switch - grupează toate calculatoarele din rețea pentru a transmite datele către alt dispozitiv și e mai bun ca hub-ul deoarece duce datele de la sursa la destinație fără a le emite în rețea 
Router - conectează LAN-ul la internet / conectează mai multe calculatoare la internet 
Modem - conectează calculatorul la internet folosind o linie de telefonie. E un echipament intern pc-ului (pe placa de baza) folosit mai rar astăzi.

Utilizari : 
	- permite partajarea resurselor eliminând necesitatea prezentei fizice a echipamentului în locația unde se solicita datele 
	- se folosește în modelul client-server ( serverul este un calculator central folosit pentru stocarea informațiilor și este administrat, iar clienții sunt calculatoarele ce solicita date de la sv ) 
	- reprezintă un mediu de comunicare 
	- e-commerce 

Avantaje 
	- back-up si roll-back de la server 
	- partajare software & hardware - se poate instala software direct pe server fără a mai fi nevoie sa fie instalat pe fiecare mașină în parte. Idem hardware
	- scalabilitate și fiabilitate ( pe măsură ce rețeaua se extinde, viteza transferului de date scade și creste predispoziția apariției de erori, dar aceasta problema poate fi depășită cu switch-uri și routere 


Arhitectura rețelei de calculatoare

a. Peer-to-peer 
	- toate calculatoarele sunt legate între ele și au privilegii și responsabilități egale ( de preferat max 10 calculatoare ) 
	- nu are server dedicat 
	- se aloca permisiuni fiecărui calculator pentru partajarea resurselor, dar pot apărea probleme dacă calculatorul cu resursa e picat 
	Avantaje 
		- costuri reduse
		- dacă pică un pc celelalte nu sunt afectate
		- usor de instalat 
	Dezavantaje 
		- Nu conține sistemul centralizat deci fără back-up 
		- Probleme de securitate întrucât fiecare 	calculator se gestionează singur 
b. Client-server
	- creat pentru utilizatori (clienți) sa acceseze resurse (poze, cântece, videos) 
	- controller-ul central este cunoscut ca server 
	- un server realizează toate operațiunile majore de la securitate la gestiunea rețelei
	- server-ul este responsabil de gestiunea resurselor (fisiere,foldere,printere)
	- dacă un calculator dorește sa comunice cu un altul atunci va trimite cererea către server, care va permite sau nu comunicarea 

	Avantaje
		- o rețea client-server conține sistemul centralizat deci se pot recupera date 
		- contine un server dedicat care creste performanta sistemului
		- o mai buna securitate deoarece resursele sunt gestionate de un singur server 
		- creste viteza de partajare a resurselor 
	Dezavantaje
		- scump, server-ul are nevoie de memorie
		- un sv are un NOS (Network Operating System) ca sa distribuie resursele către clienți
		- necesita un admin de reta


Componente 

Componentele sunt părțile principale necesare pentru instalarea software-ului. NIC, switch, cablu, hub, router, modem.
În functie de tipul rețelei unele componente pot fi redundante 

NIC  - adresa MAC sau adresa fizica este unica și este pastrata în PROM (Programmable read-only memory)
HUB - dispozitiv fizic ce răspândește conexiunea între alte calculatoare. Când un calculator solicita o informație de la rețea, acesta trimite solicitarea mai întâi către HUB care la rândul sau o distribuie la celalalte calculatoare. Toate vor verifica dacă solicitarea le apartine, în caz contrar solicitarea este ignorata. 

Tipuri de retele
 a. LAN
b. MAN
c. WAN 
d. PAN 
e. InternetWork 
	- e data de conectarea a doua sau mai multe LAN sau MAN 
	- folosește protocolul internet
	- modelul de referenda este Open System Interconnection ( OSI ) 
	Tipuri de InternetWork
	1. Extranet 	
		- rețea de comunicare bazată pe Transmission Control protocol și internet protocol.
		- utilizatorii au nevoie de credentiale pentru acces
		- nu poate avea doar un LAN, trebuie sa aibă măcar o conexiune la rețeaua externa 
	2. Intranet
		- retie dedicata numai angajaților unei organizații
		Avantaje intranet
		- comunicare ieftină
		- informatia e transmisa în timp real => eficienta
		- arhitectura neutra deoarece un calculator se poate conecta cu un altul care are o alta arhitectura
		- reduceri de cost 

Topologia retelei 

	Specifica structura rețelei anume cum sunt conectate componentele. Exista doua tipuri : fizica și logica
a. Topologia fizica e reprezentarea geometrica a tututor nodurilor dintr-o rețea
	Exista 6 tipuri : Bus, Ring, Tree, Star, Mesh si Hibrida
	1. Bus - toate stațiile sunt conectate la un cablu ‘backbone’
			- cand un nod vrea sa trimită un mesaj peste rețea acesta va trimite mesajul intregei rețele, toate stațiile primesc mesajul indiferent dacă le este adresat sau nu
			- folosita în principal în rețele standard de tip 802.3(ethernet) și 802.4 
			- configurare simpla 
			- cea mai întâlnită metoda de acces pentru topologia bus e CSMA ( Carrier Sense Multiple Access ) 
CSMA - control de acces media folosit pentru a gestiona fluxul datelor astfel încât integritatea lor sa se păstreze (sa nu se piardă pachete)
	i. CSMA CD (collision detection) metoda de acces Folosita pentru detectarea coliziunilor. Lucrează pe ‘recuperare după Coliziune’ deoarece odată ce se detectează coliziunea emițătorul va înceta transferul de date.
	ii. CSMA CA (collision avoidance) - verifica daca mediul de transmisie este ocupat sau nu, dacă este ocupat emițătorul va aștepta pana când mediul se eliberează 
Avantaje Bus
	- cost redus pentru cabluri (toate sunt interconectate) 
	- viteze moderate prin cabluri coaxiale și împletite ce suporta pana la 10Mbps
	- tehnologie prea bine cunoscuta cu dispozitive fizice ieftine 
	- limitarea dezastrului - nefuncționarea unui nod nu le impacteaza pe celelalte
Dezavantaje Bus
	- prea mult cablu
	- dacă se taie cablul (necesita echipament pentru depistare) pică toată rețeaua
	- interferenta de semnal în situația în care doua noduri transmit mesaje simultan
	- reconfigurare dificila - adăugarea de noi dispozitive încetinește rețeaua
	- atenuarea semnalului - fix : sunt folosite relee ( repeaters ) 

	2. Topologie inel
	- ca bus, dar cu capetele conectate
	- un nod primeste mesajul de la nodul precedent și trimite către următorul 
	- datele ‘Curg’ intr-o singura direcție - clockwise  / în forma unei bucle continue 
	- nu exista un capăt - fiecare nod e conectat cu altul 	
	- cea mai întâlnită metoda de acces pentru inel este pasarea de token-uri de la un nod la altul. Token - cadru ce circula în rețea 
	Pasarea token-urilor:  circula în rețea și e pasat de la un calculator la altul pana ajunge la destinație 
- Expeditorul modifica token-ul prin alipirea adresei la datele mesajului 
- Când adresa dispozitivului corespunde cu cea din token, dispozitivul destinatar va trimite o Înștiințare către dispozitivul expeditor

	3. Star 
	- Dispoziția nodurilor în forma stea se face prin interconectarea lor la un hub central
	- Calculatorul central este cunoscut ca server, restul nodurilor clienți 
	Dezavantaje: nefuncționarea serverului 

	4. Copac = bus + star 
	5. Mesh = patrat cu diagonale ( > 3 legături pe nod ) 
		- se realizează după formula  NrCabluri = (n*(n-1))/ 2 
	6. Hybrid = combinație din toate 

Moduri de transmisie ( mod de comunicare / direcționare ) 
 	- Fiecare canal de comunicare are o direcție asociata data de modul de transmisie care se regăsește în stratul fizic al rețelei. 
A. Simplex mode 
	- Unidirecțional, un nod poate doar trimite sau primi de la altul 
	- ex: statie radio - primeste dar nu transmite, tastatura primeste, monitorul emite
	- folosit în organizații unde este nevoie doar sa se trimită date 
B. Half-duplex mode 
	- transmisiune în ambele direcții dar nu simultan 
	- toată banda e Folosita când se transmite intr-o anumită direcție 
	- ex : walkie-talkie - o persoana vorbește și una asculta 
	- dezavantaj : cât timp un nod emite celălalt trebuie sa aștepte pana termina 
C. Full-duplex mode 
	- mod de comunicare bidirectional = ambele stații pot transmite și recepționa simultan 		
	- construit din doua simplex pentru fiecare direcție 
	- rapid, ex: rețea de telefonie mobila - ambele persoane pot vorbi și asculta in același timp


Modele de rețea de calculatoare 

	Arhitectura stratificata
	- dezvoltat de ISO pentru a împarți design-ul în părți mai mici 
	- fiecare strat de mai jos deservește stratul superior 
	- asigura independența între straturi punând serviciile din stratul inferior la dispoziția stratului superior fără a specifica cum sunt acestea implementate 
	- numărul de straturi, funcții, conținut al fiecărui strat diferă de la o rețea la alta
 	- serviciul este setul de acțiuni pe care un strat inferior îl oferă către stratul superior 
	- protocolul reprezintă un set de reguli despre conținut și ordinea mesajelor pe care un strat îl folosește pentru a schimba informații cu o entitate pereche 
	- interfața - modul în care se transfera informații 
	- în arhitectura stratificata *ex: stratul N al unei rețele va comunica cu stratul N al altei rețele, dar ele nu comunica direct ci pasează datele către stratul inferior pana se ajunge la cel mai de jos strat 
	- sub stratul 1 se afla mediul fizic unde are loc comunicarea efectivă 
	- In arhitectura stratificata cerintele greu de gestionat sunt împărțite în părți mai mici (divide et impera)
	- arhitectura = protocoale + straturi 
	- Avantaje:  abordarea divide et impera, modularitatea straturilor, ușor de modificat și de testat 

	Modelul OSI (Open System Interconnection - ISO 1984) 
	- model de referinta care descrie cum informația dintr-un software de pe un computer traversează mediul fizic pentru a ajunge într-un soft de pe alt pc
	- 7 straturi fiecare cu funcția sa de rețea ( task-urile sunt împărțite în 7 subtask-uri pt fiecare strat gestionate independent )
	- Responsabilitatea host-ului = [ Aplicație, Prezentare, Sesiune, Transport ] = straturi superioare, implementate în software - folosite atât de utilizator cât și de aplicație 
	- Responsabilitatea rețelei = [ Rețea, Data Link, Fizic ] = straturi inferioare folosite în transportul datelor. Straturile Data Link și cel Fizic sunt implementate atât în soft cât și în echipamentul hardware. Stratul fizic se ocupa de plasarea datelor în mediul fizic de conexiune 
1. Strat Aplicatie - oferă serviciile utilizatorului 
2. Strat Prezentare - traduceri, compresii, criptare 
3. Strat Sesiune - realizează și încheie sesiuni 
4. Strat Transport - corespondenta mesaje între procese   - se asigura ca mesajele sunt transmise în ordinea în care au fost trimise și ca datele nu au fost duplicate  - responsabilitate principala este transferul complet al datelor  - primește ‘bucăți’ de date de la stratul sesiune și le convertește în unități mai mici numite segmente  2 Protocoale folosite:  i. Protocolul Controlului de Transmisie (TCP) - protocol standard ce menține conexiunea între gazde  - când se transmit date prin protocolul TCP, atunci protocolul împarte datele în segmente. Fiecare segment traversează internetul folosind rute multiple și ajung la destinație în ordine diferită. La destinație TCP le rearanjează în ordinea inițială ii.  
5. Strat Retea - muta pachete de la sursa la destinație  - gestionează adresarea dispozitivelor, urmărind locația acestora -determina cea mai buna cale de transfer a datelor / data-link fiind responsabil de routare a pachetelor  -routerele sunt dispozitive specificate în acest strat  -protocoalele folosite pentru routarea traficului de internet sunt cunoscute ca protocoale ale stratului de rețea : IP, IPv6 Funcții: - internetworking - responsabilitate principala - oferă o conexiune logica între dispozitive - adresare - Folosita pentru identificarea dispozitivului pe internet  - routare - oferă cea mai buna cale  - pachetizare - stratul rețea primește ‘Segmente’ de date de la stratul transport și le împachetează mai departe corespunzător 
6. Strat Data Link - transfer lipsit de erori al cadrelor de date; definește formatul datelor transmise în rețea; responsabil de identificarea unica a fiecărui dispozitiv dintr-o rețea locala; conține 2 substraturi : Strat de control al legăturii logice - responsabil de transferul pachetelor către stratul Rețea al receptorului; identifica adresa din antet și  Stratul de control al accesului media - transfera pachetele în rețea  Funcții: Încadrare - transpune bitii din fluxul fizic neprelucrat în pachete numite Cadre; Adaugă un Header și un Trailer pachetului. Header-ul conține adresele sursa și destinație; Adresare fizica  Control de flux - cea mai importanta - e tehnica prin care rata constanta de transfer a datelor se menține la ambele capete astfel încât datele sa nu fie corupte. Se asigura ca stația de transmisie cu o putere de procesare mai mare nu depășește capabilitățile de procesare ale stației de Recepție Control de erori - Adaugă o valoare calculata la Trailer  numita CRC ( Cyclic Redundancy Check ) care se Adaugă la cadrul pachetului înainte de transmiterea către stratul fizic. Dacă apare vreo eroare, receptorul trimite înștiințarea de retransmisie a pachetelor corupte  Control de acces - când doua sau mai multe calculatoare sunt conectate la același canal de comunicare, protocoalele stratului data link determina ce calculator deține controlul legăturii la un moment dat 
7. Strat Fizic - oferă mediul fizic prin care circula bitii; Principala funcție este de transfer de biti între noduri; Realizează/menține/încheie conexiunea fizica; oferă specificațiile de rețea mecanice, electrice și procedurale  Funcții:  Configurarea liniei (definește cum se conectează fizic doua sau mai multe dispozitive); Transmisia de date ( modul de transmisie simplex/half-duplex/duplex ) ; Topologia - aranjamentul; Semnalul - tipul de semnal folosit pentru transmiterea informațiilor 
 
	
