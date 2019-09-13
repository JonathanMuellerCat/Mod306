1. [Introduzione](#introduzione)

   - [Informazioni sul progetto](#informazioni-sul-progetto)

   - [Abstract](#abstract)

   - [Scopo](#scopo)

2. [Analisi](#analisi)

   - [Analisi e specifica dei requisiti](#analisi-e-specifica-dei-requisiti)

   - [Use case](#use-case)

   - [Pianificazione](#pianificazione)
  
   - [Analisi dei mezzi](#analisi-dei-mezzi)
  
     - [Hardware](#hardware)
  
     - [Software](#software)

3. [Progettazione](#progettazione)

   - [Design dell’architettura del sistema](#design-dell’architettura-del-sistema)

   - [Design dei dati e database](#design-dei-dati-e-database)

4. [Implementazione](#implementazione)

5. [Test](#test)

   - [Protocollo di test](#protocollo-di-test)

   - [Risultati test](#risultati-test)

   - [Mancanze/limitazioni conosciute](#mancanze/limitazioni-conosciute)

6. [Consuntivo](#consuntivo)

7. [Conclusioni](#conclusioni)

   - [Sviluppi futuri](#sviluppi-futuri)

   - [Considerazioni personali](#considerazioni-personali)

8. [Sitografia](#sitografia)

9. [Allegati](#allegati)


## Introduzione

### Informazioni sul progetto

  Scuola e classe: SAMT I3AC
  
  Modulo: 306
  
  Alievo: Jonathan Mueller
  
  Docenti: Luca Muggiasca e Geo Peduzzi
  
  Durata progetto: 6.9.2019 - 20.12.2019
  

### Abstract

  E’ una breve e accurata rappresentazione dei contenuti di un documento,
  senza notazioni critiche o valutazioni. Lo scopo di un abstract efficace
  dovrebbe essere quello di far conoscere all’utente il contenuto di base
  di un documento e metterlo nella condizione di decidere se risponde ai
  suoi interessi e se è opportuno il ricorso al documento originale.

  Può contenere alcuni o tutti gli elementi seguenti:

  -   **Background/Situazione iniziale**

  -   **Descrizione del problema e motivazione**: Che problema ho cercato
      di risolvere? Questa sezione dovrebbe includere l'importanza del
      vostro lavoro, la difficoltà dell'area e l'effetto che potrebbe
      avere se portato a termine con successo.

  -   **Approccio/Metodi**: Come ho ottenuto dei progressi? Come ho
      risolto il problema (tecniche…)? Quale è stata l’entità del mio
      lavoro? Che fattori importanti controllo, ignoro o misuro?

  -   **Risultati**: Quale è la risposta? Quali sono i risultati? Quanto è
      più veloce, più sicuro, più economico o in qualche altro aspetto
      migliore di altri prodotti/soluzioni?

  Esempio di abstract:

  > *As the size and complexity of today’s most modern computer chips
  > increase, new techniques must be developed to effectively design and
  > create Very Large Scale Integration chips quickly. For this project, a
  > new type of hardware compiler is created. This hardware compiler will
  > read a C++ program, and physically design a suitable microprocessor
  > intended for running that specific program. With this new and powerful
  > compiler, it is possible to design anything from a small adder, to a
  > microprocessor with millions of transistors. Designing new computer
  > chips, such as the Pentium 4, can require dozens of engineers and
  > months of time. With the help of this compiler, a single person could
  > design such a large-scale microprocessor in just weeks.*

### Scopo

  Lo scopo dei questo progetto è di imparare a gestire progetti a partire da una consegna di un cliente seguendo i modelli imparati in classe (cascata), a documentaro  e a fare i diari settimanali.
  Durante la creazione del progetto ci saranno utili molte nozioni imarate da moduli degli anni passati, come 431, 307, 226 e il corrente 306. Questo progetto ci aiuterà anche ad allenarci per fare progetti futuri come il progetto finale in quarta e quelli che svolgeremo sul posto di lavoro.


## Analisi

### Analisi del dominio

Prima dell'invenzione di questo programma per generare un fiocco di neve si doveva disegnare a mano o ritagliare un foglio di carta. Questo prodotto è originale, e non esietevano prodotti simili prima. Non occorrono competenze per far funzionare il programma i quanto il metodo di utilizzo è descritto sulla pagina web del prodotto.


### Analisi e specifica dei requisiti

- L’applicativo può essere sia Java che in Javascript.
  - Se l'applicazione è Java, va creato un sito web con la descrizione e il download dell’applicazione, con descrizione di tutti i requisiti per il funzionamento.
  - Se l'applicazione è in Javascript va creato un sito web per il suo hosting.
- I punti di “taglio” vengono inseriti cliccando col mouse.
- I punti si devono poter aggiungere e resettare completamente.
  - Bonus: rimozione, spostamento di punti
- Il “fiocco di neve” viene generato quando l'utente clicca il tasto “Genera”
  - Bonus: la generazione avviene in tempo reale con una animazione
- Si può salvare il fiocco di neve come immagine raster in formato PNG e vettoriale in formato SVG (l'utente decide le dimensioni).
- L’applicativo deve permettere di salvare i punti di taglio per poter permettere modifiche
  - rigenerazione future.
- In base al tempo a disposizione, nuovi requisiti possono essere inseriti nel progetto
dopo discussione fra formatore e allievo.


  |**ID**            |Req-1                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |L'applicativo deve essere in Java o in Javascript                              |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  |                  |**Sotto requisiti**                                                            |
  |001               |Se l'applicativo è in Java necessita un sito web con
  - descrizione con screenshots
  - download
  - versione JRE
  - lista con requisiti di sistema
  |  
  |002               |Se l'applicativo è in Javascript, necessita un sito web per il suo hosting     |
  
  |**ID**            |Req-2                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Deve esserci un'interfaccia grafica                                            |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |Può essere ridimensionata (min 1024x768)                                       |
  
  |**ID**            |Req-3                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |L'area di lavoro deve essere un triangolo                                      |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-4                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |I punti di taglio si posizionano con il click del mouse                        |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-5                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |I punti di taglio si possono aggiungere                                        |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-6                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |I punti di taglio si possono resettare                                         |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-7                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |I punti di taglio si possono eliminare                                         |
  |**Priorità**      |2                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-8                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |I punti di taglio si possono spostare                                          |
  |**Priorità**      |2                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-9                                                                          |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Deve esserci un tasto "Genera"                                                 |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-10                                                                         |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Il fiocco di neve viene generato al click del pulsante "Genera"                |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-11                                                                         |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Il fiocco di neve viene generato in tempo reale                                |
  |**Priorità**      |2                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-12                                                                         |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Si può salvare il fiocco                                                       |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-13                                                                         |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Il salvataggio può essere fatto  come immagine BMP o SVG                       |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-14                                                                         |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Il salvataggio deve avere dimenzioni scelte dall'utente                        |
  |**Priorità**      |1                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |
  
  |**ID**            |Req-15                                                                         |
  |------------------|-------------------------------------------------------------------------------|
  |**Nome**          |Si possono salvare i punti di taglio per modifiche future                      |
  |**Priorità**      |2                                                                              |
  |**Versione**      |1.0                                                                            |
  |**Note**          |                                                                               |


### Use case

È presente solo un'attore che interagisce direttamente con l'applicazione.


### Pianificazione

Prima di stabilire una pianificazione bisogna avere almeno una vaga idea
del modello di sviluppo che si intende adottare. In questa sezione
bisognerà inserire il modello concettuale di sviluppo che si seguirà
durante il progetto. Gli elementi di riferimento per una buona
pianificazione derivano da una scomposizione top-down della problematica
del progetto.

La pianificazione può essere rappresentata mediante un diagramma di
Gantt.

Se si usano altri metodi di pianificazione (es scrum), dovranno apparire
in questo capitolo.


### Analisi dei mezzi

#### Hardware ####

PC messo a disposizione dalla scuola con Windows

Portatile MacBook Pro personale


#### Software ####

Pacchetto WAMP (Apache, MySQL, PHP, ecc...)

Java (JDK 11.1)

GitHub


## Progettazione

Questo capitolo descrive esaustivamente come deve essere realizzato il
prodotto fin nei suoi dettagli. Una buona progettazione permette
all’esecutore di evitare fraintendimenti e imprecisioni
nell’implementazione del prodotto.

### Design dell’architettura del sistema

Descrive:

-   La struttura del programma/sistema lo schema di rete...

-   Gli oggetti/moduli/componenti che lo compongono.

-   I flussi di informazione in ingresso ed in uscita e le
    relative elaborazioni. Può utilizzare *diagrammi di flusso dei
    dati* (DFD).

-   Eventuale sitemap

### Design dei dati e database

Descrizione delle strutture di dati utilizzate dal programma in base
agli attributi e le relazioni degli oggetti in uso.

### Schema E-R, schema logico e descrizione.

Se il diagramma E-R viene modificato, sulla doc dovrà apparire l’ultima
versione, mentre le vecchie saranno sui diari.

### Design delle interfacce

Descrizione delle interfacce interne ed esterne del sistema e
dell’interfaccia utente. La progettazione delle interfacce è basata
sulle informazioni ricavate durante la fase di analisi e realizzata
tramite mockups.

### Design procedurale

Descrive i concetti dettagliati dell’architettura/sviluppo utilizzando
ad esempio:

-   Diagrammi di flusso e Nassi.

-   Tabelle.

-   Classi e metodi.

-   Tabelle di routing

-   Diritti di accesso a condivisioni …

Questi documenti permetteranno di rappresentare i dettagli procedurali
per la realizzazione del prodotto.

## Implementazione

In questo capitolo dovrà essere mostrato come è stato realizzato il
lavoro. Questa parte può differenziarsi dalla progettazione in quanto il
risultato ottenuto non per forza può essere come era stato progettato.

Sulla base di queste informazioni il lavoro svolto dovrà essere
riproducibile.

In questa parte è richiesto l’inserimento di codice sorgente/print
screen di maschere solamente per quei passaggi particolarmente
significativi e/o critici.

Inoltre dovranno essere descritte eventuali varianti di soluzione o
scelte di prodotti con motivazione delle scelte.

Non deve apparire nessuna forma di guida d’uso di librerie o di
componenti utilizzati. Eventualmente questa va allegata.

Per eventuali dettagli si possono inserire riferimenti ai diari.

## Test

### Protocollo di test

Definire in modo accurato tutti i test che devono essere realizzati per
garantire l’adempimento delle richieste formulate nei requisiti. I test
fungono da garanzia di qualità del prodotto. Ogni test deve essere
ripetibile alle stesse condizioni.


|Test Case      | TC-001                               |
|---------------|--------------------------------------|
|**Nome**       |Import a card, but not shown with the GUI |
|**Riferimento**|REQ-012                               |
|**Descrizione**|Import a card with KIC, KID and KIK keys with no obfuscation, but not shown with the GUI |
|**Prerequisiti**|Store on local PC: Profile\_1.2.001.xml (appendix n\_n) and Cards\_1.2.001.txt (appendix n\_n) |
|**Procedura**     | - Go to “Cards manager” menu, in main page click “Import Profiles” link, Select the “1.2.001.xml” file, Import the Profile - Go to “Cards manager” menu, in main page click “Import Cards” link, Select the “1.2.001.txt” file, Delete the cards, Select the “1.2.001.txt” file, Import the cards |
|**Risultati attesi** |Keys visible in the DB (OtaCardKey) but not visible in the GUI (Card details) |


### Risultati test

Tabella riassuntiva in cui si inseriscono i test riusciti e non del
prodotto finale. Se un test non riesce e viene corretto l’errore, questo
dovrà risultare nel documento finale come riuscito (la procedura della
correzione apparirà nel diario), altrimenti dovrà essere descritto
l’errore con eventuali ipotesi di correzione.

### Mancanze/limitazioni conosciute

Descrizione con motivazione di eventuali elementi mancanti o non
completamente implementati, al di fuori dei test case. Non devono essere
riportati gli errori e i problemi riscontrati e poi risolti durante il
progetto.

## Consuntivo

Consuntivo del tempo di lavoro effettivo e considerazioni riguardo le
differenze rispetto alla pianificazione (cap 1.7) (ad esempio Gannt
consuntivo).

## Conclusioni

Quali sono le implicazioni della mia soluzione? Che impatto avrà?
Cambierà il mondo? È un successo importante? È solo un’aggiunta
marginale o è semplicemente servita per scoprire che questo percorso è
stato una perdita di tempo? I risultati ottenuti sono generali,
facilmente generalizzabili o sono specifici di un caso particolare? ecc

### Sviluppi futuri
  Migliorie o estensioni che possono essere sviluppate sul prodotto.

### Considerazioni personali
  Cosa ho imparato in questo progetto? ecc

## Bibliografia

### Bibliografia per articoli di riviste
1.  Cognome e nome (o iniziali) dell’autore o degli autori, o nome
    dell’organizzazione,

2.  Titolo dell’articolo (tra virgolette),

3.  Titolo della rivista (in italico),

4.  Anno e numero

5.  Pagina iniziale dell’articolo,

### Bibliografia per libri


1.  Cognome e nome (o iniziali) dell’autore o degli autori, o nome
    dell’organizzazione,

2.  Titolo del libro (in italico),

3.  ev. Numero di edizione,

4.  Nome dell’editore,

5.  Anno di pubblicazione,

6.  ISBN.

### Sitografia

1.  URL del sito (se troppo lungo solo dominio, evt completo nel
    diario),

2.  Eventuale titolo della pagina (in italico),

3.  Data di consultazione (GG-MM-AAAA).

**Esempio:**

-   http://standards.ieee.org/guides/style/section7.html, *IEEE
    Standards Style Manual*, 07-06-2008.

## Allegati

Elenco degli allegati, esempio:

-   Diari di lavoro

-   Codici sorgente/documentazione macchine virtuali

-   Istruzioni di installazione del prodotto (con credenziali
    di accesso) e/o di eventuali prodotti terzi

-   Documentazione di prodotti di terzi

-   Eventuali guide utente / Manuali di utilizzo

-   Mandato e/o Qdc

-   Prodotto

-   …
