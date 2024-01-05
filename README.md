# blocco-appunti-fttm
Blocco appunti del plugin wp_factotum

Guida compatibile con versione 1.4d REV.2 STABLE
Download ultima versione STABLE:

WP Factotum Repository Ufficiale: https://webessence.it/factotum/pub/repo/browser/




Esempi di utilizzo in tempo reale:

https://webessence.it/factotum/




MANUALE D'USO
Sommario
Requisiti di sistema
Requisiti minimi
Requisiti consigliati
Installazione
Nuova installazione di Factotum da zero
Aggiornamento del plugin già esistente
Configurazione
Shortcodes
Uso proprio
Uso improprio
Esempi
Criticità e problematiche note




Requisiti di sistema
Requisiti minimi

Per funzionare correttamente, WP Factotum ha bisogno di un ambiente con che rispetti i seguenti requisiti di base (come minimo):

Server Linux-based
Apache 2.0 o superiore
PHP 5.6 o superiore
MySQL 7.0 o superiore
Wordpress 4.0 o superiore
Configurazione di Wordpress "Vanilla" senza modifiche al Core-code
API Key SerpWow a pagamento
API Key Google Maps senza restrizioni
Client abilitato JavaScript
Plugin esterni:
Advanced Custom Fields PRO
Custom Post Type UI
SEOPress
Internal Link Juicer
Requisiti consigliati

Per funzionare ancora meglio e in maniera stabile, WP Factotum va preferibilmente installato in un ambiente che rispetti i seguenti requisiti ideali (raccomandati):

Server Linux-based (CentOS, CloudLinux raccomandati)
EasyApache 4 o superiore
PHP 7.2 o superiore
MySQL 8.0 o superiore (MariaDB 10.5 o superiore raccomandato)
Wordpress 5.7 o superiore
Configurazione di Wordpress "Vanilla" senza modifiche al Core-code e senza altri plugin oltre a quelli nella lista che segue
API Key SerpWow a pagamento (pacchetto mensile con auto-rinnovo raccomandato)
API Key Google Maps senza restrizioni
Client abilitato JavaScript (Chrome, Edge, Yandex Browser raccomandati)
Plugin esterni:
Advanced Custom Fields versione PRO
Custom Post Type UI
SEOPress
Internal Link Juicer
Redirection
Advanced Random Posts Widget




Installazione
Prima / nuova installazione
Scaricare il "FULL-PACKAGE" dal repository
Estrarre il contenuto di "factotum_pack.zip" in una cartella temporanea
Caricare il file "factotum.zip" in Wordpress -> Bacheca -> Plugin -> Aggiungi nuovo -> Carica plugin per procedere con l'installazione e attivazione di Factotum
Installare le dipendenze necessarie (per vedere quali mancano, attivare il plugin e andare su "WP-Factotum" nella barra laterale)
Custom Post Type settings: utilizzare il file "cpt_ui_settings.txt" che si trova nella cartella "imports" (dalla temporanea estratta nel punto 2) per caricare e importare le impostazioni del plugin di terze parti (bisognerà aprirlo e copiare/incollare il contenuto nell'apposita sezione "Import" del plugin)
Advanced Custom Fields: utilizzare il file "FREE-acf-export-2021-04-10.json" che si trova nella cartella "imports" (dalla temporanea estratta nel punto 2) per caricare e importare le impostazioni del plugin di terze parti
FATTO! Puoi ora andare su "Factotum" dalla barra laterale del backend Wordpress per iniziare ad impostare i tuoi settings, è vivamente consigliato passare per di qui PRIMA di effettuare qualsiasi operazione!
Aggiornamento / Sostituzione del plugin
Scaricare l'ultima versione dal repository (riquadri posti in basso)
Caricare il file "factotum.zip" in Wordpress -> Bacheca -> Plugin -> Aggiungi nuovo -> Carica plugin per procedere con l'installazione e attivazione di Factotum
Wordpress a questo punto dovrebbe chiedere conferma per sostituire o aggiornare il plugin, basterà quindi dare l'ok per continuare e attivare la nuova versione
FATTO! Puoi ora andare su "Factotum" dalla barra laterale del backend Wordpress per iniziare ad impostare i tuoi settings, è vivamente consigliato passare per di qui PRIMA di effettuare qualsiasi operazione!
Shortcodes
Guida all'uso corretto degli shortcode
*NEW* Shortcode [fttm_tableprice]
Esempi prova
https://www.webessence.it/factotum/


Funzioni attuali shortcode
Lo shortcode completo di tutti i suoi attributi risulta nel seguente:
[fttm_tableprice price="{value}" range="{value}" rows="{riga,[riga],[...]}"]


Info valori attributi
price = valore intero che determina il prezzo di riferimento (medio)
range = valore intero che determina il valore "delta" da addizionare/sottrarre dal valore "price" per ottenere le variabili assegnate alle altre righe
rows = nomi delle righe, separati da virgola: questo campo determina sia quante righe dovranno essere stampate nella tabella, che quali nomi assegnare ad ognuna di esse dall'alto verso il basso


*NEW* Shortcode [fttm_link]
Esempi prova
https://www.webessence.it/factotum/


Funzioni attuali shortcode
Lo shortcode completo di tutti i suoi attributi risulta nel seguente:
[fttm_link content="{keyword}" class="{custom_class1 [custom_class2] [...]}" title="{text}" source="{domain_name}" type="{type}" site="{domain_name}" target="{_self|_blank}"]


Info valori attributi
content = parola chiave da ricercare su Google, da cui viene poi restituita la lista di links
class = (opzionale) specificare una o più classi separate da uno spazio, proprio come si fa solitamente in un inline tag HTML (escludere quindi il "." punto prima della classe, non è un CSS!)
title = (opzionale) specificare un title da assegnare al tag <a>
source = (opzionale) specificare una sorgente del link, se utilizzato factotum provvede a selezionare SOLO il link proveniente da questa sorgente (es. "wikihow"); nel caso questa sorgente non venga trovata, verrà restituito il 1° link disponibile)
type = (opzionale) di default omesso, se utilizzato occorre specificare uno dei seguenti tipi di funzione:
type="site": effettua una chiamata a Google aggiungendo il parametro "site:example.com" così da ottenere SOLO i risultati inerenti ad un sito specifico, e' necessario usarlo in combinazione con il parametro "site" (all'interno del quale va specificato poi il dominio/sito da richiamare)
site = (opzionale) questo parametro va utilizzato sempre e SOLO in combinazione con il parametro "type" (il quale va settato su "site"), specificare quindi il nome a dominio o sito inclusivo del prefisso www. che andrà elaborato dallo shortcode (es. site="www.imprendo.org")
target = (opzionale) utilizzare questo parametro per decretare se aprire o meno il link in una nuova scheda (supporta qualsiasi direttiva conforme alle regole HTML5 del congresso W3C), di default il link si apre nella stessa scheda


Shortcode [fttm_spintext]
Esempi prova
https://www.webessence.it/factotum/


Funzioni attuali shortcode
Lo shortcode completo di tutti i suoi attributi risulta nel seguente:
[fttm_spintext]{contenuto}[/fttm_spintext]


Info valori contenuto
all'interno dello shortcode è opportuno inserire il contenuto spinnabile con variabili definite da dizionario che segue


Dizionario variabili
{site_url} : URL / Indirizzo Web del blog / sito
{site_name} : Nome del blog / sito

Operatori disponibili

OR = è possibile utilizzare l'operatore matematico OR (oppure) tramite il simbolo " | " che delinea 2 o più variabili / testi da cui effettuare una selezione casuale (es. [fttm_spintext]{site_url|site_name|Testo normale non variabilizzato}[/fttm_spintext])




Shortcode [fttm_image] / [fttm_images] / [fttm_gallery]
Esempi prova
https://www.webessence.it/factotum/


Funzioni attuali shortcode
Lo shortcode completo di tutti i suoi attributi risulta nel seguente:
[fttm_image content="{keyword,[keyword],[...]}" title="{testo}" size="{WP-size}|{width,height}" featured="{0|1|2}"]


la stessa formula qui sopra può essere utilizzata con l'attributo [fttm_images] o [fttm_gallery] che corrispondono allo stesso identico shortcode ma possono aiutare all'occhio dell'editore in quanto indicano l'utilizzo di più immagini e quindi la formazione di una galleria WP


Info valori attributi
content = valore testuale che indica la keyword da ricercare per il download di immagine da Google
title = inserire la didascalia che compare alle persone cieche (audio-lettura) o alla sosta del mouse sopra l'immagine
size = inserire le dimensioni immagine, in uno di questi due formati:
WP-size: le dimensioni default di Wordpress ossia "thumbnail", "medium", "large"
Width&Height: le solite dimensioni in numeri interi; è possibile inserire un numero intero con o senza il suffisso "px"; è possibile assegnare una (soltanto una) delle due dimensioni ad elaborazione automatica rispetto all'altra inserendo il valore "0" ad esempio 0x150 renderà width automaticamente calcolata in base alla height di 150 ed esempio in viceversa; assegnando un solo parametro e omettendo quindi la separazione tramite virgola (,) o tramite x (minusc. o maiusc.), il valore verrà automaticamente assegnato sottoforma di classe CSS permettendo quindi l'assegnazione di regole custom.css
featured = il solito parametro vero/falso che determina se l'immagine verrà messa in evidenza o meno indicato tramite valori interi "0" per falso o "1" per vero (in evidenza), più un valore "2" che imposta SOLO l'immagine in evidenza rimuovendola quindi dal contenuto del post; il parametro può essere omesso e di default è "0";


Shortcode [fttm_makeimage]
Esempi prova
https://www.webessence.it/factotum/


Funzioni attuali shortcode
Lo shortcode completo di tutti i suoi attributi risulta nel seguente:
[fttm_makeimage content="{keyword}" src="{url}" title="{testo}" size="{WP-size}|{width,height}" text="{testo}" font-size="{font-size}" font-color="{r,g,b}" font-pos="{x,y}" font-angle="{rotazione}" featured="{0|1|2}"]

Info valori attributi
src = inserire la URL completa di "http(s)://" in riferimento all'immagine da utilizzare
content = valore testuale che indica la keyword da ricercare per il download di immagine da Google; il parametro può essere omesso o utilizzato insieme a 'src', in quest'ultimo caso verrà data priorità a 'content' ma nel caso in cui fallisse per qualsiasi ragione il parametro 'src' verrà utilizzato come fallback (immagine alternativa);
title = inserire la didascalia che compare alle persone cieche (audio-lettura) o alla sosta del mouse sopra l'immagine
size = inserire le dimensioni immagine, in uno di questi due formati:
WP-size: le dimensioni default di Wordpress ossia "thumbnail", "medium", "large"
Width&Height: le solite dimensioni in numeri interi; è possibile inserire un numero intero con o senza il suffisso "px"; è possibile assegnare una (soltanto una) delle due dimensioni ad elaborazione automatica rispetto all'altra inserendo il valore "0" ad esempio 0x150 renderà width automaticamente calcolata in base alla height di 150 ed esempio in viceversa; assegnando un solo parametro e omettendo quindi la separazione tramite virgola (,) o tramite x (minusc. o maiusc.), il valore verrà automaticamente assegnato sottoforma di classe CSS permettendo quindi l'assegnazione di regole custom.css
text = valore testuale dell'etichetta che verrà sovrapposta all'immagine; è possibile utilizzare caratteri speciali come "\n" per dare "a capo"; in futuro saranno possibili maggiori manipolazioni stile html o bbcode nonché la formattazione (es. text-align)
font-size = dimensioni font in numero intero senza il suffisso (valore solo numerico); viene applicato il calcolo in "punti" (pt) come avviene in Photoshop o in CSS; il parametro può essere omesso e di default è "10" (punti);
font-color = questo valore corrisponde alla colorazione del testo e per ora è possibile soltanto assegnare valori RGB e quindi in combinazioni di rosso, verde e blu separati da una virgola (es. 255,255,255 produrra il bianco mentre 255,0,0 produrra il rosso); il parametro può essere omesso e di default è "0,0,0" (nero);
font-pos = valore che specifica dove va posizionato il testo rispetto all'immagine; il parametro può essere omesso e di default è "0,0"; accetta due tipi di valori:
Testuale: viene specificata una dimensione generica tramite i valori predefiniti "center", "top", "left", "bottom", "right" validi sia per asse X che per asse Y; è possibile omettere uno di questi due valori X e Y solo per la specifica "center" in quanto viene così impartito l'ordine di centrare entrambi gli assi a metà; non c'é un vero e proprio ordine di scrittura quindi è possibile inserire i valori in combinazione X, Y come anche al contrario Y,X (es. "top,center" e "center,top" danno lo stesso risultato)
Numerico: viene specificata una dimensione precisa in numeri interi per i valori X e Y che ne rappresentano gli assi; non è possibile in questo caso invertire l'ordine degli assi, pertanto il primo valore è sempre X e il secondo è Y (es. "100,150" e "150,100" definiscono sempre il primo valore come orizzontalmente posizionato su asse X e il secondo valore per l'asse verticale Y); non bisogna inserire alcun suffisso (es. "px") ma bensì numeri interi che verranno automaticamente interpretati come valori in pixel
font-angle = valore numerico intero che va da 0 a 360 gradi ed indica appunto la rotazione bidimensionale di trasformazione della scritta; il parametro può essere omesso e di default è "0"; non bisogna inserire alcun suffisso (es. " ° " o "gradi") ma bensì un numero intero che verrà automaticamente interpretato come valore in gradi
featured = il solito parametro vero/falso che determina se l'immagine verrà messa in evidenza o meno indicato tramite valori interi "0" per falso o "1" per vero (in evidenza), più un valore "2" che imposta SOLO l'immagine in evidenza rimuovendola quindi dal contenuto del post; il parametro può essere omesso e di default è "0";


Codici esempio di utilizzo

[fttm_makeimage content="mosca nera" title="ciao" size="medium" text="prova test\nlorem ipsum\nprova 1" font-size="24" font-color="255,255,255" font-pos="center,center"]

[fttm_makeimage src="http://www.webessence.it/factotum/wp-content/uploads/2020/02/mosca-nera.jpg" title="ciao" size="medium" text="prova test\nprova 2" font-size="24" font-color="255,255,255" font-pos="center,center"]

[fttm_makeimage content="mosca nera" src="http://www.webessence.it/factotum/wp-content/uploads/2020/02/mosca-nera.jpg" title="ciao" size="medium" text="prova test\nprova 3" font-size="24" font-color="255,255,255" font-pos="center,center"]

[fttm_makeimage content="^" src="http://www.webessence.it/factotum/wp-content/uploads/2020/02/mosca-nera.jpg" title="ciao" size="medium" text="prova test\nprova 4" font-size="24" font-color="255,255,255" font-pos="center,center"]

Come si può notare il primo shortcode ricerca l'immagine "mosca nera", qualora fosse già nel db prende quella altrimenti ne scarica una nuova tramite api. A questo punto si passa al secondo controllo, nel caso in cui fosse già presente l'immagine testualizzata "mosca-nera" l'algoritmo eviterà di ripetersi e provvederà quindi ad usare quella già presente in db, altrimenti procede con le funzioni di testo e salva una nuova immagine testualizzata.

Nel secondo shortcode invece c'é il solito parametro "src" che già conosci, quindi fa lo stesso descritto nel primo shortcode, solo che al posto dell'api search implementa un download via url (da verificare se funzionante http -> https e viceversa), anche qui con tutti gli opportuni e doverosi controlli "già presente in db?".

Nel terzo esempio abbiamo invece sia "content" che "src". In questo specifico caso src non verrà neanche preso in considerazione dall'algoritmo in quanto content contiene già una keyword funzionante e che non dà errori. Tuttavia, nel caso ci fossero errori di altro genere, ad esempio la quota massima di chiamate api viene raggiunta, l'algoritmo provvederà ad utilizzare il metodo classico via url tramite il parametro "src" (ecco perché la chiamo procedura di "fallback").

Nel quarto esempio provoco io stesso un errore api per dimostrare il comportamento del terzo esempio. Qui infatti "content" passa di proposito un parametro errato in quanto si tratta di un simbolo (^) ed è soltanto un carattere, quindi l'api non effettua la ricerca immagine. Ecco che entra in scena quindi il parametro "src" che proprio per casi come questo, provvede a fornire una immagine alternativa. In questo specifico caso "mosca-nera" era già presente nel db, motivo per cui utilizza una immagine vecchia già scaricata al tempo per fare poi la sovrapposizione testuale.




Shortcode [fttm_place] / [fttm_places]
Esempi prova
https://www.webessence.it/factotum/


Funzioni attuali shortcode
Lo shortcode completo di tutti i suoi attributi risulta nel seguente:
[fttm_place content="{keyword}" image="" coords="{latitudine,longitudine}" zoom="{livello}" region="" city="{luogo}" parent="{luogo}" phone="" max="{risultati}" size="{WP-size}|{width,height}" fallback="{false|true}" no_cache="{false|true}" publish="{Y-m-d H:i:s}"]


la stessa formula qui sopra può essere utilizzata con l'attributo [fttm_places] che corrisponde allo stesso identico shortcode e può essere utile all'editore nel caso in cui dimenticasse o fosse insicuro su quale forma utilizzare


NOTA BENE: gli attributi "content" e "city" in combinazione determinano le chiavi univoche durante il salvataggio in DB, questo vuol dire che è possibile memorizzare soltanto UNA volta la query indicata per tali coordinate; la città o il luogo è l'unica correlazione diretta con la keyword, le coordinate serviranno soltanto a scopo di visualizzazione della mappa e centramento dei risultati (es. supponiamo di aver cercato "fabbro a roma" riempendo gli attributi keyword e city rispettivamente con "fabbro" e "roma"; aldilà delle coordinate impartite, i risultati presi da Google Places verranno salvati in DB sulla riga "fabbro a roma" e nelle query successive per la stessa combinazione lo shortcode sfrutterà i risultati già in cache, cambiando il parametro city si forzerà un nuovo salvataggio su luogo differente, pertanto sarà possibile memorizzare altri risultati per fabbro a seconda dei quartieri o zone specifiche come per esempio "fabbro a roma centro" o "fabbro a roma nomentana" produrranno due query differenti e quindi due nuove righe in DB memorizzate distintamente da "fabbro a roma")

Info valori attributi
content = valore testuale che indica la keyword da ricercare in associazione al luogo indicato (la query a google place sarà quindi composta da questo attributo+attributo 'city');
*NEW* image = inserire la URL completa di "http(s)://" in riferimento all'immagine da utilizzare per ogni snippet (univoca); il parametro è obbligatorio, se omesso risulterà vuoto di default e genererà quindi un errore fatale sugli snippet; questo parametro viene utilizzato nella creazione degli snippet;
coords = inserire le coordinate in formato latitudine,longitudine per proiettare correttamente la mappa nel luogo indicato; se omesso verrà puntato di default su roma (41.909986,12.3959136); è possibile andare su Google Maps ed effettuare la ricerca manualmente per poi ottenere già all'interno della barra URL in alto sia le coordinate che il valore zoom desiderato (attenzione ad assicurarvi che la barra laterale sinistra sia chiusa prima di effettuare il corretto puntamento della visuale maps);
zoom = inserire il livello di zoom desiderato; se omesso verrà impostato a 11 (valore che solitamente contiene una città grande come Roma dentro in riquadro mappa in modo decente); è possibile andare su Google Maps ed effettuare la ricerca manualmente per poi ottenere già all'interno della barra URL in alto sia le coordinate che il valore zoom desiderato (attenzione ad assicurarvi che la barra laterale sinistra sia chiusa prima di effettuare il corretto puntamento della visuale maps);
*NEW* region = inserire il nome della regione, nazione o provincia; il parametro è obbligatorio, se omesso verrà impostato di default su "lazio"; questo parametro viene utilizzato nella creazione degli snippet;
city = inserire il nome della città, quartiere, zona o altro tipo di luogo (es. monumento, parco, luogo di interesse, stazione, fermata, ecc.); il parametro è ovviamente obbligatorio, tuttavia se omesso verrà impostato di default su "roma"; questo parametro determina l'univocità della query e dei risultati, perciò prestare molta attenzione alle note descritte in alto (NOTA BENE);
*NEW* parent = inserire il nome della città, quartiere, zona o altro tipo di luogo (es. monumento, parco, luogo di interesse, stazione, fermata, ecc.) CHE FA DA GENITORE; il parametro è opzionale, serve a creare l'esplosione di link interni tra place del comune e delle sue provincie o comuni limitrofi, se omesso non viene considerato;
*NEW* phone= inserire il numero di telefono possibilmente nel formato "codice internazionale + numero" (e.g. +393313270724) in riferimento al telefono di fallback da utilizzare nel caso questo dato fosse assente in alcuni degli snippet; il parametro è obbligatorio, se omesso verrà impostato di default su "+390694802342"; questo parametro viene utilizzato nella creazione degli snippet;
*NEW* slug_cat= inserire lo slug completo della Categoria madre; il parametro è facoltativo, se omesso verrà generato automaticamente da Wordpress in base al post-title;
max = valore che indica il massimo di risultati che Google Places dovrà fornire; a causa delle politiche Google, questo valore numerico in ogni caso non può mai essere maggiore di "100" e non è detto che Google onori questa richiesta ma di consueto i risultati forniti sono comunque una 20ina; il parametro può essere omesso e in tal caso il valore default è "10";
size = inserire le dimensioni mappa, nel formato che segue:
Width&Height: le solite dimensioni in numeri interi; è possibile inserire un numero intero con o senza il suffisso "px"; è possibile assegnare una (soltanto una) delle due dimensioni ad elaborazione automatica rispetto all'altra inserendo il valore "0" ad esempio 0x150 renderà width automaticamente calcolata in base alla height di 150 ed esempio in viceversa; assegnando un solo parametro e omettendo quindi la separazione tramite virgola (,) o tramite x (minusc. o maiusc.), il valore verrà automaticamente assegnato sottoforma di classe CSS permettendo quindi l'assegnazione di regole custom.css
fallback = WORK IN PROGRESS (questo parametro indicherà allo shortcode cosa fare se i risultati non vengono forniti)
no_cache = WORK IN PROGRESS (questo parametro indicherà allo shortcode se sfruttare o meno i risultati già presenti in DB)
publish = questo valore corrisponde alla data e ora di pubblicazione degli articoli dei vari risultati place ottenuti e può essere quindi utilizzato per programmare la pubblicazione futura degli stessi o impostare una data / ora specifica; il formato DEVE essere indicato secondo le specifiche php DATE Y-m-d H:i:s che in parole povere significa "AAAA-MM-DD OO🇲🇲SS" dove 'AAAA' è l'anno esteso, 'MM' è il mese esteso (con suffisso 0 fino al 9° mese), 'DD' è il giorno esteso ( con suffisso 0 fino al 9° giorno), 'OO' è l'ora estesa (formato h24 con suffisso 0 fino alla 9° ora), 'mm' sono i minuti estesi (con suffisso 0 fino al 9° secondo), 'SS' sono i secondi estesi (con suffisso 0 fino al 9° secondo) e tutti i trattini / spazi vengono preservati (es. '2020-07-22 10:40:12'); se omesso verrà utilizzata la funzione di Wordpress che prende la data e ora corrente; si consiglia sempre di utilizzare una data più "umana" possibile e quindi evitare l'uso di orari puntuali allo 00:00 così da non lasciar intendere a Google che vi sia stata una generazione automatizzata;
*NEW* custom_type= inserire lo slug completo del Custom Post Type creato in CPT-UI; se esiste Factotum provvede ad inserire tutte le generazioni inerenti SOLO a questo shortcode nel CPT indicato, altrimenti restituisce errore sul frontend; di default è vuoto e viene quindi utilizzato il post_type "post" standard di Wordpress;


Codici esempio di utilizzo

[fttm_place content="fabbro" coords="41.8908207,12.4954534" city="roma" size="auto,500"]

[fttm_place content="investigatori" coords="42.0793951,12.4035167" zoom="13" city="formello" size="auto,300" max="8" publish="2020-11-05 09:07:14"]

Come si può notare il primo shortcode ricerca una 20ina di fabbri a Roma, con le coordinate che puntano sul centro di roma e uno zoom default che permette di visualizzare la capitale per intero su più o meno tutti i dispositivi avendo un canvas in larghezza libera e alto 400pixel.

Nel secondo shortcode invece andiamo a cercare idraulico vicino alla stazione termini (sempre con una 20ina di risultati di ritorno).

Nel terzo esempio abbiamo invece tutti i parametri possibili per una query di "investigatori a formello", con coordinate che puntano sul paese e uno zoom di 13 visto che formello non è molto grande questo valore dovrebbe permettere di visualizzarlo correttamente nel canvas mappa, abbiamo anche una altezza minore (300px) lasciando però la larghezza su auto onde evitare che il riquadro con la lista investigatori vada a coprire del tutto la città nella mappa, abbiamo anche chiesto gentilmente a Google di limitare i risultati a 8 sperando mantenga tale promessa e per finire abbiamo deciso di rendere gli articoli generati pubblici soltanto il 5 Novembre 2020 alle ore 9 circa (anche se il post con la mappa generale verrà pubblicato sin da subito).




*NEW* Shortcode [fttm_place_list]

Esempi prova
https://www.webessence.it/factotum/




Funzioni attuali shortcode

Lo shortcode ha tre diverse funzioni, elencate a seguire:

Filtra per TUTTI i risultati di una determinata keyword, restituisce come output una lista di tutti i parent con i relativi figli sottoforma di <ul><li><a><ul><li><a>:
[fttm_place_list content="{keyword}" filter="all"]
Risultato ESEMPIO <html>:
<div class="fttm_place_list alignwide">
  <ul class="fttm_map_list" style="flex:1 0 20%;">
    <li>
      <h4><a href="http://www.webessence.it/factotum/disinfestazione-lazio/">Disinfestazione Lazio</a></h4>
      <ul>
        <li>
          <h5><a href="http://www.webessence.it/factotum/disinfestazioni-roma/">Disinfestazioni Roma</a></h5>
        </li>
        <li>
          <h5><a href="http://www.webessence.it/factotum/disinfestazioni-frosinone/">Disinfestazioni Frosinone</a></h5>
        </li>
        <li>
          <h5><a href="http://www.webessence.it/factotum/disinfestazioni-provincia-di-roma/">Disinfestazioni provincia di Roma</a></h5>
        </li>
      </ul>
    </li>
  </ul>
</div>
Filtra per TUTTI i risultati di una determinata keyword, restituisce come output una lista di tutti i relativi figli della regione indicata sottoforma di <ul><li><a>:
[fttm_place_list content="{keyword}" filter="region|regione|regions|regioni" region="{regione}"]
Risultato ESEMPIO <html>:
<div class="fttm_place_list alignwide">
  <ul class="fttm_map_list" style="flex:1 0 20%;">
    <li>
      <h4><a href="http://www.webessence.it/factotum/disinfestazioni-roma/">Disinfestazioni Roma</a></h4>
    </li>
    <li>
      <h4><a href="http://www.webessence.it/factotum/disinfestazioni-frosinone/">Disinfestazioni Frosinone</a></h4>
    </li>
    <li>
      <h4><a href="http://www.webessence.it/factotum/disinfestazioni-provincia-di-roma/">Disinfestazioni provincia di Roma</a></h4>
    </li>
  </ul>
</div>
Filtra per TUTTI i risultati di una determinata keyword, restituisce come output una lista del parent (città) indicato con tutti i relativi figli della città indicata sottoforma di <ul><li><a><ul><li><a>:
Risultato ESEMPIO <html>:
<div class="fttm_place_list alignwide">
  <ul class="fttm_map_list" style="flex:1 0 20%;">
    <li>
      <h4><a href="http://www.webessence.it/factotum/disinfestazioni-roma/">Disinfestazioni Roma</a></h4>
      <ul>
        <li>
          <h5><a href="http://www.webessence.it/factotum/disinfestazioni-formello/">Disinfestazioni Formello</a></h5>
        </li>
        <li>
          <h5><a href="http://www.webessence.it/factotum/disinfestazioni-campagnano-di-roma/">Disinfestazioni Campagnano di Roma</a></h5>
        </li>
        <li>
          <h5><a href="http://www.webessence.it/factotum/disinfestazioni-la-storta/">Disinfestazioni La Storta</a></h5>
        </li>
      </ul>
    </li>
  </ul>
</div>
[fttm_place_list content="{keyword}" filter="city|cities|citta" city="{citta}"]
Filtra per TUTTI i risultati di una determinata keyword, restituisce come output una lista di tutti i luoghi limitrofi/vicini (sotto lo lo stesso parent) sottoforma di <ul><li><a>:
[fttm_place_list content="{keyword}" filter="rels|limitrofi" parent="{luogo}"]
Risultato ESEMPIO <html>:
<div class="alignwide">
  <h3>Comuni vicini:</h3>
</div>
<div class="fttm_place_list alignwide">
  <ul class="fttm_map_list" style="flex:1 0 20%;">
    <li>
      <h4><a href="http://www.webessence.it/factotum/disinfestazioni-formello/">Disinfestazioni Formello</a></h4>
    </li>
    <li>
      <h4><a href="http://www.webessence.it/factotum/disinfestazioni-la-storta/">Disinfestazioni La Storta</a></h4>
    </li>
  </ul>
</div>




le formule vanno utilizzate in combinazione con lo shortcode [fttm_place], ma possono essere disposte anche in solitaria, l'importante è che vi siano dei risultati già presenti nel database o questo shortcode produrrà "Nessun risultato" come risposta

solitamente la prima formula può essere usata in solitaria senza il tag [fttm_place], a patto che l'alberatura sia già presente nel DB e che quindi vi siano altre pagine contenenti il tag [fttm_place] con la stessa keyword richiesta




NOTA BENE: l'attributo "filter" è sempre obbligatorio, qualora fosse assente, non specificato o settato male verrà utilizzata la prima formula "all" come default, inoltre gli attributi addizionali "region", "city" e "parent" vanno usati SOLO ed ESCLUSIVAMENTE in combinazione con un determinato filtro, perciò se il filtro viene impostato su "region" sarà necessario includere anche il parametro "region" che indicherà quale regione utilizzare per il filtraggio, e così via per i parametri restanti

Info valori attributi

content= valore testuale che indica la keyword da ricercare in associazione al luogo indicato;

filter= scegliere un filtro tra i disponibili:

all = questo filtro non ha bisogno di altri attributi shortcode aggiuntivi, oltre all'attributo obbligatorio "content"; lancia una query al database per la keyword indicata nell'attributo "content" ottenendo TUTTI i risultati per TUTTI gli articoli che sono associati alla keyword indicata, con una recursive search ulteriore per tutti la gerarchia che ne consegue (esempio: [fttm_place_list content="disinfestazioni" filter="all"] genererà una query mysql unica e inline che andrà a prendere tutti gli articoli genitori e relativi figli che risultano associati alla keyword "disinfestazioni", nel caso di un'alberatura per regioni e città il risultato sarà quindi comprensivo di questi ultimi)
region = questo filtro ha bisogno dell'attributo aggiuntivo "region", oltre all'attributo obbligatorio "content"; lancia una query al database per la keyword indicata nell'attributo "content" ottenendo SOLO i risultati per gli articoli figli di {regione} (la quale verrà indicata nel successivo attributo "region") senza alcuna gerarchia (esempio: [fttm_place_list content="disinfestazioni" filter="region" region="lazio"] generà una query mysql unica e inline che andrà a prendere tutti gli articoli FIGLI del parent indicato nel;
city = 
rels =

region= inserire le coordinate in formato latitudine,longitudine per proiettare correttamente la mappa nel luogo indicato; se omesso verrà puntato di default su roma (41.909986,12.3959136); è possibile andare su Google Maps ed effettuare la ricerca manualmente per poi ottenere già all'interno della barra URL in alto sia le coordinate che il valore zoom desiderato (attenzione ad assicurarvi che la barra laterale sinistra sia chiusa prima di effettuare il corretto puntamento della visuale maps);

city= inserire il livello di zoom desiderato; se omesso verrà impostato a 11 (valore che solitamente contiene una città grande come Roma dentro in riquadro mappa in modo decente); è possibile andare su Google Maps ed effettuare la ricerca manualmente per poi ottenere già all'interno della barra URL in alto sia le coordinate che il valore zoom desiderato (attenzione ad assicurarvi che la barra laterale sinistra sia chiusa prima di effettuare il corretto puntamento della visuale maps);

parent= inserire il nome della regione, nazione o provincia; il parametro è obbligatorio, se omesso verrà impostato di default su "lazio"; questo parametro viene utilizzato nella creazione degli snippet;






Codici esempio di utilizzo

[fttm_place content="fabbro" coords="41.8908207,12.4954534" city="roma" size="auto,500"]

[fttm_place content="investigatori" coords="42.0793951,12.4035167" zoom="13" city="formello" size="auto,300" max="8" publish="2020-11-05 09:07:14"]

Come si può notare il primo shortcode ricerca una 20ina di fabbri a Roma, con le coordinate che puntano sul centro di roma e uno zoom default che permette di visualizzare la capitale per intero su più o meno tutti i dispositivi avendo un canvas in larghezza libera e alto 400pixel.

Nel secondo shortcode invece andiamo a cercare idraulico vicino alla stazione termini (sempre con una 20ina di risultati di ritorno).

Nel terzo esempio abbiamo invece tutti i parametri possibili per una query di "investigatori a formello", con coordinate che puntano sul paese e uno zoom di 13 visto che formello non è molto grande questo valore dovrebbe permettere di visualizzarlo correttamente nel canvas mappa, abbiamo anche una altezza minore (300px) lasciando però la larghezza su auto onde evitare che il riquadro con la lista investigatori vada a coprire del tutto la città nella mappa, abbiamo anche chiesto gentilmente a Google di limitare i risultati a 8 sperando mantenga tale promessa e per finire abbiamo deciso di rendere gli articoli generati pubblici soltanto il 5 Novembre 2020 alle ore 9 circa (anche se il post con la mappa generale verrà pubblicato sin da subito).




*NEW* Shortcode [fttm_review]
Esempi prova
https://www.webessence.it/factotum/


Funzioni attuali shortcode
Lo shortcode completo di tutti i suoi attributi risulta nel seguente:
[fttm_review content="{nome,[nome],[...]}" value="{valore,[valore],[...]}" price="{interi.decimali}"]


Lo shortcode crea uno snippet recensione di default impostato con schema "Product" e prezzo "0.00", i nomi e valori dei campi recensioni vengono presi dagli attributi shortcode, così come la media del punteggio.


Info valori attributi
content = nomi dei campi recensione separati da virgola
value= valore dei campi recensione separati da virgola
*NEW* price = valore univoco che indica il prezzo espresso in valori interi o con virgola/punto mobile, se omesso di default viene impostato su "0.00" e quindi non viene mostrato


Codici esempio di utilizzo

[fttm_review content="Soccorso,Stradale,Soccorso stradale,Soccorso d'alta quota" value="80,100,70,50" price="50.69"]

Come si può notare in questo shortcode esempio vengono attribuiti i seguenti campi, con i relativi valori:

Soccorso: 80
Stradale: 100
Soccorso stradale: 70
Soccorso d'alta quota: 50

NOTA BENE: E' fondamentale che la conta dei nomi campi (attributo content) sia la stessa conta dei valori campi (attributo value) !!

Inoltre viene mostrato il prezzo pari a 50.69



