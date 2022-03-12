# Info

Questo repo contiene il sorgente (generato staticamente) del blog www.lamacchinadesiderante.org

## Aggiornare il blog

Ciò che viene mostrato all'url www.lamacchinadesiderante.org è il contenuto del branch `master` di questo repo. Per aggiornare il sito (in caso di inserimento contenuti, bugfix, aggiornamento del layout, ecc...) seguire la seguente procedura.

1) Questo repo è generato da un altro repo salvato solo in locale (`Repos/lamacchinadesiderante`) che contiene il sorgente di ghostjs. E' quindi necessario avere accesso a quel repo e avviare Ghost con il comando `ghost start`. All'indirizzo http://localhost:2368/ghost sarà possibile accedere al pannello di controllo di Ghost.

2) Una volta fatte le modifiche richieste, bisogna generare la versione aggiornata del sito statico. Per farlo va usato il pacchetto `ghost-static-site-generator`. 

Se il pacchetto non dovesse essere installato, basta eseguire questo comando:

`npm install -g ghost-static-site-generator`

(maggiori info su: https://github.com/Fried-Chicken/ghost-static-site-generator)

3) Per generare il sito, lanciare il seguente comando:

`gssg --ignore-absolute-paths --dest "lamacchinadesiderante_static" --preview`

dove la cartella `lamacchinadesiderante_static` corrisponde alla cartella locale in cui è contenuto il presente repo. Verrà aperta un'anteprima del sito statico nel browser.

4) Entrare nella cartella `lamacchinadesiderante_static` ed eseguire il commit e il push delle modifiche (assicurarsi di essere sul branch master). Il sito è ora aggiornato all'ultima versione.
