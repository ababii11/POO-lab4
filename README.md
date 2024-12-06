# POO-lab4
# Simulare Ecosistem

Acest proiect reprezintă o simulare a unui ecosistem în care diferite tipuri de organisme interacționează într-un mediu virtual. Scopul este de a modela dinamica dintre vegetație, consumatori de plante și consumatori de carne prin clase și interacțiuni definite în Python.

# Structura proiectului

Module:
organisme.organism:
Definiția clasei abstracte Organism care servește drept bază pentru toate organismele din simulare.
organisme.vegetatie:
Clasa Vegetatie care reprezintă organismele vegetale din mediu. Acestea pot crește sau se pot reproduce.
organisme.creatura:
Clasele Creatura, ConsumatorPlante și ConsumatorCarne care reprezintă diferitele tipuri de creaturi din ecosistem:
ConsumatorPlante: Consumatoare de vegetație.
ConsumatorCarne: Consumatoare de alte creaturi.
mediu.mediu:
Clasa Mediu care gestionează organismele și dinamica lor în spațiul virtual.
# Exemplu de utilizare:
Fișierul principal execută o simulare cu un mediu predefinit, adăugând organisme și iterând pașii simulării.
Funcționalități
Simulare dinamică:
Organismele pot să se deplaseze, să se hrĂnească și să interacționeze în funcție de tipul lor.
Mediu virtual:
Dimensiuni personalizabile pentru spațiul de simulare.
Extensibilitate:
Posibilitatea de a adăuga noi tipuri de organisme sau comportamente prin extinderea claselor existente.
# Exemple de cod
from mediu.mediu import Mediu
from organisme.vegetatie import Vegetatie
from organisme.creatura import ConsumatorPlante, ConsumatorCarne

mediu = Mediu((10, 10))
mediu.adauga(Vegetatie("Iarba", 10, (1, 1)))
mediu.adauga(ConsumatorPlante("Iepure", 20, (1, 1), 2))
mediu.adauga(ConsumatorCarne("Lup", 30, (2, 2), 3))

mediu.simuleaza(5)
Crearea unui mediu și adăugarea de organisme:
