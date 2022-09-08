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

</details>
