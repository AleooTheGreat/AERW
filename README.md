# AERW — Autoencoder cu Regresie și Filtrare Wavelet

Acest repository conține codul sursă pentru lucrarea de licență *Autoencoder cu regresie și filtrare wavelet*, care propune înlocuirea filtrului EWMA din modelul AER cu un filtru wavelet trece-jos pentru detecția anomaliilor în serii temporale.

## Conținut

- **`AERW.ipynb`** — notebook-ul principal, care conține întreaga implementare: modelul AER, sistemul de detecție, filtrul wavelet și toate experimentele din lucrare (comparația EWMA vs wavelet, sweep-ul pe familiile de wavelet și valorile parametrului `f`, evaluarea metodei Donoho-Johnstone).
- **`NAB-master/`** — setul de date Numenta Anomaly Benchmark.
- **`Yahoo_S5_Data/`** — setul de date Yahoo! Webscope S5.

## Cum se rulează

Notebook-ul este conceput pentru a rula pe **Google Colab**.

1. Deschide [Google Colab](https://colab.research.google.com/).
2. Apasă pe **File → Upload notebook** și încarcă `AERW.ipynb`.
3. Încarcă în sesiunea Colab și folderele cu date (`NAB-master/` și `Yahoo_S5_Data/`), astfel încât notebook-ul să le poată accesa.
4. La începutul notebook-ului se află o secțiune de configurare unde poți seta parametrii experimentului (setul de date, familia wavelet, valoarea lui `f`, numărul de seed-uri etc.).
5. Rulează celulele în ordine (**Runtime → Run all**).

## Recomandare hardware

Pentru reproducerea completă a rezultatelor (rulări pe 25 de seed-uri pe NAB și 10 pe Yahoo S5) este recomandat un abonament **Google Colab Pro** sau **Pro+**, care oferă acces la GPU-uri mai rapide (NVIDIA L4) și sesiuni mai lungi. Rezultatele din lucrare au fost obținute pe Colab Pro+ cu GPU NVIDIA L4.
