 2024-10-25 12:11

Tags: [[Organizacija]] [[razvoj zadataka]] [[dobit organizatora]]

TLDR; Jeopardy style igra, bila online, ovo je case study o tome kako su se mučili s organizacijom - primarno kako su slagali zadatke i što su kao organizatori dobili od toga što su organizirali. Podaci su jako ograničeni chatovi organizatora i zapis s jednog sastanka i anotatori se nisu previše slagali oko kategorije svih poruka pa sve uzeti sa zrnom soli. 

# Bilješke - On the Other Side of the Table
Paper o tome kako organizatori CTF-ova dizajniraju i odobravaju izazove i o motivaciji zašto postati organizator CTF-a.

Metoda je koristeći podatke iz chata jedno CTF-a ( jel to chat organizatora ili je in-game za postavljanje pitanja ili nešto treće?) kao case study (znači nije da svi tako rade.)

Rezultati: organizator prate set koraka za razvoj izazova, ali se muče s evaluacijom težine, vettingom i kako napraviti izazove koje natjecatelji mogu riješiti bez obzira na iskustvo. 


## Intro:

CTF zadaci su inspirirani ranjivostima usoftveru u stvarnom svijetu, ali su potrebne modifikacije da bi zadatak bio rješiv u kraćem vremenu i da bi se natjecatelji fokusirali na ključne koncepte.

Organizatori CTF-a su odgovorni za sve od stvaranja zadataka do održavanja platforme. 
U radu se za case study obrađuje UMDCTF 2020. i traže se metode na koje se razvijaju i odobravaju zadaci. 

RQs:
- Q1: What is the challenge development life cycle? 
• Q2: How are challenges vetted by the CTF organizers? 
• Q3: What motivates a CTF organizer to help in organization and what do they gain? 
•Q4: What topics do organizers discuss, and at what point in the CTF process?

Problemi na koje su naišli: 
- mali resursi (novac, ljudi, vrijeme, znanje?)
- kako ocijeniti težinu zadatka ako ga oni sami znaju riješiti
- koji su koraci za razviti zadatak
- logistička pitanja

## Related work
Eagle et al. kažu da su predavanja **konstrukcionistička** - fokusiraju se na stvaranje boljih sustava ili **protekcionistička** - fokusiraju se na učenje kako zaštititi trenutni sustav. 
CTF-ovi podučavaju **dekonstrukcionistički** - studenti uče o sigurnosti ponašajući se kao napadači.

Poznati problemi koji sprečavaju učenje u CTF-ovima:
- različito iskustvo natjecatelja -> neki se osjećaju left out kad prvi put sudjeluju, bilo zbog nedostatka znanja o sigurnosti ili zbog nedostatka komunikacije pri razvoju izazova (?)
- Organizatori moraju napraviti zadatke tako da su dovoljno izazovni da se nauči nešto novo, ali da nisu preteški da se udalji početnike

## CTF Case Study
UMDCTF 2020 - 18. travnja, cjelodnevno natjecanje (24h)
Jeopardy style
136 zadataka - Cryptography, Exploitation, Forensics, Steganography, Reverse Engineering, Web, RF i Misc.
1000+ natjecatelja iz preko 50 država - valjda ugl. studenti, ali i srednjoškolci i profesionalci
samo 11 organizatora - studenti na preddiplomskom i diplomskom studiju

bio online jer Covid
-> nije bilo fizičkih sastanaka organizatora -> slabija komunikacija
-> kako nije moralo biti uživo, mogli su online sudjelovati ljudi koji žive dalje

## Metode
3 faze:
- priupljanje podataka iz chatova
- anonimizacija i cenzuriranje podataka
- analiza podataka kvalitativnim kodiranjem

### Prikupljanje podataka
interni zapisi iz chatova (slack, zoom, discord) i bilješke sa sastanaka
Organizatori nisu imali ujedinjen i standardiziran pristup komunikaciji -> drugačija analiza za svakog od organizatora

Primarna platforma - Slack
- skoro svi su ga koristili prije CTF-a, ali ne i tijekom 
- prikupljeno samo 654 posljednjih poruka - od 9.ožujka 2020 nadalje.
	- jer slack briše poruke ako nisi na paid subscriptionu
	
Zoom
- zamjena za sastanke uživo
- 2 calla - infrastrukturna pitanja, update oko stanja razvoja zadataka
- Prikpuljeni audio podaci samo s drugog sastanka - 17. travnja - zapisani ručno i anonimizirani

Discord:
- korišten tijekom CTF-a, ne prije
- organizatori koristili više različicih kanala
- podaci prikupljeni samo 321 poruku iz jednog kanala koji je služio koordinaciji događaja

Anketa
- kratka anonimna anketa organizatorima nakon ctf-a

### Anonimizacija i redakcija
ne bih rekla da je nama bitno

### Analiza podataka
![[Pasted image 20241025131954.png]]
svaka poruka je kodirana u skladu s tablicom iznad.

Suglasnost (cohen's Kappa) 2 anotatora je 0.64 za primarne i 0.73 za sekundarne tagove

### Ograničenja
Kasno se počelo sa skupljanjem podatka, jedan sastanak na discordu uopće nije bio snimljen
nisu svi organizatori dopustili da se koriste njihove poruke pa je dio podataka zato nestao ili mu je nedostajao kontekst.
Nije se pratio cijeli proces nego samo zajedničke interakcije organizatora pa je puno zadataka vjj napravljeno i bez da su se spomenuli u porukama u datasetu
2 autora rada su također bili organizatori pa je prisutan neki bias, ali oni nisu sudjelovali kao koderi. 

2020 je bila posebna godina jer se UMDCTF nije prije organizirao na takav način pa ovo nije pogled u to kako inače rade. 

## Rezultati
### Challenge development lifecycle
![[Pasted image 20241025132851.png]]
Počinje od challenge ideje - često inspirirana nekim prošlim zadacima, nekom istraživačkom temom ili nejim konceptom.

Organizatori nisu baš pričali o idejama za zadatke, vjv da bi se spriječilo stvaranje sličnih zadataka, ali su također imali zajedničke neformalne sastanke za stvaranje zadataka i bacanje ideja. 


Kad razvijaju zadatak, u njega ubaci flag,  i sve datoteke vezane za zadatak ( uključujući README s opisom problema i hashem zastavice) pushaju u privatni Github repo za natjecanje

Malo informacija među porukama je bilo o tome kako se hostaju neki zadaci i kakva je infrastruktura


### Challenge distribution and vetting
Kad netko napravi zadatak i pusha ga, podijeli ga na slacku da drugi probaju riješiti. 
	Remark: Moglo se neki bot napraviti da za svaki zadatak dolazi porukau  neki kanalu umjesto da autor mora ručno dodavati
Zadatke **najčešće** reviewa nekoliko organizatora, ali ne uvijek. Zbog ograničenog vremena neke zadatke testira samo jedan organizator -> neki zadaci ipsadne da su nerješili ili imaju bugove ili su prejednostavni. 


Budući da se čini da je organizacija na volonterskoj bazi, neki organizatori su odbijali pisati write-upove ili dodatan posao. 
U podacima nema dokaza o standardiziranom načinu dodjeljivanja težine/bodova zadacima. Nekada čak ni autor zadatka nije znao koju težinu mu pridijeliti. 

Testiranje se može koristiti za dodjeljivanje težine, ali organizatori kao volonteri nemaju resurse za odraditi to na dobar način. 


Opcije za ocjenjivanje: 
statičko i dinamičko

Statičko ocjenjivanje: 
zadatak vrijedi konstantan broj bodova
Dinamičko ocjenjivanje: broj bodova varira o točnosti predane zastavice, vremenu između otvaranja zadatka i predaje rješenja, broju timova koji su riješili zadatak. 
	tužno za neiskusne timove jer će oni riješiti samo jednostavne zadatke koje svi mogu riješiti a na njima će bodovi biti manji
	isto tako, početnički timovi neće znati koje zadatke početi rješavati pa možda zapnu predugo na nečemu teškome. 

### Motivacija organizatora
nama manje bitno



