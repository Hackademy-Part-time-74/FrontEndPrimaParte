git è un     distributed     version control system

un version control system uno strumento utile per tenere traccia di come uno stesso progetto evolve nel tempo
distributed cioè utile per lavorare in team


Solo chi ha il Mac deve installare questo da terminale:
xcode-select --install



# Configurazione iniziale a livello di sistema operativo
git config --global user.name "Eric Cartman"
git config --global user.email "eric.cartman@gmail.com"



# Parole chiave
- repository un contenitore di dati utili a tenere traccia di come uno stesso progetto evolve nel tempo. Una repository è formata da una o più branch
- branch una linea di sviluppo nel tempo (un asse del tempo). Un branch è formato da uno o più commit.
- commit istantanea del progetto (il backup)


Ogni progetto ha la sua repository
il comando git init è utile inizializzare una nuova repository locale


La directory del progetto è la working directory
La staging area è una anteprima del commit. Possiamo visualizzare lo stato della staging area eseguendo git status

Procedura per usare git:
1) eseguo il comando git init (operazione one time) una sola volta a inizio progetto

2) scrivo codice
3) inserisco i file presenti nella working directory all'interno della staging area eseguendo git add .
4) a partire dai file presenti nella staging area creiamo un nuovo commit eseguendo git commit -m "qui descrizione del commit"
5) git push origin main

2) scrivo codice
3) inserisco i file presenti nella working directory all'interno della staging area eseguendo git add .
4) a partire dai file presenti nella staging area creiamo un nuovo commit eseguendo git commit -m "qui descrizione del commit"
5) git push origin main

2) scrivo codice
3) inserisco i file presenti nella working directory all'interno della staging area eseguendo git add .
4) a partire dai file presenti nella staging area creiamo un nuovo commit eseguendo git commit -m "qui descrizione del commit"
5) git push origin main


Per visualizzare la lista dei commit eseguiamo il comando git log oppure in modo più sintetico git log --oneline





GitHub è un servizio di hosting per repository git remote
Dobbiamo prima di tutto collegare:
- l'utente attualmente loggato sul sistema operativo
- con l'account su GitHub

creando una coppia di chiavi privata e pubblica eseguendo ssh-keygen


Il comando seguente rinomina il branch da master a main:
git branch -M main



Il comando git remote collega la repository locale con la corrispondente repository remota conoscendo l'URL di quest'ultima
origin è un alias per l'url della repository remota
git remote add origin URLDellaRepositoryRemota

git remote set-url origin URLDellaRepositoryRemota




Il comando git push effettua l'upload dei commits presenti nel branch main della repository locale verso il branch main della repository remota che si trova a origin
git push origin main


Il comando git pull effettua il download dei commits presenti nel branch main della repository remota che si trova a origin verso il branch main della repository locale 
git pull origin main



Il collaborator che si aggiunge allo sviluppo di un progetto già esistente:
1) git clone URLDellaRepositoryRemota (operazione one time)





In generale, git prova a risolvere automaticamente il conflitto:
- se ci dovesse riuscire vi verrà chiesto di inserire solo il messaggio di risoluzione del commit con conseguente creazione di un commit automatico
- se non ci dovesse riuscire guarda dopo

Se dovesse nascere un conflitto:
1) saranno mostrati dei delimitatori per le parti di codice in conflitto
2) scelgo cosa tenere e cosa no cancellando i delimitatori
3) termino la risoluzione del conflitto con un nuovo "commit di risoluzione del conflitto"

