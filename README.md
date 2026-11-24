# Simulatore d'esame

Simulatore per gli esami a risposta multipla e aperta a partire dal **paniere** del corso (il PDF delle domande fornito dall'ateneo). È una sola pagina HTML: si apre nel browser, senza installare nulla.

## Cosa fa

- Legge il PDF del paniere ed estrae lezioni, domande chiuse e domande aperte.
- Crea prove come all'esame eCampus (24 domande a risposta multipla e 2 aperte), con o senza tempo limite, più le modalità **ripasso errori** e **allenamento**.
- Alla consegna la prova si fa correggere da Gemini (o da un altro chatbot) con un copia e incolla, oppure si corregge a mano. Le risposte corrette vengono ricordate per le prove successive.
- Statistiche: andamento dei voti e risposte giuste per lezione.
- Mappa concettuale del corso, costruita blocco per blocco.
- Esportazione del paniere in Markdown e backup completo in JSON.

## Privacy

Panieri, voti e statistiche restano **solo nel browser** di chi usa la pagina (IndexedDB). Nessun dato viene inviato a un server. Per spostarli su un altro computer si usa «Esporta backup» / «Importa backup».

## Avvertenze

- Strumento personale di studio, **non affiliato** con eCampus né con altri atenei.
- Le correzioni fatte da un chatbot possono contenere errori: ogni voto resta modificabile.
- I panieri non sono inclusi nel repository: ognuno carica il proprio.
