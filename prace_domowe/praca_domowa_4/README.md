# Praca domowa 4

1. Dane obrazowe
Stworzyć pipeline do preprocessingu, aby działał z każdą bazą danych zdjęciową z zespołu. W celach testowych ograniczyć liczbę zdjęć z każdej bazy do kilku (aby dało się to odznaczyć). Narzędzie ma służyć w przyszłości do szybkiego łączenia kilku baz danych w jeden zbiór treningowy. Nie zmieniać sztucznie folderów, w których znajdują się pierwotnie zdjęcia z bazy danych. W preprocesingu przygotować ujednolicenie rozmiaru zdjęć do wybranego rozmiaru, jedna operacja przeskalowania wartości pikseli lub operacja na histogramie oraz minimum jedna inna operacja na obrazie (uzasadnić wybór w oparciu o różnice między bazami danych, które badaliście w poprzednich pracach domowych). 

 
2. Dane tekstowe
W przypadku braku bazy danych z tekstem w grupie, to należy połączyć artykuły dotyczące baz danych w jeden i na tym tekście przeprowadzić następujące operacje:
- zamienić na małe litery
- usunąć cyfry lub zamienić na odpowiednie tagi + uzasadnić wybór
- usunąć śmieci z tekstu (nie ręcznie, ale np. przy użyciu wyrażeń regularnych!) + napisać co zostało usunięte
- wykonać part-of-speech tagging + napisać wnioski
- zamienić tekst na wektory - użyć pretrenowane word embeddingi np. word2vec, GloVe, BERT + uzasadnić wybór
- użyć narzędzi do lemmatyzacji i do stemmingu

 
3. Dane tabelaryczne
Wykonać dla wszystkich danych tabelarycznych, na których można wytrenować model, a jeśli takich nie ma, to również na takich, które można dodać do modelu obrazowego. Celem preprocessingu jest przygotowanie danych do treningu modelu, dlatego zachęcam do takiego przygotowania danych, aby Wasz model mógł osiągnąć na nich jak najlepsze wyniki.
- poradzić sobie z brakującymi i nieprawidłowymi danymi + uzasadnić dlaczego w ten sposób
- przeskalować wartości
- zastosować odpowiednie kodowanie danych kategorycznych + uzasadnić dlaczego takie
- usunąć współliniowość, jeśli istnieje
- odrzucić nieistotne kolumny, (jeśli taki istnieją) + uzasadnić

Uwaga:
Dane CT i RTG należy traktować jako osobne zbiory, nie łączyć ich.
Liczbę kanałów, jeśli jest różna w obrazach w bazach danych, to należy ujednolicić, sugeruję jednokanałowe.
Zdjęcia CT 2D i 3D można traktować osobno, albo połączyć i zamienić 3D na wiele 2D, trzeba jednak rozważyć za i przeciw oraz co chcecie wykorzystać i jak do trenowania Waszych modeli.
