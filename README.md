# Atari_Games_Reinforcement_Learning

## Introduzione
Questa guida ha lo scopo di illustrare i passi necessari per permettere ad un agente di [Reinforcement Learning](https://it.wikipedia.org/wiki/Apprendimento_per_rinforzo) di imparare a giocare a diversi giochi dell'Atari 2600.  
L'argomento sarà parte del talk, curato dal professore Fabio Stella, intitolato **"Come lavorare sui dati: i linguaggi per la machine intelligence"** che si terrà in data 21 dicembre 2018 presso l'Università degli Studi di Milano-Bicocca.  
![alt text](https://www.frenkowski.it/wp-content/uploads/2018/12/pm.gif)



### Prerequisiti
Scaricare e installare [Anaconda (Python 3.7 version)](https://www.anaconda.com/download/).  
Scaricare e scompattare il contenuto della repository attuale, come mostrato in figura.  

![alt text](https://www.frenkowski.it/wp-content/uploads/2018/12/t2_n.jpeg)

## Ambiente 
Aprire Anaconda Navigator e creare un nuovo ambiente che ospiterà [Tensorflow](https://www.tensorflow.org/).  
Questo può essere fatto:
### via Anaconda Navigator
```
Environments > Create 
```
Impostare **"tensorflow"** come nome e scegliere **Python 3.6** come Packages
   
   
## Preparazione
Selezionare, da Environments, tensorflow e aprire il terminale come mostrato nella seguente figura. 
![alt text](https://www.frenkowski.it/wp-content/uploads/2018/12/play.png)

Se tutto è andato a buon fine avrete (tensorflow) seguito da un percorso (ad esempio C:\Users\ponti\) all'inizio del vostro terminale. 
![alt text](https://www.frenkowski.it/wp-content/uploads/2018/12/t1.jpeg)

Creare una nuova cartella nel percorso indicato di fianco a (tensorflow) nel terminale e rinominarla "Gym".           
Copiare i file "Gym.py" e "Load_Model.py", scaricati in precedenza dalla repository, all'interno della cartella Gym. 
Da terminale, spostarsi all'interno della cartella Gym con il seguente comando:
```
cd gym
```
![alt text](https://www.frenkowski.it/wp-content/uploads/2018/12/t3.jpeg)


## Packages
A questo punto dare il seguente comando al terminale:
```
pip install tensorflow
```

Prima di poter procedere al training è necessario installare dei packages specifici.                   
Procedere quindi con i seguenti comandi:
```
pip install gym
```
```
pip install gym[atari]
```
![alt text](https://www.frenkowski.it/wp-content/uploads/2018/12/t4.jpeg)

In caso questo comando restituisca un errore, provare il comando seguente: 
```
pip install --no-index -f https://github.com/Kojoley/atari-py/releases atari_py
```
e procedere con:
```
pip install matplotlib
pip install scikit-image
```


## Training
Ora è possibile allenare il nostro agente di Reinforcement Learning in modo che impari a giocare a **Pacman**.              
Rimandendo nel terminale relativo all'ambiente "tensorflow" dare il seguente comando:
```
python Gym.py
```
L'agente procederà ora al training. Dopo aver raggiunto un determinato numero di iterazioni sarà mostrato a video il nostro agente di Reinforcement Learning mentre proverà a giocare.                  
Con l'aumentare delle iterazioni si potrà notare un incremento delle prestazioni.



## Testing
Una volta finito il training si può procedere a testare il modello relativo al precedente training.
Sempre da terminale dare il seguente comando:
```
python Load_Model.py
```
Verrà mostrato a video il nostro agente mentre giocherà a 100 partite di Pacman, al termine del quale si avrà lo score medio finale.


## Consigli
* Per ottenere delle perfomance migliori è consigliabile installare [Tensorflow con il supporto alla GPU](https://www.quantinsti.com/blog/install-tensorflow-gpu)
* Per aver un tempo di training inferiore si può ridurre il valore della variabile **n_steps**, nel file Gym.py (magari passando da 1000000 a 250000)
* Per evitare l'attesa, dovuta ai tempi di training, è possibile provare il modello già allenato. Copiare la cartella "MsPacman", disponibile nella repository scaricata in precedenza, all'interno della cartella "Gym" e passare direttamente alla fase di testing   

* Possono essere provati altri giochi dell'Atari, la lista completa è disponibile sulla documentazione ufficiale [Gym](https://gym.openai.com/envs/#atari). Per esempio, nel file "Gym.py", provare a modificare il valore della variabile **game = "SpaceInvaders"**


## Riferimenti
* [Deep_Reinforcement_Learning-Atari](https://github.com/ykteh93/Deep_Reinforcement_Learning-Atari)
* [Beat Atari with Deep Reinforcement Learning!](https://becominghuman.ai/lets-build-an-atari-ai-part-0-intro-to-rl-9b2c5336e0ec)


## Ringraziamenti
* Il professor [Fabio Stella](https://www.unimib.it/fabio-antonio-stella)
* I miei compagni di corso, Andrea Ponti, Simone Rizza e Edoardo Silva. 

In caso di consigli, dubbi o problemi è possibile contattarmi via email all'indirizzo [frenkowski@gmail.com](mailto:frenkowski@gmail.com). 
