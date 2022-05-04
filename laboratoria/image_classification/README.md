# Basic MNIST Example
Ze strony: https://github.com/pytorch/examples/tree/main/mnist

```bash
pip install -r requirements.txt
python main.py
# CUDA_VISIBLE_DEVICES=2 python main.py  # to specify GPU id to ex. 2
```

Zadanie 1: uruchomić trening - trenować kilka epok i zapisać wytrenowany model

	Odpowiedz na pytania: 
	- Co zrobić w przypadku "pytorch RuntimeError: CUDA error: out of memory"?
	- Jak zmienia się loss w trakcie treningu?
	- Jak wygląda architektura sieci?
	- Jaka jest funkcja straty, optymalizator, funkcja aktywacji w ostatniej warstwie?

Uwaga: W celu nauki, każdą dalszą zmianę można uruchamiać na treningu, który będzie trwał 1 epokę.

	
Zadanie 2: Dodaj do preprocessingu zdjęć RandomRotation.


Zadanie 3: Wyświetl przykładowe zdjęcia wraz z przewidzianymi etykietami.


Zadanie 4: Zmień model na pretrenowany Resnet-18 i wejście trzykanałowe.

	Kroki: 
	I) zmienić obraz na trzykanałowy
	II) zmienić sieć na ResNet-18
	III) załadować pretrenowane wagi
	
	 Pomocny materiał: https://github.com/pytorch/tutorials/blob/master/beginner_source/transfer_learning_tutorial.py


Zadanie 5: Zmień bazę danych na: https://download.pytorch.org/tutorial/hymenoptera_data.zip i dostosuj kod do zadania klasyfikacji binarnej.
	
	 Pomocny materiał: https://github.com/pytorch/tutorials/blob/master/beginner_source/transfer_learning_tutorial.py

