Questo progetto ha come obiettivo la realizzazione di un sistema di pedestrian detection basato su LinearSVC, HOG descriptor e PCA. Abbiamo implementato un sistema completo di detection con procedura multi-scale sliding window e non-maxima suppression, confrontando le performance con e senza preprocessing PCA.

Requisiti: Python 3.x , scikit-learn, numpy, matplotlib, opencv-python


File principali: 
  extract_hog.py: Estrazione HOG features
  train_model.py: Addestramento e selezione iperparametri
  sliding_window.py: Implementazione multi-scala
  nms.py: Non-Maxima Suppression
  evaluate.py: Valutazione sul validation/test set
  visualize.py: Visualizzazione risultati con bounding box
  
  
Successi:    Buona rilevazione anche in ambienti affollati (es. 009616.jpg)
             Individuati soggetti che l'OpenCV detector ha ignorato

Fallimenti:  Falsi positivi su strutture lineari (es. finestre, edifici in 005907.jpg)
             Il nostro detector ha mostrato migliori capacità di individuazione di pedoni isolati


Conclusione: Il modello senza PCA mostra performance leggermente superiori, ma entrambi sono comparabili.
             OpenCV tende ad avere meno falsi positivi, ma perde pedoni in zone periferiche.

