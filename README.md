# Valutazione candidati PHP/mySQL

I candidati sono pregati di fornire la soluzione ai quesiti che seguono, eventualmente specificando anche la sommaria spiegazione delle scelte operate.
Per rispondere, i candidati dovranno eseguire un fork del presente repository, predisporre la soluzione e avviare una pull request oltre a completare la procedura di candidatura attraverso il sito InfoJobs.

## Premessa

L'ambiente operativo del presente questionario deve essere 

Ambiente: **PHP versione 5.3**

Tipo Database: **mySQL**

Database host: **127.0.0.1**

Database username: **testUser**

Database password: **testPassword**

Database name: **candidatura**


Tabella "**clienti**" creata come di seguito:

    CREATE TABLE `clienti` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`nome` VARCHAR(64) NOT NULL,
	`indirizzo` VARCHAR(255) NOT NULL,
	`provincia` VARCHAR(2) NOT NULL,
	`partitaiva` VARCHAR(11) NOT NULL,
	PRIMARY KEY (`id`)
	) COMMENT='Questa tabella contiene i dati relativi ai clienti dell'azienda.'
	ENGINE=InnoDB;


Tabella "**fatture**" creata come di seguito:

    CREATE TABLE `fatture` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`partitaiva` VARCHAR(64) NOT NULL,
	`scadenza` DATE NOT NULL,
	`importo` DECIMAL(10,2) NOT NULL,
	`aliquotaiva` INT(100) NOT NULL,
	PRIMARY KEY (`id`)
	COMMENT='Questa tabella contiene i dati relativi alle fatture emesse per ciascun cliente aziendale'
	COLLATE='latin1_swedish_ci'
	ENGINE=InnoDB;

Inserire nel database i seguenti dati di esempio:

```
INSERT INTO `clienti` (`id`, `nome`, `indirizzo`, `provincia`, `partitaiva`) VALUES (1, 'Acme Inc', 'Via Aurelia 100', 'RM', '11111111111');
INSERT INTO `clienti` (`id`, `nome`, `indirizzo`, `provincia`, `partitaiva`) VALUES (2, 'NewCo s.p.a.', 'Via Salaria, 100', 'RM', '22222222222');
INSERT INTO `clienti` (`id`, `nome`, `indirizzo`, `provincia`, `partitaiva`) VALUES (3, 'OldCo s.p.a.', 'Via Montenapoleano, 100', 'MI', '33333333333');
INSERT INTO `clienti` (`id`, `nome`, `indirizzo`, `provincia`, `partitaiva`) VALUES (4, 'Super Co s.p.a.', 'Via della Vittoria, 100', 'TO', '44444444444');
INSERT INTO `clienti` (`id`, `nome`, `indirizzo`, `provincia`, `partitaiva`) VALUES (5, 'Ultra Co s.r.l.', 'Via Rom, 100', 'BA', '55555555555');
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (1, '11111111111', '2018-08-05', 100.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (2, '11111111111', '2018-09-05', 200.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (3, '11111111111', '2018-10-05', 800.00, 4);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (4, '22222222222', '2019-11-05', 300.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (5, '22222222222', '2017-11-05', 400.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (6, '22222222222', '2018-10-05', 600.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (7, '33333333333', '2018-11-05', 100.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (8, '33333333333', '2019-11-05', 200.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (9, '33333333333', '2017-11-05', 100.00, 22);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (10, '55555555555', '2018-11-05', 200.00, 21);
INSERT INTO `fatture` (`id`, `partitaiva`, `scadenza`, `importo`, `aliquotaiva`) VALUES (11, '55555555555', '2017-11-05', 300.00, 22);
```


### Quesito 1

Il candidato è invitato a creare un file PHP che:
* esegua la connessione al database come specificato in premessa
* estragga la lista dei clienti della provincia di RM
* generi, in HTML, una TABLE contenente i risultati estratti come sopra

### Quesito 2

Il candidato è invitato a creare un file PHP che:
* esegua la connessione al database come specificato in premessa
* estragga la somma del fatturato diviso per ciascuna provincia
* generi, in HTML, una TABLE contenente i risultati estratti come sopra

### Quesito 3

Il candidato è invitato a creare un file PHP che:
* esegua la connessione al database come specificato in premessa
* estragga il totale fatturato per ciascun cliente
* generi, in HTML, una TABLE contenente i risultati estratti come sopra

## Note finali

I candidati sono invitati a presentare le risposte utilizzando lo stile di programmazione preferito.
***Tuttavia, si prega di non utilizzare librerie esterne (come PEAR e simili).***
Grazie!
