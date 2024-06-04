Nella seguente repository è stata implementato il source code di matrix_multiplication.cpp il quale contiene   un insieme di test unitari scritti utilizzando la libreria Google Test
per verificare la correttezza e le prestazioni di una funzione per la moltiplicazione di matrici. 

Sono definiti cinque test distinti per verificare diversi aspetti della funzione di moltiplicazione delle matrici:

    TestMultiplyMatrices: Verifica la corretta moltiplicazione di due matrici di dimensioni differenti.
    HandlesEmptyMatrices: Controlla il comportamento della funzione quando le matrici di input sono vuote.
    Handles1x1Matrix: Testa la moltiplicazione di due matrici di dimensione 1x1;
    HandlesDifferentSizes: Verifica la moltiplicazione di due matrici 2x2 per confermare la corretta gestione delle matrici di dimensioni diverse ma compatibili.
    HandlesNegativeValues: Verifica la corretta gestione dei valori negativi all'interno delle matrici durante la moltiplicazione.
Oltre i 5 test unitari sono presenti anche uno stress test finalizzato a testare il funzionamento del codice nel caso di dimensioni di una matrice molto grandi ed un performance test che verifica
se è possibile eseguire il programma all'interno di un lasso di tempo prestabilito.

Tra le criticità nella fase di testing abbiamo trovato:
1- errori nella moltiplicazione tra matrici contenenti valori negativi.
2-problemi legati alla gestione di vettori non inizializzati, infatti i test spesso degeneravano in segmentation fault.
3- Il programma non è in grado di gestire matrici di piccole dimensioni (fallimento del test della matrice di dimensione 1) probabilmente legati a casi specificied elementari che non sono stati presi in considerazione e che non assecondano l'algoritmo convenzionale.
4-fallimentare  il test di moltiplica tra matrici vuote ( una osservazione ricorrente è legata al fatto che l'algoritmo non è in grado di gestire matrici di dimensione variabile)
5-Anche lo stress test si è rivelato  una parte critica dell'algoritmo, anche per matrici di dimensione di dimensione parti a 10.


