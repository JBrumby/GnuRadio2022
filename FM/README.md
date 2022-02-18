Dies ist ein ausfühlrich dokumentierter Quellcode für 
Gnu Radio.

Ich lerne mit Gnu Radio umzugehen. 

Die eingfügten Kommentar sind ohne jede Gewähr und spiegeln nur mein
mangelshaftes Verständnis wieder.

der Code funtkioniert mit: 

- ADALM Pluto 
- RTL-SDR
- HackRF (Es gab ein Problem mit der Verstärkung und mit der Frequenzgenauigkeit), deshalb hat bi mir gnuradio nie funktioniert.)

unter:
GnuRadio 3.9.5

auf einem Raspberry Pi 400.

Vielleicht hilft es einem anderen

Viel Spaß damit!

Fazit der bisherigen Eperimente
================================

für meinen HackRF gilt:
-----------------------
jegliche Grundlagenschaltungen für den hackRF sind sinnlos, wenn der Hinweis auf 
- die fehlende AGC fehlt 
- und darausfolgend der Hinweis, dass die if-Gain und bb-gain experimentell eingestellt werden müssen. Bei meinen 
Experimenten ist die rf-Gain bisher ohne Bedeutung.
- Wenn die Gain zu hoch eingestllt ist schwingt der rf-Verstärker, das Ergebnis ist dasselbe wie kein Empfang. Man sieht
nichts im Waterfall und es rauscht nur, als ob das Band leer ist.
- Der DC-Spike muss mit einem Block "IQ-Correction" beseitigt werden, weil sonst der Empfänger zugestopft ist.

für meinen Pluto gilt: 
-----------------------
Er funktioniert einfach mit der Grundschlatung und deshalb mit einem Primitiv-Empfangskonzept.

für meinen rtl-sdr gilt; 
------------------------
Erfunktioniert einfach mit der Grundschaltung und deshalb in menem Primitiv-Empfnagskonzept