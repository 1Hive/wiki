---
description: Guadagna Honey per i contributi
---

# Pollen

Pollen è un sistema di contribuzione che riconosce contributi offerti alle community 1Hive su [Discord](https://discord.com/invite/P4rRDUKTAU),[ Forum](https://forum.1hive.org/), e[ Github](https://github.com/1Hive), premiando tali contributi con una distribuzione su base settimanale di Honey.

## **Come posso partecipare**

Non appena inizi ad interagire sulle piattaforme Discord, Forum e Github della community 1Hive stai già guadagnando Pollen, che viene aggiunto al tuo wallet registrato sotto forma di dolce Honey. 

Per ricevere la tua parte di Pollen dovrai creare degli account sulle piattaforme supportate, e collegare questi al tuo indirizzo xDai. Più semplicemente, ti basterà inserire le seguenti informazioni sul canale Discord[ 🐛onboarding](https://discord.gg/eYwxwv4nzk);

```text
#🏵pollen
github: justabee
discourse: justabee
discord: justabee#1234
xDai: 0x0...000
```

Sostituisci `justabee#1234` e `0x0...000` con i tuoi account. Per Discourse si intende il [Forum](https://forum.1hive.org/).

Per ulteriori informazioni, e per comprendere come pollen è calcolato, o per controllare le distribuzioni, [il canale 🏵pollen](https://discord.com/invite/y8fPNcNdAa) su discord è il luogo adatto per tutto ciò.

## **Distribuzione di Pollen** 

La distribuzione di Pollen viene calcolata utilizzando SourceCred per creare ed analizzare un grafico di interazioni tra i membri della community. Sebbene questa non sia una rappresentazione perfetta del valore dei contributi, Pollen può aiutare a premiare quelle interazioni importanti ma troppo granulari per poter creare proposte o creare un nuovo Sciame.

SourceCred monitora tutti i messaggi e i contributi sul Discord, Forum e GitHub, applicando un moltiplicatore a un punteggio base di 1Cred \(credito\) per azione. Una delle fonti primarie per guadagnare Crediti è quando un testo da te scritto \(o un’azione da te effettuata\) è positivamente commentata e recepita degli altri membri, attraverso l’uso delle emojis. Semplicemente mandare messaggi non permette di guadagnare crediti. I pesi per la distribuzione di Cred \(crediti\) sono decisi dalla comunità 1Hive.

I crediti guadagnati all’interno di 1Hive sono utili sono all’interno di 1Hive. Questi non sono punteggi trasferibili, e sono retroattivi; Dunque, anche se ti registrerai dopo aver già iniziato a contribuire, riceverai comunque i crediti per il periodo precedente  \(Ma, logicamente, potrai ricevere il pagamento solo dopo esserti registrato\).

Il [Pollen Explorer](https://1hive.github.io/pollen/#/explorer) ha una classifica degli utenti di Pollen che mostra i crediti guadagnati attraverso il loro impegno con 1Hive.

I pesi che determinando il quantitativo di Pollen guadagnato per ogni azione possono essere trovati nel[ pollen explorer](https://1hive.github.io/pollen/#/explorer) cliccando su “SHOW WEIGHT CONFIGURATION” \(Mostra configurazione peso\).

![](../.gitbook/assets/image%20%288%29.png)

### **Distribuzione Totale**

La somma di Honey distribuita settimanalmente è limitata a $15,000 o 33 Honey qualora il valore di 33 Honey fosse inferiore a $15,000. 5% della distribuzione settimanale va direttamente al team di SourceCred.

![Figura 1. Distribuzione settimanale in Honey calcolata in USD](../.gitbook/assets/image%20%2814%29.png)

### **Tasso di distribuzione**

Il pagamento settimanale è determinato dal contributo recente di un contributore e dal suo contributo totale.

* Il contributo settimanale è il quantitativo di Pollen guadagnato dagli utenti negli ultimi 7 giorni
* Il contributo totale è il quantitativo di Pollen guadagnato dagli utenti fino alla data di distribuzione
* Il tasso di decadimento è la velocità con cui decade il calcolo del contributo totale per ogni settimana precedente. Ad esempio, per un tasso di decadimento del 40%, la settimana precedente è ponderata al 100%, la seconda settimana precedente è ponderata al 60%, la terza settimana precedente è ponderata al 36%, ecc.

| **Parametro di Distribuzione** | **Allocazione & Tasso** |
| :--- | :--- |
| Contributo Settimanale | 25 HNY |
| Contributo Totale | 8 HNY |
| Tasso di Decadimento | 40% |

### **Distribuzione della Piattaforma**

Una ripartizione della distribuzione relativa di ciascuna piattaforma di polline ogni settimana.

| Piattaforma | Percentuale di Distribuzione |
| :--- | :--- |
| GitHub | 30% |
| Discord | 40% |
| Forum | 30% |

### **Calcolo Pollen su Discord**

Sul Discord, per ottenere crediti per altri utenti tramite le risposte emoji, gli utenti devono aver ricevuto qualche credito in passato. Coniare per se stessi non è possibile e il sistema tiene anche in considerazione l'importo del conio per gli altri a seconda di quanto credito ha guadagnato il minatore.

| Total Cred | Mint Weight |
| :--- | :--- |
| 120+ Cred | 1x |
| 90+ Cred | 0.75x |
| 60+ Cred | 0.5x |
| 30+ Cred | 0.25x |
| 0 to 30 Cred | 0x |

Tutti gli emoji danno 1 credito, a parte le eccezioni seguenti.

| Emoji | Mint Weight |
| :--- | :--- |
| 🍯 + `:Honeypot:` \(custom emoji\) | 2x |
| 🐝 + `:Honeybee:` \(custom emoji\) | 2x |
| 💩 | 0x |
| 👎 | 0x |

I canali che danno 0 cred includono: ✅check-in, 🐸memes, 🤖bot-commands, 🕹arcade, 🦩lounge, 🍱kitchen, Fauna e tutti i canali di Informazione

Il canale 🐝marketing fornisce 0.25x il valore del credito standard 

Il canale 🍄nominations fornisce il 95% dei cred per gli users che sono stati taggati nel messaggio. L’utente che posts riceve un 5% The 🍄nominations channel mints 95% of cred for users who have been tagged in messages. Gli utenti che condividono un utente taggato ottengono il 5% di credito per le risposte. Tutti gli utenti taggati condividono il quantitativo di credi in modo uguale.

### **Calcolo Pollen sul Forum**

Sul forum i cred totali che un utente può coniare dipendono dal livello di fiducia  - trust level - dell’utente stesso.

| Trust level | Mint Weight |
| :--- | :--- |
| 4 | 1.5x |
| 3 | 1.25x |
| 2 | 1x |
| 1 | 0.1x |
| 0 | 0x |

## Regole

SourceCred è un software estremamente giovane, e dunque ci sono ancora vari modi per sfruttarlo a proprio beneficio. Tale rischio è stato ridotto da alcuni cambiamenti dei parametri, ma 1Hive ancora impone le regole seguenti, che sono conosciute e monitorate da molti utenti della community.

1. One account per user policy - 1 singolo Account per utente - A ogni utente è concesso l’uso di un solo account. 
2. No reactions/likes trading allowed - Passaggio di reactions/scambi non consentito - Fare accordi con altri utenti di cliccare e commentare positivamente i reciproci posts non è consentito.  Lo scambio di reazioni / mi piace è definito da uno schema di 2 o più utenti che reagiscono reciprocamente alla maggior parte o a tutti i post dell'altro, indipendentemente dalla qualità del contenuto.
3. Bug use / Exploits / Manipulation - Uso di bug / exploit / manipolazione - Qualora ti renda conto che esiste un problema nel sistema, sei pregato di riportarlo immediatamente. Coloro che sfruttano eventuali falle del sistema a proprio vantaggio rischiano una disattivazione dell’account.

## **Links Utili**

Attuali e precedenti [Aggiornamenti ai parametri di Pollen](https://forum.1hive.org/t/updates-to-sourcecred/726).

[Regole Generali](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155) riguardanti Pollen.

[Documentazione SourceCred](https://sourcecred.io/docs/) per ulteriori informazioni.  


