---
description: >-
  Conviction Voting wird verwendet, um die Verteilung von Honey aus dem
  gemeinsamen Pool zu regulieren.
---

# Verteilung

## Conviction Voting

Mit Conviction Voting können Vorschläge kontinuierlich und gleichzeitig erstellt und geprüft werden. Die Teilnehmer können ihre Präferenzen für die von ihnen unterstützten Vorschläge angeben, aber sie können ihren Einfluss nicht auf mehrere Vorschläge „doppelt zählen“.   
  
Wenn sie anfangen, einen Vorschlag zu unterstützen, gilt die Unterstützung \(als Conviction bezeichnet\) nicht sofort, sondern muss sich im Laufe der Zeit entsprechend einer exponentiellen Abklingfunktion oder Halbwertszeit aufladen.   
  
Derzeit gibt es zwei Arten von Vorschlägen, die sich auf die Verteilung von Honey auswirken: Signaling-Vorschläge, bei denen kein Honey angefordert wird, und Finanzierungsvorschläge, bei denen Honey angefordert wird.

Für Finanzierungsvorschläge gibt es eine Ausführungsschwelle, die auf der Grundlage des Anteils der beantragten Mittel an den im Gemeinschaftspool verfügbaren Mitteln festgelegt wird. Je größer der Anteil, desto größer der erforderliche Schwellenwert.  
  
Schauen Sie sich dieses [cadCAD-Modell](%20https://github.com/BlockScience/Aragon_Conviction_Voting) an, um den Mechanismus genauer zu untersuchen.  
  
Die von 1Hive verwendete Implementierung des Conviction-Votings wurde in Zusammenarbeit mit [Aragon](%20https://aragon.org/), [Commons Stack](%20https://commonsstack.org/) und [Block Science](%20https://block.science/) entwickelt.

