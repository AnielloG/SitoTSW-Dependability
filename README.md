# 3GVintage - Progetto di Dependability

Questa repository contiene il progetto **3GVintage**, un e-commerce di abbigliamento vintage
di seconda mano, utilizzato come caso di studio per le attività del progetto di **Dependability**.

---

## 1. Specifiche del progetto

Il sistema è stato sviluppato originariamente per il corso di *Tecnologie Software per il Web*
(A.A. 2023/2024, Università degli Studi di Salerno) ed è documentato nel README della
repository originale:

👉 [README del progetto TSW (SitoTSW)](https://github.com/AnielloG/SitoTSW/blob/main/README.md)

Questa repository riprende quel codice come base su cui svolgere le attività richieste
dal progetto di Software Dependability.

---

## 2. Come avviare il sito

### Prerequisiti

- **JDK** (versione compatibile con il progetto, ad esempio 11 o superiore)
- **Apache Tomcat** (versione compatibile con le Servlet usate, ad esempio 9.x)
- **MySQL** (server in esecuzione in locale o raggiungibile in rete)
- Un IDE Java con supporto a Tomcat (Eclipse, IntelliJ IDEA, NetBeans...) oppure la sola
  riga di comando

### Passaggi

1. **Clonare la repository**
   ```bash
   git clone <>
   cd <>
   ```

2. **Creare il database**
    - Avviare MySQL e creare uno schema (ad esempio `3gvintage`).
    - Eseguire lo script SQL presente nella repository (`<.sql>`) per creare
      le tabelle e, se previsto, i dati di esempio.

3. **Configurare le credenziali del database**
   Il progetto si collega a MySQL tramite JDBC. Le credenziali (URL, utente, password) si
   impostano nella classe o nel file di configurazione che crea la connessione, in genere una
   classe di utilità nel package del modello (es. `<percorso/ClasseConnessione.java>`).
   Occorre indicare:
    - **URL** JDBC, ad esempio `jdbc:mysql://localhost:3306/<nome_database>`
    - **Username** dell'utente MySQL
    - **Password** dell'utente MySQL

4. **Configurare Tomcat**
    - *Da IDE*: aggiungere un server Tomcat nelle impostazioni dell'IDE, importare il progetto
      come Dynamic Web Project / progetto Maven (a seconda della struttura) e fare il deploy
      sul server.
    - *Da riga di comando*: generare il file `.war` (ad esempio con `mvn package` se è
      presente il `pom.xml`, oppure esportando il progetto dall'IDE), copiarlo nella cartella
      `webapps` di Tomcat e avviare il server con `bin/startup.sh` (Linux/macOS) o
      `bin\startup.bat` (Windows).

5. **Aprire il sito**
   Con Tomcat attivo, il sito è raggiungibile da browser all'indirizzo: http://localhost:8080/<nome-contesto>/

## 3. Documentazione delle lezioni

Ogni lezione svolta per il progetto di Dependability ha un README dedicato. L'elenco viene
aggiornato man mano che si procede con le richieste.

| # | Lezione / Attività | README |
|---|--------------------|--------|
| 1 | _da definire_ | _link in arrivo_ |
| 2 | _da definire_ | _link in arrivo_ |
| 3 | _da definire_ | _link in arrivo_ |

---
