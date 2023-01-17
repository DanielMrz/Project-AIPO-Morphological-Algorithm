# Project-AIPO-Morphological-Algorithm
Algorytm obcinania gałęzi polega na stopniowym redukowaniu odcinków posiadających wolne zakończenie. W ostateczności powstają jedynie zamknięte pętle i odcinki przecinające brzeg obrazu.


Funkcjonalność programu opiera się na przetwarzaniu obrazu binarnego za pomocą operacji morfologicznych. W przetwarzaniu obrazów binarnych ważne jest określenie, kiedy dwa piksele sąsiadują ze sobą. W tym celu definiuje się dla każdego piksela jego sąsiedztwo.
Najczęściej wykorzystywane sąsiedztwa punktu „p”  o współrzędnych (x,y) to:

czterospójne - obejmuje cztery piksele przyległe do danego z góry, dołu i po bokach,
 ![image](https://user-images.githubusercontent.com/18464477/213010735-062a64a3-4875-4fb3-a842-634faaa62a17.png)

ośmiospójne - obejmuje osiem pikseli przyległych do danego po jednym z góry i z dołu, dwa po bokach oraz cztery na przekątnych,
 ![image](https://user-images.githubusercontent.com/18464477/213010747-8d16553f-1f54-421b-8f4c-178dddb077b7.png)

Operacje morfologiczne są jednymi z ważniejszych operacji przetwarzania obrazów, gdyż pozwalają przeprowadzić zaawansowaną analizę kształtów poszczególnych obiektów oraz odległości między nimi. Podstawowe przekształcenia morfologiczne można ze sobą łączyć, co daje podstawę do budowania skomplikowanych systemów analizy obrazu. Przetwarzanie obrazów binarnych odbywa się z wykorzystaniem morfologii matematycznej.
Właściwości filtrów morfologicznych określane są przez tzw. element strukturalny, wykorzystywany jako ruchome okno. Określony jest względem wybranego piksela, tzw. punktu centralnego lub początkowego. Element strukturalny  może przybrać dowolny kształt i wielkość, zawierać dowolną kombinację wartości 0 i 1, zaś jego punkt centralny może być w dowolnym miejscu. Dla uproszczenia zapisu skomplikowanych kształtów można niektórym pikselom przypisać literę oznaczającą, że mogą one przyjąć dowolną wartość.
Jednym z częściej stosowanych elementów strukturalnym jest kwadrat o boku 3x3 i wartości 1 dla wszystkich pikseli. W niektórych operacjach element strukturalny jest obracany symetrycznie względem punktu środkowego.
 ![image](https://user-images.githubusercontent.com/18464477/213010776-2cae7740-dbce-4883-b641-764487b0c743.png)
 
 Szkielet figury, to zbiór wszystkich punktów równoodległych od co najmniej dwóch brzegów. Szkielet odzwierciedla podstawowe własności topologiczne figury, a jego dalsza analiza może zostać wykorzystana do
- klasyfikacji figur ze względu na kształt,
- wyznaczania orientacji figur podłużnych,
- określania linii środkowej szerszych linii,
- rozdzielanie złączonych obiektów.
Szkieletyzacja jest operacją wyznaczania liniowej reprezentacji (szkieletów) figur na analizowanym obrazie. Można ją wyznaczać na dwa sposoby
- stosując operację pocieniania, mówi się wtedy o szkielecie binarnym,
- na podstawie transformaty odległościowej - otrzymując tzw. szkielet MAT,
Wyznaczanie szkieletu binarnego polega na wielokrotnym stosowaniu (często naprzemiennych, z różnymi elementami strukturalnymi) operacji pocieniania - do momentu, aż kolejne operacje nie wpływają na wygląd obrazu wynikowego. W tym celu można stosować różne zestawy elementów strukturalnych. Program wykorzystuje operację pocieniania.

Algorytm obcinania gałęzi polega na stopniowym redukowaniu odcinków posiadających wolne zakończenie. W ostateczności powstają jedynie zamknięte pętle i odcinki przecinające brzeg obrazu.



