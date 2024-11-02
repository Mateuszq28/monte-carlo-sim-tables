#### Powiązane projekty
- [monte-carlo-sim-python](https://github.com/Mateuszq28/monte-carlo-sim-python) - własna implementacja symulacji światła, moduł wizualizacji ścieżki przemieszczania się fotonów w 3D (za pomocą Vispy)
- [monte-carlo-sim-benchmark](https://github.com/Mateuszq28/monte-carlo-sim-benchmark) - przykładowe symulacje z literatury (tiny, small, mc321) oraz ich porównanie z własną symulacją, zapis do jednolitego formatu `CUBES.json`, przetwarzanie końcowe i normalizacja, generowanie tabel porównawczych, wykresy, mapy ciepła, wizualizacje 3D, mapy ciepła
- [monte-carlo-sim-tables](https://github.com/Mateuszq28/monte-carlo-sim-tables) - tabele ze statystykami rozkładów transportu fotonów dla przeprowadzonych eksperymentów
- [CUBES](https://1drv.ms/f/c/7871da7edeb06dcc/Ei70d6guE4lBgMsf6FgGbJsBUcYmqrgZFZZxBHvQeMgqBQ) - wyniki najważniejszych eksperymentów zapisane w ujednoliconym formacie `CUBE.json`

### Tabele ze statystykami rozkładów transportu fotonów dla przeprowadzonych eksperymentów.
**all_print_stats.csv** - indywidualne cechy rozkładów\
**all_compare2benchmark.csv** - porównanie do benchmarku, czyli najlepszej symulacji z serii


oznaczenia w **all_print_stats.csv:**
| nazwa                    | opis
|-------------------------:|:-----------------------------------------------------------------------|
Name | nazwa
Sum | suma
Avg | średnia
ks_normal | statystyka testu Kolmogorov–Smirnova na normalność rozkładu, odfiltrowane wartości poniżej 1 percentyla i powyżej 99 percentyla
ks_normal pval | wartość p testu Kolmogorov–Smirnova (wyżej)
ks_normal log | statystyka testu Kolmogorov–Smirnova na normalność rozkładu, odfiltrowane wartości poniżej 1 percentyla i powyżej 99 percentyla, przekształcenie logarytmem
ks_normal log pval | wartość p testu Kolmogorov–Smirnova (wyżej)
ks_normal tan | statystyka testu Kolmogorov–Smirnova na normalność rozkładu, odfiltrowane wartości poniżej 1 percentyla i powyżej 99 percentyla, przekształcenie funkcją tangens
ks_normal tan pval | wartość p testu Kolmogorov–Smirnova (wyżej)
ks yeo-johnson | statystyka testu Kolmogorov–Smirnova na normalność rozkładu, odfiltrowane wartości poniżej 1 percentyla i powyżej 99 percentyla, przekształcenie Yeo-Johnson
ks yeo-johnson pval | wartość p testu Kolmogorov–Smirnova (wyżej)
ks quantile | statystyka testu Kolmogorov–Smirnova na normalność rozkładu, odfiltrowane wartości poniżej 1 percentyla i powyżej 99 percentyla, przekształcenie transformerem kwantylowym
ks quantile pval | wartość p testu Kolmogorov–Smirnova (wyżej)
skew | skośność
kurtosis | kurtoza
q0 | wartość minimalna
q0_25 | pierwszy kwartyl
q0_50 | drugi kwartyl
q0_75 | trzeci kwartyl
q1 | wartość maksymalna
std | odchylenie standardowe
variance | wariancja
Overflow | suma transportu fotonu poza badanym obszarem
perc_in | stosunek transportu fotonu wewnątrz badanego obszaru do całkowitego transportu fotonów
n_photons | liczba fotonów
non_zero_vals | liczba komórek różnych od zera
zero_vals | liczba komórek równych zero
table_category | kategoria tabeli (całość - spłaszczenie, przekrój, średnia)
experiment_seria | seria eksperymentów
benchmark_path | najlepsza symulacja z serii - wzorzec


oznaczenia w **all_compare2benchmark.csv:**
| nazwa                    | opis
|-------------------------:|:-----------------------------------------------------------------------|
name | nazwa
corr spearman | korelacja Spearmana
pval spearman | wartość p korelacji Spearmana
t_stat | test T Wilcoxona
t_pval | wartość p testu T Wilcoxona
u_stat | test U Manna-Whitney’a
u_pval | wartość p testu U Manna-Whitney’a
chi2_flat_stat | test niezależności zmiennych chi-kwadrat przeprowadzony na częstościach spłaszczonych tablic
chi2_flat_pval | wartość p testu niezależności zmiennych chi-kwadrat
chi2_2d_stat | test niezależności zmiennych chi-kwadrat przeprowadzony na częstościach średnich (obrazów 2D)
chi2_2d_pval | wartość p testu niezależności zmiennych chi-kwadrat
chi2_3d_stat | test niezależności zmiennych chi-kwadrat przeprowadzony na częstościach histogramów 3D
chi2_3d_pval | wartość p testu niezależności zmiennych chi-kwadrat
MSE | błąd średniokwadratowy
RMSE | średnia kwadratowa błędów
MSE raw | błąd średniokwadratowy przed odfiltrowaniem wartości skrajnych
RMSE raw | średnia kwadratowa błędów przed odfiltrowaniem wartości skrajnych
ks_stat1 | statystyka testu Kolmogorov–Smirnova na normalność rozkładu pierwszego
ks_pval1 | wartość p testu Kolmogorov–Smirnova (wyżej)
ks_stat2 | statystyka testu Kolmogorov–Smirnova na normalność rozkładu drugiego (benchmark, wzorcowy)
ks_pval2 | wartość p testu Kolmogorov–Smirnova (wyżej)
ks_test_eq | statystyka testu Kolmogorov–Smirnova na pochodzenie obu zbiorów z tego samego rozkładu
ks_pval_eq | wartość p testu Kolmogorov–Smirnova (wyżej)
levene_stat | test Levena na równość wariancji
levene_pval | wartość p testu Levena
corr_pearson | korelacja Pearsona (nieistotna ze względu na brak rozkładu normalnego)
pval_pearson | wartość p korelacji Pearsona
ttind_stat | test t dla prób niezależnych (nieistotna ze względu na brak rozkładu normalnego)
ttind_pval | wartość p testu t
ttrel_stat | test t dla prób zależnych (nieistotna ze względu na brak rozkładu normalnego)
ttrel_pval | wartość p testu t
table_category | kategoria tabeli (całość - spłaszczenie, przekrój, średnia)
experiment_seria | seria eksperymentów
benchmark_path | najlepsza symulacja z serii - wzorzec
