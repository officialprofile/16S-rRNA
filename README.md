<details>

<summary>Statistical Analysis of Microbiome Data with R</summary>
https://doi.org/10.1007/978-981-13-1534-3

Należy uwzględnić metodę przechowywanai prób. Ekstrakcja DNA ze świezych lub zamrożonych może wpłynąć strukture mikrobiomu. Dla przykładu, przechowywanie prób w -80 stopniach vs natychmiastowa ekstrakcja ma przełożenie na stosunek Firmicutes do Bacteroidetes w późniejszym PCRze.

OTU obejmują sekwencje które różnią się o nie więcej niż o 3% (gatunki), 5% (genus - rodzaj), 20% (phylum - gromada)

Domyślnie OTU jest utożsamiane z róznicami <3%, dlatego OTU czasem wymiennie niektórzy stosują z gatunkiem.

OTU nie powstają w oparciu o referencje (klasteryzacja a nie klasyfikacja), więc mogą obejmować kilka jednostek taksonomicznych.

16S rRNA seq zawyża różnorodność bakteryjną z racji błędów podczas sekwencjonowania oraz amplifikacji. Zniwelowanie tego błędu jest trudne

16S rRNA seq jest w stanie tylko ocenić występowanie danych taksonów ale nie ich biologiczne funkcje.

16s rRNA seq jest wykorzystywane tylko do ustalenia obecności znanych taksonów o poznanych markerach, które da się amplifikować.

Brak złotych standardów pod kątem QC, filtorwania i ogólnie analizy.

PERMANOVA jest testem nieparametrycznym.

Analiza mocy jest stosowana w celu ustalenia minimalnej liczebności próby potrzebnej do wykrycia efektu o zadanej wielkości. Ewentualnie możemy jej użyć do wyznaczenia mocy, gdy znamy wielkosć efektu oraz liczebność próby. Zbyt duża liczebność też stanowi problem, gdyż wtedy będziemy wykrywać zbyt małe efekty. 

W przypadku testu t moc zależy od: całkowitej liczebności prób, stosunku wielkości jednej próby do drugiej, alfyy, wielkości efektu, odchylenia standardowego.

Moc, wielkość efektu, wielkość próby i alfa są wzajemnie powiązanymi parametrami, tj. każdy jest funkcją pozostałych trzech.

Test nieparametryczny może być mocniejszy od swojego parametrycznego odpowiednika gdy założenia nie są spełnione.

UniFrac nieważony uwzględnia tylko obecność lub nieobecność danych gatunków, natomiast ważony uwzględnia dodatkowo informację na temat liczebności, którą wykorzystuje jako wagę dla drzewa filogenetycznego, na podstawie którego obliczana jest odległość.

Później rozwinięto metodę dokonując poprawki na różnice w wariancjach.

Zero-inflated data, sparse data są problemem z punktu widzenia wymiarowości; z powodu prawoskośnego rozkładu który generują modeluje się ten rozkład za pomocą ujemnego rozkładu dwumianowego.

Metrykami alfa różnorodności są indeksy Chao 1, Shannon (Shannon-Wiener), Simpson i Pielou.

Indeks Chao1 może być liczby tylko na liczbahc całkowitych.

Indeks Shanonna przykłada większą wagę do mniej powszechnych gatunków. Indeks Shanonna H' zwykł nie przekraczać 5.0. 

Indeks Simpsona kładzie większą wagę na bardziej popularne gatunku, jego wartość waha się od 0 do prawie 1. Indeks ten jest względnie odporny na obecność rzadkich gatunków (dodajemy kwadraty prawdopodobieńśtw).

Generalnie możemy wyróżnić dwie charakterystyki alfa róznorodności: równomierność (evenness) oraz bogactwo (richness). H0 dla evenness to "wszystkie gatunki w hipotetycznej społeczności (community) są równoliczne.

Miary beta różnorodności możemy podzielić na binarne oraz ilościowe. Te pierwsze owzględniają tylko obecność lub nie dalego gatunku, natomiast ilościowe także liczebność.

O ile obliczanie alfa różnorodności jest proste, o tyle sposób mierzenia beta jest kontrowersyjny. Najpopularniejszymi miarami jest wskaźnik Jaccarda (binarna) oraz Braya-Curtisa.  

Wskaźnik Jaccarda można przedstawić w formie diagramu venna (proporcja części wspólnej do całości). Przyjmuje wartości od 0 (różne) do 1 (podobne).

Miara Braya-Curtisa to proporcja oparta o metrykę taksówkową, przyjmuje wartości od 0 (podobne) do 1 (różne). Rzadkie gatunki mają niewielkie znaczenie dla wartości współczynnika (w mianowniku jest dodawanie liczbności gatunku z obu prób, a liczniku różnica).

metody aglomeryzacyjne = klasteryzacja

single-linkage agglomerative clustering = metoda najbliższego sąsiada. Są jeszcze complete-linkage (najdalższy sąsiad) oraz average linkage.

Klasteryzacja Warda - taka jakby ANOVA, grupowanie aby minimalizować wariancję

</details>


<details>

<summary>Useful links</summary>
https://rachaellappan.github.io/VL-QIIME2-analysis/

https://github.com/BikLab/BITMaB2-Tutorials/blob/master/QIIME2-metabarcoding-tutorial-already-demultiplexed-fastqs.md

https://github.com/uw-madison-microbiome-hub/Microbiome_analysis_in-_R

https://cran.r-project.org/web/packages/corncob/vignettes/corncob-intro.pdf

https://www.nicholas-ollberding.com/post/introduction-to-the-statistical-analysis-of-microbiome-data-in-r/
</details>
