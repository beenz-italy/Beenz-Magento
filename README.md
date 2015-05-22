# Beenz-Magento 

**Beenz-Magento** è un modulo per Magento che permette una facile integrazione con le API di [Beenz.com] (https://api.beenz.com)

* Versione: 1.0.0
* Data: 2015-05-18
* Sviluppato da: [Beenz.com](https://www.beenz.com/)
* Licenza: [MIT](http://opensource.org/licenses/MIT)
* Contact: [tech@beenz.com](mailto:tech@beenz.com)

## Sommario

**Beenz-Magento** permette una rapida integrazione con le API di [Beenz.com] (https://api.beenz.com).
In particolare sono supportate le promo di tipo ``purchase`` e ``plugin``. In questo modo l'amministratore di Magento può ricompensare i propri clienti per
 
* acquisti
* iscrizioni al sito
* recensioni
* iscrizioni alla newsletter


## Installazione

1. Scaricare il file `magento-beenz.zip`
2. Decomprimere il contenuto del file nella directory in cui è installato Magento (``$MAGENTO_DIR``)
3. Cancellare la cache di Magento (``$MAGENTO_DIR/var/cache/*``)


## Note sull'uso

### Connessione account

La prima operazione da compiere è collegare l'account Beenz con il sistema Magento. Per far questo è necessario inserire l'indirizzo email di registrazione, la password e lo shopId nell'apposito form nella sezione Beenz del pannello di configurazione di Magento.
È possibile testare la connessione e, una volta che questa è stata stabilita con successo, salvare la configurazione.
 
### Attivazione promo purchase

La connessione dell'account permette già di inoltrare le chiamate relative agli acquisti senza ulteriori configurazioni. La chiamata viene inoltrata al momento della fatturazione (*invoice*).


#### BEENZ_TAG

In qualsiasi momento è possibile corredare gli articoli a catalogo con i BEENZ_TAG dall'apposito form di configurazione dell'articolo. Si possono utilizzare più BEENZ_TAG (separandoli con la virgola ",")


#### Recesso

La chiamata per il recesso di articoli già acquistati viene inoltrata automaticamente quado l'amministratore di Magento utilizza la procedura di rimborso.


### Attivazione promo plug-in

Attualmente è possibile usare le promo plug-in in relazione alle seguenti azioni:

* iscrizioni al sito
* recensioni
* iscrizioni alla newsletter

Per ognuna di queste azioni, nel form di configurazione, è presente una coppia di righe. È necessario riempire la riga relativa con il corretto ext-id e usare il tasto per caricare il corretto promoId. Se l'operazione ha successo è possibile salvare la
configurazione relativo alla/le promo.

Le chiamate vengono inoltrate al momento in cui l'azione viene effettuata dall'utente. Fa eccezione la chiamata relativa alle recensioni che viene effettuata all'approvazione.


### coda 

**Beenz-Magento** è dotato di una coda di chiamate. Questa feature permette all'amministratore di Magento di:
 
 * monitorare lo stato delle transazioni
 * re-inoltrare chiamate fallite (a causa di temporanei problemi di rete)
 * intervenire su transazioni non inoltrate per utenti che hanno dimenticato di specificare la mail con cui sono registrati presso Beenz.com
 

## Licenza

**Beenz-Magento** è rilasciato con licenza MIT.

Vedere [LICENSE](LICENSE) file per dettagli.




