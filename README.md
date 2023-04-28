## NIEKTORÉ DATASETY SÚ DOSTUPNÉ LEN NA VYŽIADANIE, KEĎŽE ICH VEĽKOSŤ PRESAHUJE KAPACITU REPOZITÁRA
## SOME DATA SETS WILL BE AVAILABLE ON DEMAND SINCE THEY WON'T FIT TO THE GITHUB REPO


* **1a_data_downloading_preprocessing.ipynb** - tento skript má za úlohu stiahnuť a spracovať dáta z portálu OmniWeb a porovnať ich s dátami v knižnici Aidapy. Následne sú tieto dáta predpripravené pre ďalšiu prácu, sú vyhodnotené prázdne hodnoty a sú vykonané prvotné analýzy na týchto dátach.

* **1b_data_basic_analysis_division.ipynb** - tento skript pracuje so všetkými dostupnými dátami a rozdelí ich do troch skupín - heliosferické, geomagnetické a solárne indexy.

* **2a_analysis_merged_final.ipynb** - ďalej sme použili skript bol určený na vytvorenie základných analýz, boxplotov a porovnanie priebehov jednotlivých hodnôt. Tento skript sa používa pri úvodnej analýze dátovej sady.

* **2b_anova_corr_analyses.ipynb** - ďalší skript bol použitý na prvotnú selekciu dát na trénovanie. Ide o skript, ktorým sme vytvorili korelačné a ANOVA analýzy. Výstupom z týchto analýz bol výber dôležitých parametrov, ktoré boli použité ako jeden zo vstupov pre neurónovú sieť.

* **3_data_preparation.ipynb** - Ďalší skript bol použitý na predspracovanie vstupu pre trénovanie. Cieľom bolo vytvoriť okná dát o špecifických veľkostiach s určitým časovým posunom. V skripte bola použitá min-max normalizácia, technika okien a horizontov a prístup posuvného okna. Okrem toho bola práca so správnou veľkosťou okien a riešením chýbajúcich hodnôt. Používateľ môže meniť premennú _features_cols, kde môže zadať prázdne pole pre autoregresný model alebo rôzny rozsah premenných ako vstup pre multivariabilný model. Používateľ tiež určuje veľkosť okna pomocou window_size a časový posun pomocou minutes_ahead.

* **4a_autoreg.ipynb** - tento skript je určený na trénovanie autoregresnej neurónovej siete. Parametre sietí sú popísané v práci. Trénovanie bolo vykonané na 5 epochách.

* **4b_eval_autoreg_samo.ipynb** - tento skript je určený na vyhodnotenie natrénovaného autoregresného modelu pomocou troch techník vyhodnotenia popísaných v práci. Ako výstup slúži CSV súbor, ktorý obsahuje všetky hodnoty Confusion matrix - TP, TN, FP, FN a zároveň všetky metriky, ktoré sme si vybrali na začiatku - Precision, Recall, F1 Score, AUC-ROC, AUC-PR a True Skill Score (TSS). Vyhodnocovala sa spravidla posledná epocha, no taktiež bolo možné tento prístup zmeniť a vyhodnocovať všetky epochy.

* **5a_multiNN.ipynb** - tento skript je určený na trénovanie multivariačnej neurónovej siete. Parametre sietí sú popísané v práci. Trénovanie bolo vykonané na 5 epochách.

* **5b_eval_multiNN.ipynb** - tento skript je určený na vyhodnotenie natrénovaného multivariačného modelu pomocou troch techník vyhodnotenia popísaných v práci. Ako výstup slúži CSV súbor, ktorý obsahuje všetky hodnoty Confusion matrix - TP, TN, FP, FN a zároveň všetky metriky, ktoré sme si vybrali na začiatku - Precision, Recall, F1 Score, AUC-ROC, AUC-PR a True Skill Score (TSS). Vyhodnocovala sa spravidla posledná epocha, no taktiež bolo možné tento prístup zmeniť a vyhodnocovať všetky epochy.


