# SBB Sitzbänke Analyse

Gibt es einen Zusammenhang zwischen dem Anteil älterer Menschen in einer Gemeinde und der Sitzbank-Versorgung am dortigen Bahnhof?

**→ [Zur Webseite](https://mfriedlipublic.github.io/SBB_Benches)**

---

## Idee

Sitzbänke sind besonders für Seniorinnen und Senioren wichtig. Ich wollte wissen ob Bahnhöfe in Gemeinden mit einem höheren Anteil älterer Menschen entsprechend besser ausgestattet sind — und ob sich das in den öffentlich verfügbaren SBB-Daten zeigt.

Das Resultat: ein schwacher aber statistisch signifikanter Zusammenhang (r ≈ 0.23). Ob durch Planung oder Zufall sei dahingestellt.

> Spassprojekt. Rein explorativ, nicht überinterpretieren.

## Datenquellen

Alle Daten sind öffentlich verfügbar und können direkt heruntergeladen werden:

| Datensatz | Quelle |
|---|---|
| Mobiliar im Bahnhof | [data.sbb.ch](https://data.sbb.ch/explore/dataset/mobiliar-im-bahnhof/) |
| Passagierfrequenz | [data.sbb.ch](https://data.sbb.ch/explore/dataset/passagierfrequenz/) |
| Didok Haltestellen | [data.sbb.ch](https://data.sbb.ch/explore/dataset/dienststellen-gemass-opentransportdataswiss/) |
| Anteil über 65-Jährige pro Gemeinde | [mapexplorer.bfs.admin.ch](https://mapexplorer.bfs.admin.ch/?obs=main&lang=de#c=indicator&i=ch_01_02_01a.pop65&i2=ch_01_02_01a.anteilpop65&s=2024&s2=2024&view=map179) |

Die Excel- und CSV-Dateien sind nicht im Repository enthalten — einfach direkt von den Quellen oben herunterladen und im gleichen Ordner wie das Notebook ablegen.

## Struktur

```
SBB_Benches/
├── analyse.ipynb   # Analyse-Notebook
├── index.html      # Generierte Webseite
└── README.md
```

## Reproduzieren

```bash
pip install pandas numpy plotly scipy openpyxl
jupyter notebook analyse.ipynb
```

Die letzte Zelle generiert die `index.html`.
