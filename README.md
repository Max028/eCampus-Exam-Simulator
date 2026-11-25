# Simulatore d'esame

Simulatore per gli esami a risposta multipla e aperta a partire dal **paniere** del corso (il PDF delle domande fornito dall'ateneo). È una sola pagina HTML: si apre nel browser, senza installare nulla.

**▶ [Prova il simulatore](https://max028.github.io/eCampus-Exam-Simulator/)** · hai un account Claude? Usa la [versione su claude.ai](https://claude.ai/artifact/82WfSbLV5ZHPM3FW9whLbn), con correzione automatica e mappe concettuali.

## Come è nato

Per prepararmi agli esami provavo a farmi fare delle simulazioni da Gemini, caricando il paniere del corso. Il risultato era frustrante: a volte non riusciva nemmeno ad analizzare il PDF, altre volte non capiva cosa gli stessi chiedendo, e spesso inseriva nella prova domande che nel paniere non esistevano.

Così ho deciso di costruire uno strumento che facesse una cosa sola, ma bene: leggere il paniere vero e proprio, estrarre tutte le domande così come sono, e creare prove con lo stesso formato dell'esame. Il chatbot interviene solo dopo, per correggere, e su domande che vengono davvero dal paniere. Il simulatore è stato sviluppato con l'aiuto di Claude.

## Cosa fa

- Legge il PDF del paniere ed estrae lezioni, domande chiuse e domande aperte.
- Crea prove come all'esame eCampus (24 domande a risposta multipla e 2 aperte), con o senza tempo limite, più le modalità **ripasso errori** e **allenamento**.
- Alla consegna la prova si fa correggere da Gemini (o da un altro chatbot) con un copia e incolla, oppure si corregge a mano. Le risposte corrette vengono ricordate per le prove successive.
- Statistiche: andamento dei voti e risposte giuste per lezione.
- Mappa concettuale del corso, costruita blocco per blocco.
- Esportazione del paniere in Markdown e backup completo in JSON.

## Privacy

- **Nessun dato raccolto.** Panieri, voti, statistiche e risposte salvate restano **solo nel browser** di chi usa la pagina (IndexedDB): nessun dato viene inviato a un server. Per spostarli su un altro computer si usa «Esporta backup» / «Importa backup».
- **Nessun cookie né tracciamento.**
- **Nessun server esterno.** Caratteri e librerie sono inclusi nel repository e serviti da GitHub Pages: aprendo il sito non viene contattato nessun altro server. GitHub, come ogni hosting, registra i dati tecnici delle visite.
- **Chatbot solo su richiesta.** I contenuti vengono inviati a Gemini o a Claude solo se l'utente sceglie di farlo.

## Avvertenze

- **Progetto indipendente**: non è affiliato, approvato o collegato in alcun modo a eCampus né ad altre università. È stato realizzato con il solo scopo educativo e senza fini di lucro.
- Le correzioni fatte da un chatbot possono contenere errori: ogni voto resta modificabile.
- I panieri non sono inclusi nel repository: ognuno carica il proprio.

## Componenti di terze parti

- [pdf.js](https://github.com/mozilla/pdf.js) 4.10.38 di Mozilla, licenza Apache 2.0: `vendor/pdfjs/`
- Caratteri Public Sans, Source Serif 4, Bricolage Grotesque e JetBrains Mono, licenza SIL Open Font License 1.1 (pacchetti Fontsource): `vendor/fonts/`

Le licenze originali sono incluse nelle rispettive cartelle.

## Licenza

Codice distribuito con licenza [MIT](LICENSE): puoi usarlo, modificarlo e ridistribuirlo, mantenendo la nota di copyright. Il software è fornito «così com'è», senza garanzie.
