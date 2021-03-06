# [LINQ to SQL](index.md)
## [Introduzione](getting-started.md)
### [Operazioni eseguibili con LINQ to SQL](what-you-can-do-with-linq-to-sql.md)
### [Passaggi tipici per l'utilizzo di LINQ to SQL](typical-steps-for-using-linq-to-sql.md)
### [Download di database di esempio](downloading-sample-databases.md)
### [Apprendimento tramite procedure dettagliate](learning-by-walkthroughs.md)
#### [Procedura dettagliata: Modello a oggetti e query semplici (Visual Basic)](walkthrough-simple-object-model-and-query-visual-basic.md)
#### [Procedura dettagliata: eseguire query tra relazioni (Visual Basic)](walkthrough-querying-across-relationships-visual-basic.md)
#### [Procedura dettagliata: modifica dei dati (Visual Basic)](walkthrough-manipulating-data-visual-basic.md)
#### [Procedura dettagliata: utilizzo solo di stored procedure (Visual Basic)](walkthrough-using-only-stored-procedures-visual-basic.md)
#### [Procedura dettagliata: Modello a oggetti e query semplici (C#)](walkthrough-simple-object-model-and-query-csharp.md)
#### [Procedura dettagliata: eseguire query tra relazioni (C#)](walkthrough-querying-across-relationships-csharp.md)
#### [Procedura dettagliata: modifica dei dati (C#)](walkthrough-manipulating-data-csharp.md)
#### [Procedura dettagliata: utilizzo solo di stored procedure (C#)](walkthrough-using-only-stored-procedures-csharp.md)
## [Guida per programmatori](programming-guide.md)
### [Creazione del modello a oggetti](creating-the-object-model.md)
#### [Procedura: Generare il modello a oggetti in Visual Basic o C#](how-to-generate-the-object-model-in-visual-basic-or-csharp.md)
#### [Procedura: generare il modello a oggetti come file esterno](how-to-generate-the-object-model-as-an-external-file.md)
#### [Procedura: generare codice personalizzato modificando un file DBML](how-to-generate-customized-code-by-modifying-a-dbml-file.md)
#### [Procedura: convalidare file di mapping esterni e DBML](how-to-validate-dbml-and-external-mapping-files.md)
#### [Procedura: rendere serializzabili le entità](how-to-make-entities-serializable.md)
#### [Procedura: personalizzare classi di entità mediante l'Editor del codice](how-to-customize-entity-classes-by-using-the-code-editor.md)
##### [Procedura: specificare nomi di database](how-to-specify-database-names.md)
##### [Procedura: rappresentare tabelle come classi](how-to-represent-tables-as-classes.md)
##### [Procedura: rappresentare colonne come membri di classi](how-to-represent-columns-as-class-members.md)
##### [Procedura: rappresentare le chiavi primarie](how-to-represent-primary-keys.md)
##### [Procedura: eseguire il mapping di relazioni tra database](how-to-map-database-relationships.md)
##### [Procedura: rappresentare colonne come generate dal database](how-to-represent-columns-as-database-generated.md)
##### [Procedura: rappresentare colonne come timestamp o versioni](how-to-represent-columns-as-timestamp-or-version-columns.md)
##### [Procedura: specificare i tipi di dati del database](how-to-specify-database-data-types.md)
##### [Procedura: rappresentare colonne calcolate](how-to-represent-computed-columns.md)
##### [Procedura: specificare campi di archiviazione privati](how-to-specify-private-storage-fields.md)
##### [Procedura: rappresentare colonne per l'accettazione di valori Null](how-to-represent-columns-as-allowing-null-values.md)
##### [Procedura: eseguire il mapping di gerarchie di ereditarietà](how-to-map-inheritance-hierarchies.md)
##### [Procedura: specificare il controllo di conflitti di concorrenza](how-to-specify-concurrency-conflict-checking.md)
### [Comunicazione con il database](communicating-with-the-database.md)
#### [Procedura: connettersi a un database](how-to-connect-to-a-database.md)
#### [Procedura: eseguire direttamente comandi SQL](how-to-directly-execute-sql-commands.md)
#### [Procedura: riutilizzare una connessione tra un comando ADO.NET e un DataContext](how-to-reuse-a-connection-between-an-ado-net-command-and-a-datacontext.md)
### [Esecuzione di query sul database](querying-the-database.md)
#### [Procedura: eseguire una query per ottenere informazioni](how-to-query-for-information.md)
#### [Procedura: recuperare informazioni in sola lettura](how-to-retrieve-information-as-read-only.md)
#### [Procedura: controllare la quantità di dati correlati recuperata](how-to-control-how-much-related-data-is-retrieved.md)
#### [Procedura: filtrare dati correlati](how-to-filter-related-data.md)
#### [Procedura: disattivare il caricamento posticipato](how-to-turn-off-deferred-loading.md)
#### [Procedura: eseguire direttamente query SQL](how-to-directly-execute-sql-queries.md)
#### [Procedura: archiviare e riutilizzare query](how-to-store-and-reuse-queries.md)
#### [Procedura: gestire le chiavi composite nelle query](how-to-handle-composite-keys-in-queries.md)
#### [Procedura: recuperare molti oggetti contemporaneamente](how-to-retrieve-many-objects-at-once.md)
#### [Procedura: filtrare a livello di DataContext](how-to-filter-at-the-datacontext-level.md)
#### [Esempi di query](query-examples.md)
##### [Query di aggregazione](aggregate-queries.md)
###### [Restituire il valore medio da una sequenza numerica](return-the-average-value-from-a-numeric-sequence.md)
###### [Contare il numero di elementi in una sequenza](count-the-number-of-elements-in-a-sequence.md)
###### [Trovare il valore massimo in una sequenza numerica](find-the-maximum-value-in-a-numeric-sequence.md)
###### [Trovare il valore minimo in una sequenza numerica](find-the-minimum-value-in-a-numeric-sequence.md)
###### [Calcolare la somma dei valori in una sequenza numerica](compute-the-sum-of-values-in-a-numeric-sequence.md)
##### [Restituire il primo elemento di una sequenza](return-the-first-element-in-a-sequence.md)
##### [Restituire o ignorare elementi in una sequenza](return-or-skip-elements-in-a-sequence.md)
##### [Ordinare elementi in una sequenza](sort-elements-in-a-sequence.md)
##### [Raggruppare elementi in una sequenza](group-elements-in-a-sequence.md)
##### [Eliminare elementi duplicati da una sequenza](eliminate-duplicate-elements-from-a-sequence.md)
##### [Determinare se alcuni o tutti gli elementi di una sequenza soddisfano una condizione](determine-if-any-or-all-elements-in-a-sequence-satisfy-a-condition.md)
##### [Concatenare due sequenze](concatenate-two-sequences.md)
##### [Restituire la differenza dei set tra due sequenze](return-the-set-difference-between-two-sequences.md)
##### [Restituire l'intersezione tra set di due sequenze](return-the-set-intersection-of-two-sequences.md)
##### [Restituire l'unione di set di due sequenze](return-the-set-union-of-two-sequences.md)
##### [Procedura: convertire una sequenza in una matrice](convert-a-sequence-to-an-array.md)
##### [Convertire una sequenza un tipo in un elenco generico](convert-a-sequence-to-a-generic-list.md)
##### [Convertire un tipo in un IEnumerable generico](convert-a-type-to-a-generic-ienumerable.md)
##### [Formulare join e query di prodotto incrociato](formulate-joins-and-cross-product-queries.md)
##### [Formulare proiezioni](formulate-projections.md)
### [Creazione e invio di modifiche dei dati](making-and-submitting-data-changes.md)
#### [Procedura: inserire righe nel database](how-to-insert-rows-into-the-database.md)
#### [Procedura: aggiornare righe nel database](how-to-update-rows-in-the-database.md)
#### [Procedura: eliminare righe dal database](how-to-delete-rows-from-the-database.md)
#### [Procedura: inviare modifiche al database](how-to-submit-changes-to-the-database.md)
#### [Procedura: racchiudere tra parentesi quadre gli invii di dati utilizzando transazioni](how-to-bracket-data-submissions-by-using-transactions.md)
#### [Procedura: creare un database in modo dinamico](how-to-dynamically-create-a-database.md)
#### [Procedura: gestire i conflitti di modifiche](how-to-manage-change-conflicts.md)
##### [Procedura: rilevare e risolvere gli invii in conflitto](how-to-detect-and-resolve-conflicting-submissions.md)
##### [Procedura: specificare quando vengono generate eccezioni di concorrenza](how-to-specify-when-concurrency-exceptions-are-thrown.md)
##### [Procedura: specificare per quali membri viene eseguito il test dei conflitti di concorrenza](how-to-specify-which-members-are-tested-for-concurrency-conflicts.md)
##### [Procedura: recuperare informazioni sui conflitti di entità](how-to-retrieve-entity-conflict-information.md)
##### [Procedura: recuperare informazioni sui conflitti di concorrenza](how-to-retrieve-member-conflict-information.md)
##### [Procedura: risolvere i conflitti mantenendo valori di database](how-to-resolve-conflicts-by-retaining-database-values.md)
##### [Procedura: risolvere i conflitti sovrascrivendo i valori di database](how-to-resolve-conflicts-by-overwriting-database-values.md)
##### [Procedura: risolvere i conflitti mediante l'unione con valori di database](how-to-resolve-conflicts-by-merging-with-database-values.md)
### [Supporto per il debug](debugging-support.md)
#### [Procedura: visualizzare il codice SQL generato](how-to-display-generated-sql.md)
#### [Procedura: visualizzare un insieme di modifiche](how-to-display-a-changeset.md)
#### [Procedura: visualizzare comandi LINQ to SQL](how-to-display-linq-to-sql-commands.md)
#### [Risoluzione dei problemi](troubleshooting.md)
### [Informazioni di base](background-information.md)
#### [ADO.NET e LINQ to SQL](ado-net-and-linq-to-sql.md)
#### [Analisi del codice sorgente in LINQ to SQL](analyzing-linq-to-sql-source-code.md)
#### [Personalizzazione di operazioni di inserimento, aggiornamento ed eliminazione](customizing-insert-update-and-delete-operations.md)
##### [Personalizzazione di operazioni: panoramica](customizing-operations-overview.md)
##### [Operazioni di inserimento, aggiornamento ed eliminazione](insert-update-and-delete-operations.md)
##### [Responsabilità dello sviluppatore nell'override del comportamento predefinito](responsibilities-of-the-developer-in-overriding-default-behavior.md)
##### [Aggiunta di logica di business mediante metodi parziali](adding-business-logic-by-using-partial-methods.md)
#### [Data binding](data-binding.md)
#### [Supporto dell'ereditarietà](inheritance-support.md)
#### [Chiamate a metodo locali](local-method-calls.md)
#### [Applicazioni a più livelli e remote con LINQ to SQL](n-tier-and-remote-applications-with-linq-to-sql.md)
##### [Più livelli di LINQ to SQL con ASP.NET](linq-to-sql-n-tier-with-aspnet.md)
##### [Più livelli di LINQ to SQL con Servizi Web](linq-to-sql-n-tier-with-web-services.md)
##### [LINQ to SQL con applicazioni client/server strettamente accoppiate](linq-to-sql-with-tightly-coupled-client-server-applications.md)
##### [Implementazione della logica di business a più livelli](implementing-business-logic-linq-to-sql.md)
##### [Recupero di dati e operazioni CUD in applicazioni a più livelli (LINQ to SQL)](data-retrieval-and-cud-operations-in-n-tier-applications.md)
#### [Identità degli oggetti](object-identity.md)
#### [Modello a oggetti LINQ to SQL](the-linq-to-sql-object-model.md)
#### [Stati di oggetti e rilevamento di modifiche](object-states-and-change-tracking.md)
#### [Concorrenza ottimistica: panoramica](optimistic-concurrency-overview.md)
#### [Concetti relativi alle query](query-concepts.md)
##### [Query [LINQ to SQL]](linq-to-sql-queries.md)
##### [Esecuzione di query tra relazioni](querying-across-relationships.md)
##### [Esecuzione remota e locale](remote-vs-local-execution.md)
##### [Caricamento posticipato e immediato](deferred-versus-immediate-loading.md)
#### [Recupero di oggetti dalla cache di identità](retrieving-objects-from-the-identity-cache.md)
#### [Sicurezza in LINQ to SQL](security-in-linq-to-sql.md)
#### [Serializzazione](serialization.md)
#### [stored procedure](stored-procedures.md)
##### [Procedura: restituire rowset](how-to-return-rowsets.md)
##### [Procedura: utilizzare stored procedure che accettano parametri](how-to-use-stored-procedures-that-take-parameters.md)
##### [Procedura: utilizzare stored procedure mappate per più forme di risultati](how-to-use-stored-procedures-mapped-for-multiple-result-shapes.md)
##### [Procedura: utilizzare stored procedure mappate per forme di risultati sequenziali](how-to-use-stored-procedures-mapped-for-sequential-result-shapes.md)
##### [Personalizzazione di operazioni utilizzando stored procedure](customizing-operations-by-using-stored-procedures.md)
##### [Personalizzazione di operazioni utilizzando esclusivamente stored procedure](customizing-operations-by-using-stored-procedures-exclusively.md)
#### [Supporto delle transazioni](transaction-support.md)
#### [Tipi SQL-CLR non corrispondenti](sql-clr-type-mismatches.md)
#### [Mapping del tipo personalizzato SQL-CLR](sql-clr-custom-type-mappings.md)
#### [Funzioni definite dall'utente](user-defined-functions.md)
##### [Procedura: utilizzare funzioni definite dall'utente con valori scalari](how-to-use-scalar-valued-user-defined-functions.md)
##### [Procedura: utilizzare funzioni definite dall'utente con valori di tabella](how-to-use-table-valued-user-defined-functions.md)
##### [Procedura: chiamare funzioni definite dall'utente inline](how-to-call-user-defined-functions-inline.md)
## [Riferimento](reference.md)
### [Tipi di dati e funzioni](data-types-and-functions.md)
#### [Mapping del tipo SQL-CLR](sql-clr-type-mapping.md)
#### [Tipi di dati Basic](basic-data-types.md)
#### [Tipi di dati Boolean](boolean-data-types.md)
#### [Semantica Null](null-semantics.md)
#### [Operatori numerici e di confronto](numeric-and-comparison-operators.md)
#### [Operatori di sequenza](sequence-operators.md)
#### [Metodi System.Convert](system-convert-methods.md)
#### [Metodi System.DateTime](system-datetime-methods.md)
#### [Metodi System.Math](system-math-methods.md)
#### [Metodi System.Object](system-object-methods.md)
#### [Metodi System.String](system-string-methods.md)
#### [Metodi System.TimeSpan](system-timespan-methods.md)
#### [Funzionalità non supportata](unsupported-functionality.md)
#### [Metodi System.DateTimeOffset](system-datetimeoffset-methods.md)
### [Mapping basato su attributi](attribute-based-mapping.md)
### [Generazione di codice in LINQ to SQL](code-generation-in-linq-to-sql.md)
### [External Mapping](external-mapping.md) (Mapping esterno)
### [Domande frequenti](frequently-asked-questions.md)
### [SQL Server Compact e LINQ to SQL](sql-server-compact-and-linq-to-sql.md)
### [Conversione dell'operatore query standard](standard-query-operator-translation.md)
## [Esempi](samples.md)
