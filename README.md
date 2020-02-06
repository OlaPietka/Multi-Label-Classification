# MultiLabelClassification_Py

**Opis sieci** 
Trenowanie sieci polegało na klasyfikacji wieloetykietowej. Sieć uczona była na następujących zestawach etykiet: 
* Black jeans
* Blue dress
* Blue jeans
* Blue shirt
* Red dress 
* Red shirt 
 
W pierwszej wersji programu została zaimplementowana sieć LeNet5, natomiast po próbach i głębszej analizie zdecydowałam się na sieć SmallerVGNet, która okazała się przynieść najlepsze wyniki.
  

Hiperparametery | Wartości
------------ | -------------
Batch size | 32 
Image resize | 96 
Image depth | 3 
Agumentation | Rotation range: 30 Width shift range: 0.1  Height shift range: 0.1 Zoom range: 0.2 Horizontal flip: True 
Optimizer | Adam 
Loss | Binary corssentropy 
Neural | network type SmallerVGNet 
Epochs | 50, 75, 150, 500, 1000 
 
 

 
Omówienie 
Każde uczenie omawiane poniżej zostało wykonane dla hiperparametrów wymienionych wcześniej. Testowanie odbywa się na 31 zdjęciach nie zawartych w zbiorze treningowym. 
 
Dla 50 epoch: 
 
Poprawnie rozpoznane dwie etykiety: 68% 
Poprawnie rozpoznana jedna etykieta: 32% 
Nie rozpoznano poprawnie żadnej etykiety: 0% 
 
Dla 75 epoch: 
 
Poprawnie rozpoznane dwie etykiety: 74% 
Poprawnie rozpoznana jedna etykieta: 26% 
Nie rozpoznano poprawnie żadnej etykiety: 0% 
 
Dla 150 epoch: 
 
Poprawnie rozpoznane dwie etykiety: 71% 
Poprawnie rozpoznana jedna etykieta: 29% 
Nie rozpoznano poprawnie żadnej etykiety: 0% 
 
Dla 500 epoch: 
 
Zdaje się, że val_loss zaczyna rosnąć przy takiej ilości epoch, przez co może dojść do przeuczenia sieci. 
 
Poprawnie rozpoznane dwie etykiety: 77% 
Poprawnie rozpoznana jedna etykieta: 23% 
Nie rozpoznano poprawnie żadnej etykiety: 0% 
 
Mimo, że val_loss wydaje się rosnąć, osiągnęliśmy lepszy wynik niż w poprzednich przypadkach. Żeby dokładnie sprawdzić wzrost val_loss przeprowadziłam jeszcze jedno trenowanie dla dwukrotnie więcej epoch. 
 
Dla 1000 epoch: 
 
 
Teraz możemy łatwo zauważyć, że val_loss zaczyna rosnąć od około 150. 
 
Poprawnie rozpoznane dwie etykiety: 74% 
Poprawnie rozpoznana jedna etykieta: 26% 
Nie rozpoznano poprawnie żadnej etykiety: 0% 
 
Mimo przeuczenia sieci osiągnęliśmy taki sam wynik jak dla 150 epoch. 
 
 
 
 
Podsumowanie 
Najlepszy wynik osiągnęliśmy dla 500 epoch w postaci 77% poprawnie rozpoznanych dwóch etykiet. 
 
Zdjęcia których żadna wytrenowana sieć nie była w stanie rozpoznać w pełni poprawnie: 
 
 Sieć nie była uczona dla zestawów „Red jeans” oraz „Black dress” dlatego dla powyższych przykładów mogliśmy się spodziewać takiego wyniku. 
 
Różnego rodzaju wariacje, które każda wytrenowana sieć rozpoznała poprawnie: 
 
 
