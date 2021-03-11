Funzionalità di editing 
==================


Editing dei Percorsi
------------------------
On line o in ambiente desktop tramite il progetto QGIS dedicato: percorsi.qgs
Da completare



Editing degli indirizzi
------------------------


Le problematiche
+++++++++++++++++++++++
L'indirizzario comunale (tabella t_civici) è alla base della localizzazione degli indirizzi delle utenze servite dal servizio di raccolta rifuiti porta a porta.
In fase di implementazione delle query che consente di agganciare le anagrafiche con gli indirizzi della banca dati comunale sono emerse una serie di criticità che richiedeno interventi correttivi.
Le chiavi di aggancio impiegate sono Codice Via Comunale, Numero civico , Esponente.

I possibili esiti di questa operazione sono stati suddivisi su più layer per una più agevole consultazione:
#. Aggancio univoco:  relazione 1:1 tra l'indirizzo in anagrafica e indirizzario comunale

#. Aggancio fallito: non è possibile trovare una corrispondenza 

#. Aggancio fallito per via assente nell'indirizzario: non è possibile trovare una corrispondenza perchè nell'indirizzario non sono presenti indirizzi per quella specifica strada

#. Agganci multipli: relazione 1:n tra l'indirizzo presente in anagrafica e indirizzo presente tra i civici del comune dovuto alla presenza di duplicati nell'indirizzario comunale. In altri termini, a parità di codvia, numero civico, esponente sono presenti record con posizioni (geometrie) differenti. 



Cosa modificare 
+++++++++++++++++++++++
Di volta in volta sarà necessario valutare se modificare i dati relativi alle anagrafiche dei clienti o la banca dati degli indirizzi comunali. 
Le correzioni degli indirizzi associati alle anagrafiche devono essere effettuate tramite il gestionale ad uso interno.
Per correzioni degli indirizzi comunali è possibile lavorare on line o in ambiente desktop tramite il progetto QGIS dedicato: correzioni_indirizzi.qgs


Il progetto QGS per la correzione degli indirizzi
+++++++++++++++++++++++
Si descrivono di seguito i pricipali layer caricati nel progetto :

* Civici del Comune (t_civici) : un circoletto piccolo blu per ogni civico presenti nell'indirizzario comunale (esclusi i civici del Centro Storico).
* Aggancio univoco (v_aggancio_univoco) : un circoletto verde laddove l'aggancio anagrafica-civici ha esito positivo
* Aggancio multiplo (v_agganci_multipli) : un circoletto arancione laddove l'aggancio anagrafica-civici produce più candidati 
* Civici duplicati (v_civici_duplicati) : per evidenziare la casistica precedente anche in assenza di anagrafiche da agganciare
* (v_civici_non trovati) : tabella alfanumerica con indicazione del numero di contratto 
* (v_codvia_assente) : tabella alfanumerica con indicazione del numero di contratto 
Gli altri layer (stradario, limiti amministrativi,  frazioni, ) servono, al bisogno, ad inqauadrare il contesto territoriale.

Gli unici layer editabili sono Civici del Comune (t_civici) e la tabella alfanumerica dello Stradario (stradario_comunale).

La maschera di editing dell'indirizzario richiede di compilare i seguenti campi:

* Via: obbligatorio, è possibile scegliere la denominazione della via da un elenco a discesa che compare non appena si inizia a digitare al prima lettera
* Numero : il numero civico, obbligatorio
* Lettera : l'espondente, non obbligatorio
Il campo flag_modificato serve ad individuare le correzioni effettuate alla banca dati comunale, è un booleano e non è editabile perchè popolato automaticamente in caso di inserimento di un nuovo record o di modifica di un record esistente.

La modifica dello stradario comunale è da utilizzare solo nel caso in cui, a causa di mancato aggiornamento della fonte dati, fosse necessario inseire nuove strade o modificare la donominazione di strade esistenti.

Le correzioni
+++++++++++++++++++++++

Di seguito, nel dettaglio, le operazioni da eseguire caso per caso.

1.Indirizzi non agganciati
+++++++++++++++++++++++


2.Indirizzi non agganciati per via assente nell'indirizzario
+++++++++++++++++++++++
Questo rappresenta un caso particolare rispetto al precedente. L'aggancio 

3.Agganci multipli
+++++++++++++++++++++++
