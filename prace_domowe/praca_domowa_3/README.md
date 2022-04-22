# Praca domowa 3



## Mosmed
https://arxiv.org/abs/2005.06465

1. Podstawowe informacje o bazie danych: rok powstania, źródła danych, liczba danych itp.

    Dane były zebrane od 01.03 do 25.04 2020r w szpitalach miejskich w Moskwie w Rosji. Tomografie są anonimowe. Jest 1110 zdjęć. 42% to mężczyźni 56% to kobiety. Pacjenci mają od 18 do 97 lat. Mediana wieku to 47 lat.  

    Dane są podzielone na 4 kategorie: : CT-0 – 254 (22,8%), CT-1 – 684 (61,6%), CT-2 – 125 (11,3%), CT-3 – 45 (4,1%), CT-4 – 2 (0,2%). 

    Dane są w formacie NIfti. 

    Dla 50 zdjęć zanotowano również maski. 

2. Jakie istotne informacje są w artykule, a nie widać tego w bazie danych?
	
    W artukule mamy informacje o min/max/median od wieku. 
    
3. Jakie informacje dotyczące bazy danych nie zostały przedstawione w artykule? Czy mogło to być zrobione specjalnie? Uzasadnij.

    Wszytskie informacje zostały zawarte w artykule. 
	
4. Jakie artykuły korzystały z tej bazy danych? Jakie zadania były wykonywane (klasyfikacja, segmentacja, detekcja itp.)? Jakie wyniki trenowania zostały osiągnięte (jeśli nie była to jedyna baza danych, to wypisz inne tak, by dało się je zidentyfikować)?

    * COVID-19 Detection in Computed Tomography Images with 2D and 3D Approaches - https://arxiv.org/pdf/2105.08506.pdf. 
    
    Badanie omawia tworzenie modelu klasyfikacji. Model miałby predyktować, czy pacjent jest chory na Covid-19. Wynik AUC modelu na bazie danych Mosmed wynosi 0.99. Oprócz bazy Mosmed zostały również użyte bazy: CC-19; BIMCV-COVID-19; COVID-CT-MD; HKBU-HPML-COVID-19; IST-C. 
    

## Reflacx
https://arxiv.org/abs/2109.14187

1. Podstawowe informacje o bazie danych: rok powstania, źródła danych, liczba danych itp.

    Dane były zebrane w trzech fazach. W pierwszych dwóch fazach pięciu radiologów analizowało kolejno 59 i 50 tych sasmych zdjęć CXR. W drugiej fazie dodatkowo ulepszono oznakowania danych. W trzeciej fazie tych samych pięciu radiologów przeanalizowała 500 zdjęć każdy. 
    
    Pierwsza faza odbywała się od 11 lisopada 2020 do 4 stycznia 2021, druga od 1 marca 2021 do 11 marca 2021, a trzecia od 24 marca 2021 do 7 czerwca 20212. Sesja, w której były zbierane dane średnio trwała 2.21h, gdzie najdłużej były to 3.93h, a najkrócej 0.2h.

    Baza posiada 3052 przypadków. Użyto 2616 unikatowych zdjęć CXR. 3052 przypadków posiadało dane o śledzeniu ruchu oka. 
    
    Zdjęcia obserwowane przez radiologów były z bazy danych MIMIC-CXR. Zostały użyte jedyne zdjęcia, które miały informacje o tym, czy są "PA", czy "AP". Przefiltrowano również zdjęcia, które były na boku, przekrzywione, bądź przewrócone poziomo. Wzięto 20% danych z grupy testowej danych MIMIC-CXR oraz 80% z innych grup tej bazy. 
    
    Opisane jest również jak odbywała się sesja badania zdjęć. Były rejestrowane poruszanie się oczu radiologa oraz jego wypowiedzi. Do zbierania informacji stworzono specjany interfejs, który mozna znaleźć na stronie:https://github.com/ricbl/eyetracking. Lekarz mógł przybliżać zdjęcie oraz nim poruszać. Można było rysować miejsca z anomaliami płuc. Można było również poprawiać tekst transkrypcji, która na żywo rejestrowała diagnozę lekarza. 
    
    Do zbierania informacji o oku użyto urządzenia Eyelink 1000 Plus, 27 calowego monitora BenQ PD2700U oraz mikrofonu PowerMic II. 
	
    Podano również niepewności urządzeń. Średni błąd kalibracji wynosił 0.43&pm;0.02;&deg;(max 2.79&deg;) w pierwszej fazie badań, 0.43&pm;0.03;&deg;(max 1.09&deg;) w drugiej i 0.44&pm;0.01;&deg;(max 1.5&deg;) w trzeciej. 
    
    Opisane również są pewne ograniczenia badań: 
    * W badaniu używany był jeden monitor, gdzie w warunkach klinicznych jest wykorzystywane wiele. 
    * W warunkach klinicznych diagnoza jest często modyfikowana po pierewszej transkrypcji. Jednak ze względu na potrzebę zapisywania diagnozy wraz z czasem zostało to ograniczone. 
    * Przez śledzeniu ruchu oka pozycja lekarza była ograniczona. W tym jest również pozycja głowy. W związku z tym lekarze nie mogli przybliżać glowy do telewizora, co skutkowało większym użyciem przybliżenia w analizie zdjęcia. Dodatkowo lekarze stwierdzali większe zmeczenie po krótszym okresie czasu. 
    * Zostały użyte zdjęcia z jednej bazy danych, więc zdjęcia posiadają wszystkie wady zawarte w tej bazie. Oprócz tego lekarze stwierdzili, że zdjęcia są gorszej jakości niż w normalnych warunkach. 
    * Zdjęcia wyświetlane lekarzowi na monitorze nie były orginalnej jakości ze względu na ograniczenia komputera. 
    * Długość kalibracji wynosiła 45-60 min. Dodatkowo specjalnie wyznaczona osoba nadzorowała, czy kalibracja była udana. 
    
    Dane są dostępne jedynie w Physionet. 
    
2. Jakie istotne informacje są w artykule, a nie widać tego w bazie danych?

    Nie ma informacji o niepewnościach urządzenia. Reszta informacji została zawarta w bazie, często w skróconej formie, bez dokładniejszych opsiów. 
	
3. Jakie informacje dotyczące bazy danych nie zostały przedstawione w artykule? Czy mogło to być zrobione specjalnie? Uzasadnij.

    Wszystkie informacje zawarte w bazie danych zostały omówione w artykule. 
	
4. Jakie artykuły korzystały z tej bazy danych? Jakie zadania były wykonywane (klasyfikacja, segmentacja, detekcja itp.)? Jakie wyniki trenowania zostały osiągnięte (jeśli nie była to jedyna baza danych, to wypisz inne tak, by dało się je zidentyfikować)?

    * Comparing radiologists’ gaze and saliency maps generated by interpretability methods for chest x-rays - https://arxiv.org/pdf/2112.11716.pdf
    
    Artykuł omawia tworzenia map istotności dla bazy Reflacx. Udało się uzyskać wynik 0.79 AUC dla omawianych w artykule algorytmów. 
    
## SIIM_TEST_TRAIN
1. Podstawowe informacje o bazie danych: rok powstania, źródła danych, liczba danych itp.

    W 2019 roku The Society for Imaging Informatics in Medicine (SIIM)  i American College of Radiology (ACR) współpracowały z with the Society of Thoracic Radiology (STR) i MD.ai, aby zorganizować wyzwanie uczenia maszynowego dotyczące wykrywania i lokalizacji odmy opłucnowej na Kaggle.W tym konkursie uczestnicy zostali poproszeni o opracowanie modelu do klasyfikacji (i segmentacji) odmy opłucnowej z zestawu zdjęć radiograficznych klatki piersiowej, aby pomóc we wczesnym rozpoznaniu odmy opłucnowej. 
    
    Podczas konkursu uczestnicy korzystali z rozszerzonych adnotacji ze zbioru danych radiogramów klatki piersiowej z National Institutes of Health (NIH). 
    
    Baza posiada 2 foldery typu DICOM. Folder treningowy posiada 12089 plików, a testowy 3205. Dodatkowo w naszej bazie mamy również plik csv, który zapewnia kodowanie masek dla każdego obrazu.
    
    Mamy łącznie 9378 zdrowych pacjentów i 2669 pacjentów z odmą opłucnową.
    
2. Jakie istotne informacje są w artykule, a nie widać tego w bazie danych?

    Ta baza nie posiada swojego głównego artykułu, ponieważ była częścią konkursu. 
    
3. Jakie informacje dotyczące bazy danych nie zostały przedstawione w artykule? Czy mogło to być zrobione specjalnie? Uzasadnij
    
    Nie ma informacji na temat brakujących zdjęć do masek. Myślę, że mógł być to zabieg specjalny jako dodatkowe utrudnienie w ramach części konkursu.
    


4. Jakie artykuły korzystały z tej bazy danych? Jakie zadania były wykonywane (klasyfikacja, segmentacja, detekcja itp.)? Jakie wyniki trenowania zostały osiągnięte (jeśli nie była to jedyna baza danych, to wypisz inne tak, by dało się je zidentyfikować)?
    
    Artykuł "SIIM-ACR Pneumothorax Segmentation" z portalu medium.com użył segmentacji. Na kaggle w związku z konkursem możemy znaleźć wiele amatorskich prac związacych z segmentacją i klafyfikacją. 


## ZhangLabData
1. Podstawowe informacje o bazie danych: rok powstania, źródła danych, liczba danych itp.

    Ten zestaw danych zawiera tysiące zweryfikowanych obrazów OCT i RTG klatki piersiowej opisanych i przeanalizowanych w „Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep Learning”. 
    
    Obrazy są podzielone na zestaw treningowy i zestaw testowy niezależnych pacjentów. Obrazy są oznaczone jako (choroba)-(randomizowany identyfikator pacjenta)-(numer obrazu przez tego pacjenta). OCT są podzielone na 4 katalogi: CNV, DME, DRUSEN i NORMAL. Obrazy rentgenowskie klatki piersiowej są podzielone na 2 katalogi: PNEUMONIA, NORMAL.
    
    Zdjęć OCT mamy 108312. W folderze trening mamy ich CNV-37206, DME-11349, DRUSEN-8617, NORMAL-51140. W folderze test mamy po 250 zdjęć dla każdej kategorii. Zdjęć X-ray mamy 5856. W folderze trening mamy chorych na odme płucną: bakteryjną-2538 oraz wirusową-1345, oraz zdrowych 1349. W części trengowej mamy chorych na odme płucną: bakteryjną-242 oraz wirusową-148, oraz zdrowych 624.
    
    Zdjęcia X-ray zostały wybrane ze zbioru ze szpitala Guangzhou Women and Children’s Medical Center, Guangzhou. 
    
2. Jakie istotne informacje są w artykule, a nie widać tego w bazie danych?
    
    Dla OCT: Z artykułu możemy dowiedzieć się o cechach charakterystycznych naszych pacjentów tj. wiek, płeć, pochodzenie. Dodatkowo dowiadujemy się, że ilość pacjentów, których zdjęcia użyto do folderu treningowego (108 312 obrazów od 4686 pacjentów) oraz testowego (1000 obrazów od 633 pacjentów) jest mniejsza od ilości zdjęć, zatem niektórzy pacjenci znajdują się na więcej niż jednym zdjęciu
    
    Dla X-ray: Dowiadujemy się o wieku naszych pacjentów. Są to dzieci od 1 do 5 roku życia. Dodatkowo dowiadujemy się, że zarówno w części testowej i treningowej każdy pacjent jest jedynie na jednym zdjęciu.
    
    W celu analizy zdjęć rentgenowskich klatki piersiowej, wszystkie radiogramy klatki piersiowej były początkowo sprawdzane pod kątem kontroli jakości poprzez usunięcie wszystkich skanów o niskiej jakości lub nieczytelnych. Zatem wszystkie zdjęcia powinny być dobrej jakości.
    
3. Jakie informacje dotyczące bazy danych nie zostały przedstawione w artykule? Czy mogło to być zrobione specjalnie? Uzasadnij.
    
    Nie zawarto informacji na temat litery R zawartej na zdjęciach, która w zależności od zdjęcia jest usytuowana w różnej części zdjęcia. Nie zawarto informacji o aparaturze medycznej na zdjęciach. 
    
4. Jakie artykuły korzystały z tej bazy danych? Jakie zadania były wykonywane (klasyfikacja, segmentacja, detekcja itp.)? Jakie wyniki trenowania zostały osiągnięte (jeśli nie była to jedyna baza danych, to wypisz inne tak, by dało się je zidentyfikować)?
    
    Nasz główny artykuł - "Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep Learning". Zadania wykonywane i ich wyniki to:
    Dla OCT: Multi-class comparison accuracy: 96.6%, “limited model” classifying accuracy 93.4%, Binary classifirers: normal vs CNV accuracy 100%, normal vs DM accuracy 98.2%, drusen vs normal 99%,
    Dla X-Ray:  Binary classifirers: pneumonia vs normal accuracy 92.8%, baterial vs viral 90.7%
    
    W artykule "Detecting Pneumonia in an iOS App with Create ML" również użyto klasyfikacji.
    

## siim-covid-19

https://osf.io/532ek/
link do artykułu

1. Podstawowe informacje o bazie danych: rok powstania, źródła danych, liczba danych itp.

    Baza zawiera 10 178 wybranych losowo z szerszej grupy zdjęć X-ray klatki piersiowej, po wcześniejszym odsianiu tych, które nie mają dołączonego pliku dicom, czy tych z niewłaściwą lateralizacją. zebrane z dwóch publicznych źródeł: `MIDRC-RICORD` oraz `BIMCV`. W bazie są zdjęcia chorych na `bacterial pneumonia`, `cardiogenic pulmonary edema`, `pleural effusion`, `atelectasis`, `nodule/mass`, `interstitial lung disease`, and `pneumothorax`.   

    Wszystkie dane i metadane do diagnostyki obrazowej zostały de-identyfikowane przed ich dostarczeniem do tej bazy danych, mamy podział na płeć.  

    W bazie 22% pacjentów chorych na Covid-19 nie wykazywało żadnych oznak zapalenia płuc, 48% pacjentów z negatywnym wynikiem testu na Covid-19 miało etykietę `negative for pneumonia`.

2. Jakie istotne informacje są w artykule, a nie widać tego w bazie danych?

    Baza zawiera zdjęcia z widokiem PA i widokiem AP od przodu otrzymane i w sposób radiografii komputerowej (CX) oraz radiografii cyfrowej (DX).
etykiety są wzajemnie wykluczające się, by zwiększyć spójność w raportach radiologicznych.

3. Jakie informacje dotyczące bazy danych nie zostały przedstawione w artykule? Czy mogło to być zrobione specjalnie? Uzasadnij.

    Są zdjęcia tego samego pacjenta, które wyglądają identycznie - nie różnią się ani jednym pikselem, natomiast w jednym takim przypadku który badałem, jedno z dziewięciu zdjęć ma inne etykiety niż pozostałe, nie wiem właściwie dlaczego tak jest.

4. Jakie artykuły korzystały z tej bazy danych? Jakie zadania były wykonywane (klasyfikacja, segmentacja, detekcja itp.)? Jakie wyniki trenowania zostały osiągnięte (jeśli nie była to jedyna baza danych, to wypisz inne tak, by dało się je zidentyfikować)?

    W konkursie na Kaggle baza danych wykorzystywana była do detekcji, nie znalazłem innych jej użyć.

## Luna-16

https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI#1966254f633413761b746ff9e49dd8f0d5b679d  
https://luna16.grand-challenge.org/Home/  

1. Podstawowe informacje o bazie danych: rok powstania, źródła danych, liczba danych itp.

    Baza danych o nazwie `LIDC-IDRI` zawiera kolekcję skanów tomograficznych klatek piersiowych.  
    Skany posiadają oznaczone uszkodzenia. Przeznaczona do wykrywania raka płuc. 
    1018 przypadków w bazie danych, każdy zawiera zdjęcia skanu z wykorzystaniem tomografa komputerowego, z dołączonym plikiem XML rejestrującym proces annotowania zdjęcia.  
    Baza zawiera łącznie 244,527 zdjęć.  
    Pierwsze wersje "testowe" tej bazy odbywały się w czerwcu 2011 roku, opublikowano wtedy pierwsze 399 przypadków, z kiedy pochodzą dane - nie znalazłem
        
2. Jakie istotne informacje są w artykule, a nie widać tego w bazie danych?

    mamy dwie ramki .csv dotyczące kandydatów na guzy, dopóki nie przeczyta się artykułu, w którym można wyczytać, że druga ramka `candidates_v2.csv` została dodana w celu redukcji fałszywych pozytywów. zawiera ona tych samych kandydatów, i więcej.
    
3. Jakie informacje dotyczące bazy danych nie zostały przedstawione w artykule? Czy mogło to być zrobione specjalnie? Uzasadnij.

    Poza zdjęciami, zbyt wielu informacji w bazie danych nie mamy.

4. Jakie artykuły korzystały z tej bazy danych? Jakie zadania były wykonywane (klasyfikacja, segmentacja, detekcja itp.)? Jakie wyniki trenowania zostały osiągnięte (jeśli nie była to jedyna baza danych, to wypisz inne tak, by dało się je zidentyfikować)?


    http://ijdri.com/ijbbe/2017/a202010-048.pdf - detekcja z wykorzystaniem sieci neuronowych - udało się wykrywać raka płuc w 86.6% przypadków. Wykorzystano inną bazę danych(https://www.kaggle.com/c/data-science-bowl-2017), która okazała się jednak nieadekwatna, żeby odpowiednio sklasyfikować zestaw walidacyjny.
    
    
    
