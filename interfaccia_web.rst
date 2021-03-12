Interfaccia web
==================================

.. .. image:: img/interfaccia.png

L'interfaccia web dello strumento webGIS è composta principalmente dall'area di mappa dove vengono visualizzati i dati, due toolbar da cui si accede alle principali funzionalità (es. stampa, editing, strumenti di misura e ricerca, ecc.) o agli strumenti di zoom e pan, l'albero dei layer da cui è possibile accendere/spegnere i singoli layer o l'intero gruppo, che verranno automaticamente visualizzati nell'area di mappa, e un menu da cui selezionare lo sfondo cartografico da visualizzare in area di mappa.

Funzionalità di base
-----------------------------
da completare
   


Tabella attributi e selezione
-----------------------------
da completare


Editing 
-----------------------------

Per accedere agli strumenti di editing dello strumento webGIS è necessario fare il login con il proprio utente e password. Solo alcuni utenti hanno i permessi necessari per poter procedere alla modifica e aggiunta on line degi layer, quindi solo questi utenti, una volta loggati, potranno visualizzare e utilizzare gli strumenti di editing.

Una volta entrati con il proprio utente, qualora si abbiano i permessi per la modifica on line, selezionare nella toolbar laterale i pulsante Modifica.
 consente l'editing degli  geometria che deve essere disegnata dall'operatore sulla mappa


Edition tool
""""""""""""""""""""""""""""""""
E' sufficiente selezionare dal menù a tendina il layer che si vuole modificare e premere il tasto "Aggiungi". Una volta selezionato il layer si potrà procedere a disegnare la geometria sulla mappa.
In caso di layer puntuali con un solo click del mouse si crea la nuova geometria che potrà essere spostata tenendo premuto il tasto sinistro del mouse. Per quanto riguarda invece gli eventi lineari, cliccando con il mouse sulla mappa si crea la nuova geometria lineare, a ogni click del mouse corrisponde un nuovo vertice della geometria lineare, con il doppio click del mouse viene terminato l'editing della geometria. Modificando un veneto lineare si attivano inoltre alcuni strumenti di editing che permettono di spostare i singoli vertici della geometria lineare, traslarla, ruotarla e modificarla eliminandone una parte.

.. Sullo strumento webGIS sono implementate funzioni di snap, in fase di editing è quindi possibile "agganciarsi" precisamente alle geometrie delle strade disegnando nuovi percorsi per i giri di raccolta rifiuti.

Una volta disegnata la geometria si può procedere alla compilazione della tabella degli attributi relativa alla geometria appena disegnata. A seconda del leyer che si sta modificando, si possono riempire i diversi campi della tabella inserendo manualmente l'informazione o scegliendola da menù a tendina in caso di colonne con relativa decodifica.
Altre colonne come ad esempio 'data inserimento', 'flag modificato' o 'utente ultima modifica' non sono editabili in quanto vengono automaticamente riempite dal database al momento del salvataggio delle modifice. 
.. Se presenti è possibile caricare nelle colonne predisposte allegati in formato pdf  o delle immagini semplicemente cliccando sul pulsante che peremette di scegliere il file dal proprio pc.
Qualora le colonne definite obbligatorie lato progetto Qgis non venissero compilate, lo strumento restituirà un errore non permettendo all'operatore di salvare le modifiche.

Terminato il disegno geometrico e compilata la tabella è possibile salvare il nuovo elemento premendo sul pulsante salva. Una volta salvata sarà immediatamente visibile sulla mappa.


Stampa
-----------------------------
da completare


