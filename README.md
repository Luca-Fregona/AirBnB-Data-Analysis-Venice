# Andamento di un Airbnb: Venezia

Progetto di Data Science a cura di **Luca Fregona**.

Analisi esplorativa degli annunci Airbnb della città di Venezia, con l'obiettivo di individuare quali caratteristiche (struttura, posizione, recensioni, servizi) influenzano maggiormente il prezzo degli alloggi.

## Motivazioni

Il mercato degli affitti brevi rappresenta un settore di grande interesse. Il progetto esplora la situazione attuale degli Airbnb nel contesto unico della città di Venezia, combinando analisi dei dati e strategie mirate per identificare le migliori caratteristiche degli annunci.

## Obiettivo

Analizzare i dati più rilevanti relativi agli Airbnb di Venezia al fine di individuarne le migliori caratteristiche.

## Dataset

I dati provengono da [Inside Airbnb](https://insideairbnb.com/), snapshot di Venezia del 7 dicembre 2024:

- [listings.csv.gz](https://data.insideairbnb.com/italy/veneto/venice/2024-12-07/data/listings.csv.gz)

### Preparazione dei dati

- Rimozione delle colonne poco rilevanti per l'analisi (es. `host_name`, `minimum_nights`)
- Esclusione delle proprietà sulla terraferma di Venezia
- Rimozione delle righe con valori NaN nelle categorie più rilevanti (es. `price`)
- Riempimento dei valori NaN nelle altre colonne con informazioni opportune
- Correzione dei dtype delle colonne

## Struttura dell'analisi

- **A** — Analisi del prezzo in base alla struttura degli Airbnb
- **B** — Analisi del prezzo in base alla distribuzione geografica degli Airbnb, con heatmap dei prezzi sulla cartina di Venezia
- **C** — Analisi del prezzo in base alle recensioni degli Airbnb
- **D** — Analisi del prezzo in base ai servizi offerti dagli Airbnb, con individuazione dei servizi più e meno correlati al prezzo

## Principali risultati

- La maggior parte degli alloggi sono intere case (86,7%), con meno di tre camere e 2,5 bagni
- Il prezzo dipende da dimensioni e posizione: San Marco è il quartiere più costoso, mentre Murano e Burano offrono soluzioni economiche con ottime recensioni
- Gli alloggi più economici ricevono più recensioni, mentre quelli più costosi hanno generalmente punteggi più alti sulla posizione
- Servizi come lavastoviglie e balcone aumentano il valore percepito, mentre altri come il self check-in non sembrano avere lo stesso effetto

## Tecnologie utilizzate

- **Python**
- **Jupyter Notebook**
- **pandas** — pulizia e analisi dei dati
- **folium** — heatmap geografica interattiva
- **reveal.js** — esportazione del notebook in presentazione a slide (via nbconvert)

## Struttura del repository

```
├── progetto_slides.html   # Presentazione (slide reveal.js esportate dal notebook)
├── README.md
```

## Come visualizzare la presentazione

Basta aprire il file `progetto_slides.html` in un browser. Usare le frecce direzionali per navigare tra le slide.

## Autore

Luca Fregona
