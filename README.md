# 42 ft_irc


<h3> Italiano 🇮🇹</h3>

Il progetto consiste nello sviluppare un server IRC in C++98. L'obiettivo principale è creare un server in grado di gestire contemporaneamente più client senza mai bloccarsi. Il programma prende in input il numero di una porta e la password per connettersi al server, in ascolto sulla porta specificata. La comunicazione tra i client e il server avverrà tramite TCP/IP (v4 o v6), in questo caso v4. Nel progetto è fondamentale utilizzare operazioni di I/O non bloccanti e implementare la funzione poll().

È necessario ricreare varie funzionalità di IRC, tra cui:

- Autenticazione: I client dovranno autenticarsi con un nickname e un username, dopo aver inserito la giusta password.
- Operazioni sui canali: I client potranno unirsi a dei canali, inviare e ricevere messaggi privati. Tutti i messaggi inviati da un client su un canale dovranno essere inoltrati agli altri client presenti nello stesso canale.
- Tipi di utente: Il server dovrà distinguere utenti normali da operatori.
- Comandi degli operatori dei canali: KICK (espellere un client dal canale), INVITE (invitare un client a unirsi a un canale), TOPIC (cambiare o visualizzare il topic del canale) e MODE (modificare la modalità del canale, in particolare +-i, +-k ,+-l, +-t, +-o).
- DCC: condivisione di file.
- Bot: creazione di un bot.

Durante il corso del progetto, è possibile acquisire diverse competenze, tra cui:

- Programmazione in C++98: Il progetto richiede l'utilizzo del linguaggio C++98, che implica rispettare la sintassi e le funzionalità disponibili in questa versione del linguaggio.    Concetti di networking: Comprendere la comunicazione TCP/IP, le socket e la gestione simultanea di più client è fondamentale per la creazione di un server IRC.
- I/O non bloccante: Implementare file descriptor non bloccanti utilizzando la funzione "poll" (o il suo equivalente) aiuta a evitare operazioni bloccanti e garantisce che il server rimanga reattivo.
- Gestione degli errori: Il progetto richiede un'ampia fase di testing per gestire varie possibili situazioni di errore in modo appropriato.
- Gestire comandi parziali: Per poter elaborare un comando, è necessario prima aggregare i pacchetti ricevuti per ricostruirlo ed elaborarlo.

Il progetto l'ho sviluppato con @mttmrz e abbiamo scelto konversation come client di riferimento. Il programma funziona interamente con nc, è molto meno intuitivo visto che i messaggi al server devono essere mandati con il formato giusto, in caso di errore saranno ignorati.

-------------------

<h3> English 🇬🇧</h3>

The project consists of developing an IRC server in C++98. The main goal is to create a server capable of handling multiple clients simultaneously without ever blocking. The program takes as input a port number and a password for connecting to the server, listening on the specified port. Communication between clients and the server will take place via TCP/IP (v4 or v6), in this case, v4. It is essential in the project to use non-blocking I/O operations and implement the poll() function.

Various IRC functionalities need to be recreated, including:

- Authentication: Clients must authenticate with a nickname and username after entering the correct password.
- Channel Operations: Clients can join channels, send and receive private messages. All messages sent by a client on a channel should be forwarded to other clients in the same channel.
- User Types: The server must distinguish between regular users and operators.
- Channel Operator Commands: KICK (eject a client from the channel), INVITE (invite a client to join a channel), TOPIC (change or view the channel's topic), and MODE (modify the channel's mode, specifically +-i, +-k, +-l, +-t, +-o).
- DCC: File sharing.
- Bot: Create a bot.

Throughout the course of the project, you can acquire various skills, including:

- C++98 Programming: The project requires using the C++98 language, which involves adhering to the syntax and features available in this version of the language.
- Networking Concepts: Understanding TCP/IP communication, sockets, and handling multiple clients simultaneously is crucial for creating an IRC server.
- Non-blocking I/O: Implementing non-blocking file descriptors using the poll() function (or its equivalent) helps avoid blocking operations and ensures the server remains responsive.
- Error Handling: Extensive testing is necessary to handle various possible error situations appropriately.
- Handling Partial Commands: To process a command, it is necessary to first aggregate the received packets to reconstruct and process it.

I developed this project with @mttmrz, and we chose Konversation as the reference client. The program works entirely with nc, but it is less intuitive since messages to the server must be sent in the correct format; otherwise, they will be ignored.
