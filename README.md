# Previsione dei giorni di indennizzo

Progetto d'esame di Machine Learning, ITS Digital Academy.

## Obiettivo
Stimare quanti giorni vengono indennizzati per ogni caso di malattia professionale, a partire dai dati del caso.

## Metodo
- Preparazione dei dati: estrazione di anno e mese dalla data, codifica delle variabili categoriche, valori mancanti sostituiti con la mediana, standardizzazione
- Modello base: Random Forest Regressor ottimizzato con GridSearchCV (240 combinazioni di parametri, validazione incrociata a 5 fold)
- Modello a due stadi: un classificatore decide se il caso ha giorni di indennizzo, un regressore stima quanti

## Risultati sul test set
| Modello | MAE (giorni) | MSE |
| --- | --- | --- |
| Random Forest singolo | 19,1 | 890 |
| Classificatore + regressore | 17,1 | 997 |

Il modello a due stadi sbaglia meno in media, ma commette qualche errore grande in più.

## Strumenti
Python, pandas, scikit-learn, Jupyter Notebook

## Nota
Il dataset non è incluso nel repository.
