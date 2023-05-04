# Playing Flappy Bird with DQN, Double DQN, Duel DQN, and DQN with prioritized experience replay
![image](https://github.com/AlbertSun0930/Playing-Flappy-Bird-with-DQN-Double-DQN-Duel-DQN-and-DQN-with-prioritized-experience-replay/blob/main/duration/GIF%202023-5-2%2017-13-46.gif)


In this project we adopt the original DQN code from [cite](https://github.com/hardlyrichie/pytorch-flappy-bird). We use cuda to achieve much faster convergence.   We also implement 4 algorithms combined with DQN by ourselves, i.e, double-DQN, prioritized experience replay, dueling network architecture and integration of them.  


Performance
--------------------------------
We stop training when the current game can be played for more than 600 steps, and the past 100 games can be played for more than 300 steps on average. Below is the line chart of average model performance.

![image](https://github.com/AlbertSun0930/Playing-Flappy-Bird-with-DQN-and-improvements/blob/main/duration/comprison%20of%20algorithms.png)

<img src="https://github.com/AlbertSun0930/Playing-Flappy-Bird-with-DQN-and-improvements/blob/main/duration/comprison%20of%20algorithms.png" width="10px">


Getting started
--------------------------------

To get models to start training run:

```
python DQN.py train
python PriDQN.py train
python DoubleDQN.py train
python DuelDQN.py train
python PriDoubleDuelDQN.py train
```

To test models:

We have save neural network parameters of the PriDoubleDuelDQN model. You can test it by runing:  
```
python PriDoubleDuelDQN.py test
```

For others, you need to train the models first and get convergence. Then you can run the following codes for testing:
```
python PriDQN.py test
python DoubleDQN.py test
python DuelDQN.py test
python DQN.py test
```
