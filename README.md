<details>

<summary>Statistical Analysis of Microbiome Data with R</summary>

Należy uwzględnić metodę przechowywanai prób. Ekstrakcja DNA ze świezych pod zamrożonych może wpłynąć strukture mikrobiomu. Dla przykładu, przechowywanie prób w -80 stopniach vs natychmiastowa ekstrakcja ma przełożenie na stosunek Firmicutes do Bacteroidetes w późniejszym PCRze.

OTU obejmują sekwencje które różnią się o nie więcej niż o 3% (gatunki), 5% (genus - rodzaj), 20% (phylum - gromada)

Domyślnie OTU jest utożsamiane z róznicami <3%, dlatego OTU czasem wymiennie niektórzy stosują z gatunkiem.

OTU nie powstają w oparciu o referencje (klasteryzacja a nie klasyfikacja), więc mogą obejmować kilka jednostek taksonomicznych.

16S rRNA seq zawyża różnorodność bakteryjną z racji błędów podczas sekwencjonowania oraz amplifikacji. Zniwelowanie tego błędu jest trudne

16S rRNA seq jest w stanie tylko ocenić występowanie danych taksonów ale nie ich biologiczne funkcje.

16s rRNA seq jest wykorzystywane tylko do ustalenai obecności znanych taksonów o poznanych markerach, które da się amplifikować.

Brak złotych standardów pod kątem QC, filtorwania i ogólnie analizy.

PERMANOVA jest testem nieparametrycznym.

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
