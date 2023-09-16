<div align="center">
  <a href="#">
  	<img src="https://raw.githubusercontent.com/lbabbu/Application-Logo-App-LOL/main/LOL-logo.png" alt="Logo project" height="160" />
  </a>
  <br>
  <br>
  <p>
    <b>Limited outdoor localization App</b>
  </p>
  <p>
     <i>Applicazione user-friendly che sfrutta il machine learning e la regressione lineare multivariabile per predirre la posizione dell’utente. 
</i>
  </p>
</div>

---

**Content**

- [Descrizione](#descrizione)
- [Features ✨](#features-)
- [Installazione 🐙](#installazione-)
- [Utilizzo 💡](#utilizzo-)
- [Permessi richiesti all'utente](#permessi-richiesti-allutente)
- [Esempi di codice 🖍](#esempi-di-codice-)
- [Documentazione 📄](#documentazione-)
  - [Metodi](#metodi)
  - [API](#api)
  - [Librerie](#librerie)

## Descrizione

Questa applicazione è un potente strumento per la localizzazione outdoor in spazi limitati, che offre una soluzione basata sul machine learning. Lâpp è suddivisa in 4 pagine: trilaterazione (a scopo dimostrativo), scansione dell'area, database delle aree e predizione della posizione.

Il tab 'Trilaterazione' utilizza la potenza del segnale di Wi-Fi e reti cellulari per calcolare la posizione dell'utente. Al tocco del pulsante di rilevamento, l'applicazione genera una lista di reti nelle vicinanze, seleziona le tre con la distanza stimata minore e quindi determina la posizione dell'utente.

Nel tab 'Scansione dell'area', gli utenti possono scansionare un'area specifica e raccogliere tutti i dati dei vari sensori del dispositivo, mentre il tab 'Database di aree' fornisce un elenco di tutte le aree precedentemente scansionate.

Il cuore dell'applicazione si trova nel tab 'Predizione della posizione', dove il machine learning, attraverso l'uso di modelli di regressione lineare, prevede la posizione dell'utente basandosi sui dati precedentemente scansionati.

Questa applicazione offre quindi un metodo per la localizzazione outdoor, in grado di girare interamente in locale sul dispositivo e senza doversi apppoggiare a servizi a pagamento o server esterni per salvare o allenare i dati delle scansioni.

## Features ✨

###Trilateration

- Rilevamento di reti Wi-Fi e cellulari: l'applicazione è in grado di generare un elenco di reti Wi-Fi e reti cellulari nelle vicinanze attraverso la pressione di un pulsante di rilevamento.

- Creazione di un elenco unificato: una volta completata la scansione, le liste separate di reti Wi-Fi e cellulari vengono consolidate in un unico insieme.

- Classificazione basata sulla distanza: l'elenco unificato viene ordinato in base alla distanza dal dispositivo ai punti di rete, e vengono selezionati i primi tre punti per garantire la massima precisione.

- Identificazione di punti noti: se un punto di rete identificato durante la scansione coincide con un punto noto nel relativo file CSV, questo viene evidenziato in rosso per una facile identificazione.

- Algoritmo di trilaterazione: l'applicazione utilizza un avanzato algoritmo di trilaterazione per determinare la posizione stimata dell'utente quando sono disponibili almeno tre punti noti.

- Visualizzazione della posizione prevista: la posizione stimata dell'utente viene visualizzata direttamente all'interno dell'applicazione.

- Integrazione con Google Maps: l'utente ha la possibilità di visualizzare la posizione prevista in Google Maps cliccando sul pulsante "open in google maps".

###Machine learning

- Selezione della posizione sulla mappa: consente agli utenti di selezionare con precisione la loro posizione reale su una mappa interattiva, fornendo un punto di riferimento visivo durante l'utilizzo dell'applicazione.

- Menu a tendina intelligente: Nella pagina di scan è presente un menu a tendina, nel quale ci sono tutte le opzioni che un utente può effettuare durante la scansione, inoltre l'utente è aiutato da una UI intuitiva e da delle icone per favorire la comprensione.

- Continuazione della scansione: l'opzione "Continua scan" permette agli utenti di riprendere una scansione interrotta senza la necessità di creare un nuovo file. Questo facilita la gestione dei dati e consente un risparmio di tempo.

- Salvataggio dei modelli scansionati: Grazie all'applicazione che gira completamente in locale, non vi è bisogno di alcun database interno o esterno per salvare le varie scansioni. Quando l'utente decide di allenare il modello con i dati che ha appena scansionato, il modello viene riempito con i dovuti coefficienti e salvato in un file CSV all'interno del file system del dispositivo.

- Nella pagina della lista dei modelli, vi è anche un bottone "Download"; che permette all'utente di scaricare immediatamente sul suo dispositivo tutti i modelli predefiniti di default presenti sul database universitario.

- Predizione della posizione tramite modelli di Machine Learning: il tab 'Predizione della posizione' applica tun algoritmo di regressione lineare multivariabile per prevedere la posizione (latitudine e longitudine) dell'utente in base ai dati raccolti dal GPS. L'uso di modelli di regressione lineare consente una stima accurata della posizione.
- Nella pagina Prediction, non solo vi è il risultato sia in forma testuale che visiva sulla mappa di OpenStreetMap, ma vi è anche una bussola (funzionante in ogni orientamento del dispositivo), che permette all'utente di orientarsi nella direzione in cui si trova la posizione predetta.
- Per la bussola vi è anche all'apertura, un messaggio che mostra che tipo di movimento fare per calibrare al meglio i sensori in modo da avere una bussola più precisa.

- Visualizzazione su mappa: Essendo l'applicazione indipendente da servizi a pagamento (come Google Maps), l'utente può visualizzare la posizione prevista su una mappa interattiva di OpenStreetMap, direttamente all'interno dell'applicazione.

- Interfaccia utente intuitiva: l'interfaccia dell'applicazione è stata progettata con l'utente in mente, assicurando che le funzionalità siano facilmente accessibili e comprensibili, indipendentemente dal livello di familiarità con il Machine Learning.

## Installazione 🐙

Ci sono 2 opzioni per l'installazione:

1. Clonare la repository.
2. Nella cartella "Download", c'è l'apk per installare direttamente l'app sul tuo dispositivo Android e avviarla immediatamente.

## Utilizzo 💡

Ecco una lista di screenshot per una migliore comprensione del funzionamento dell'applicazione:

  <a href="#">
  	<img src="https://raw.githubusercontent.com/lbabbu/Application-Logo-App-LOL/main/foto%20finali%20app%20LOL/pagina%20scan.png" alt="App" height="700" />
    <img src="https://raw.githubusercontent.com/lbabbu/Application-Logo-App-LOL/main/foto%20finali%20app%20LOL/menu%20a%20tendina%20pagina%20scan.png" alt="App" height="700" />
    <img src="https://raw.githubusercontent.com/lbabbu/Application-Logo-App-LOL/main/foto%20finali%20app%20LOL/pagina%20lista%20modelli.png" alt="App" height="700" />
    <img src="https://raw.githubusercontent.com/lbabbu/Application-Logo-App-LOL/main/foto%20finali%20app%20LOL/pagina%20prediction.png" alt="App" height="700" />
    <img src="https://raw.githubusercontent.com/lbabbu/Application-Logo-App-LOL/main/foto%20finali%20app%20LOL/tab%20trilaterazione.png" alt="App" height="700" />
  </a>

## Permessi richiesti all'utente

Ecco l'elenco delle permissions richieste all'utente:

- ACCESS_NETWORK_STATE: Permette all'app di accedere alle informazioni sullo stato della rete, come ad esempio la disponibilità e il tipo di connessione (WiFi, mobile, nessuna connessione).

- INTERNET: Permette all'app di accedere a Internet per poter effettuare richieste verso server esterni o scaricare dati.

- ACCESS_WIFI_STATE: Permette all'app di accedere alle informazioni sullo stato del Wi-Fi, come ad esempio se il Wi-Fi è abilitato e il nome della rete Wi-Fi connessa.

- CHANGE_WIFI_STATE: Permette all'app di cambiare lo stato del Wi-Fi, ad esempio abilitandolo o disabilitandolo.

- ACCESS_FINE_LOCATION: Permette all'app di accedere alla posizione precisa dell'utente con una precisione di livello strada. Questo richiede un consenso esplicito dell'utente.

- ACCESS_COARSE_LOCATION: Permette all'app di accedere alla posizione approssimativa dell'utente senza una precisione di livello strada. Anche in questo caso, è necessario il consenso dell'utente.

- READ_PHONE_STATE: Permette all'app di accedere allo stato del telefono, come ad esempio il numero IMEI e l'operatore di rete. Nota che l'accesso a questo permesso è diventato più restrittivo nelle versioni recenti di Android.

- READ_EXTERNAL_STORAGE: Permette all'app di leggere dati dallo storage esterno dell'utente, come ad esempio le immagini o altri file. Si noti che è stata specificata una versione massima di SDK (32), il che significa che il permesso sarà valido solo fino a quella versione di Android.


## Documentazione 📄

Ecco l'elenco dei metodi e di alcune API utilizzate nel codice:

### Metodi

- `calculateEstimatedDistanceToCellTower()`: Questo metodo calcola la distanza stimata fino a una torre cellulare in base alla potenza del segnale RSSI.
- `calculateEstimatedDistance()`: Questo metodo calcola la distanza stimata fino a un punto di accesso WiFi in base alla potenza del segnale RSSI.
- `latLonToCartesian()`: Questo metodo converte le coordinate di latitudine e longitudine in coordinate cartesiane.
- `cartesianToLatLon()`: Questo metodo converte le coordinate cartesiane in coordinate di latitudine e longitudine.
- `updateButtonVisibility()`: Aggiorna la visibilità dei pulsanti in base allo stato corrente della scansione.
- `onResume()`: Richiamato quando la vista del fragment sta per diventare visibile. Questo metodo gestisce il ricaricamento della mappa e del tracker della posizione GPS.
- `onAccuracyChanged(Sensor sensor, int accuracy)`: Chiamato quando cambia l'accuratezza di un sensore. Non esegue alcuna azione specifica nel codice fornito.
- `onSensorChanged(SensorEvent event)`: Chiamato quando i dati del sensore cambiano. Aggiorna i dati dell'oggetto dataRow con i valori dei sensori.
- `showInputDialog()`: Mostra una finestra di dialogo per consentire all'utente di inserire un nome per il dataset.
- `continueOnClick(String userInput)`: Gestisce l'azione di continuare dopo che l'utente ha inserito un nome per il dataset.
- `saveToFile()`: Salva i dati nell'oggetto dataRow su un file CSV se writeData è impostato su true.
- `saveSensorDataToCSV()`: Salva i dati dell'oggetto dataRow su un file CSV, aggiungendo i dati al file esistente se già presente.

### API

- `TelephonyManager`: Questa classe fornisce accesso alle informazioni sui servizi di telefonia del dispositivo.
- `WifiManager`: Questa classe fornisce accesso alle informazioni sui servizi WiFi del dispositivo.
- `LocationManager`: Questa classe fornisce accesso ai servizi di localizzazione.
- `android.location.jar`: Questa libreria fornisce l'API per accedere ai servizi di localizzazione di Android, come l'accesso alla posizione GPS e ad altre fonti di localizzazione.
- `com.google.android.gms:play-services-location:18.0.0`: Questa libreria fornisce l'API per l'accesso ai servizi di localizzazione di Google Play Services, come la geolocalizzazione basata su WiFi e celle.
- `com.google.android.gms:play-services-maps:18.1.0`: Questa libreria fornisce l'API per l'accesso ai servizi di mappe di Google Play Services, consentendo di utilizzare funzionalità avanzate di mappa come visualizzazione di mappe, posizionamento dei marcatori e calcolo di percorsi.

### Librerie

- `android.jar`: Questa è la libreria Android base.
- `android.net.jar`: Questa libreria fornisce accesso ai servizi di rete.
- `androidx.appcompat:appcompat:1.6.1`: Supporta funzionalità aggiuntive per versioni precedenti di Android.
- `com.google.android.material:material:1.5.0`: Fornisce componenti Material Design per un'interfaccia utente moderna.
- `com.google.code.gson:gson:2.8.6`: Libreria per la conversione di oggetti Java in formato JSON e viceversa.
- `androidx.constraintlayout:constraintlayout:2.1.4`: Gestisce il layout delle viste in modo responsivo e flessibile.
- `androidx.navigation:navigation-fragment:2.6.0`: Componente di navigazione per la gestione dei flussi di navigazione nell'app.
- `androidx.navigation:navigation-ui:2.6.0`: Componente di navigazione per l'integrazione con l'interfaccia utente.
- `junit:junit:4.13.2`: Framework per il testing unitario in Java.
- `androidx.test.ext:junit:1.1.5`: Estensioni per il framework di testing JUnit su Android.
- `androidx.test.espresso:espresso-core:3.5.1`: Framework per il testing dell'interfaccia utente su Android.
- `org.apache.commons:commons-math3:3.6.1`: Libreria per operazioni matematiche avanzate.
- `com.lemmingapex.trilateration:trilateration:1.0.2`: Libreria per calcoli di trilaterazione.
- `com.opencsv:opencsv:5.5`: Libreria per la lettura e scrittura di file CSV in Java.
- `org.osmdroid:osmdroid-geopackage:6.1.10`: Libreria per la gestione dei file di geopackage in Osmdroid.
- `org.osmdroid:osmdroid-android:6.1.10`: Libreria di mappe open-source per Android.
- `org.osmdroid:osmdroid-wms:6.1.10`: Libreria per il supporto del servizio Web Map Server (WMS) in Osmdroid.
- `org.osmdroid:osmdroid-mapsforge:6.1.10`: Libreria per il supporto del formato Mapsforge in Osmdroid.
- `org.osmdroid:osmdroid-shape:6.1.10`: Libreria per la gestione delle forme (shape) in Osmdroid.
- `androidx.preference:preference:1.1.1`: Libreria per la gestione delle preferenze nelle impostazioni dell'app.
