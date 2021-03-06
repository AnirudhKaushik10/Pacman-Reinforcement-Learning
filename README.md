
### True Online Sarsa Lamda playing PowerGrid [lamda = 0.9 and Training episodes = 500] 

![alt text](https://github.com/AnirudhKaushik10/Pacman-Reinforcement-Learning/blob/master/pacman_powerGrid.gif "Logo Title Text 1")




### To run pacman world use the following command

python pacman.py -p TrueOnlineSarsaLamda -a extractor=SimpleExtractor -x 500 -n 550 -l originalClassic


Options:

    -a: Feature extractor = [SimpleExtractor, ImprovedExtractor (works on a n-step truncated bfs and may take time to train)] 
    -l: Map name = [originalClassic, mediumClassic, powerClassic, etc (all maps are available in layouts folder)]
    -p: Agent = [EpisodicSemiGradient, TrueOnlineSarsaLamda, or ApproximateQAgent]
    -x: Number of training episodes
    -n: Number of test episodes
    -q: Quiet Mode without graphics (optional)


### For gridWorld :

python gridworld.py -a q -k 10 -n 0.2 -g MazeGrid -e 0.5 -w 100

Options :

    -a : Agents ( q for q learning, s for sarsa agent, slamda for sarsa lamda agent)
    -n : for noise (probability of taking a random action instead of the intended action)
    -e : for epsilon (epsilon probability for taking a random action while training instead of the greedy action)
    -k : numer of training iterations
    -w : window size
    -g : Grid [BookGrid, BridgeGrid, CliffGrid, MazeGrid] 
    
### Algorithmic Information

TrueOnline SARSA Lambda Agent converges much faster than Approximate Q Agent and Episodic Semi-Gradient SARSA Agent, since each it utilizes eligibilty traces to update the features for all previous steps with a decay factor, rather than only updating the immediate previous step as done in other agents. TrueOnline SARSA Lambda Agent is implemented as given on page number 300 in the book Reinforcement Learning: An Introduction by Sutton & Barto
      
      
      
