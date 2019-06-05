# gym-fightingice

Unoffical gym API for game FightingICE.


See http://www.ice.ci.ritsumei.ac.jp/~ftgaic/ for more information about FightingICE and the AI Competition.

4 envs can be used:

FightingiceDataNoFrameskip-v0 <br />
FightingiceDataFrameskip-v0 <br />
FightingiceDisplayNoFrameskip-v0 <br />
FightingiceDisplayFrameskip-v0

In env with mark "Data", a vector from game data with 15 frames delay is returned for obs. <br />
In env with mark "Display" a ndarray with no frame delay is returned for obs. But it run slower. <br />
In env with mark "Frameskip", after one step called, obs after the action finished will be returned, frames before AI can control will be skipped. <br />

And env FightingiceEnv_TwoPlayer is only for development.

# Requirement

gym to make env. Simplely run
```bash
$ pip install gym
```
Or see gym official https://gym.openai.com/ and github https://github.com/openai/gym for more information.
<br /><br />

Java and py4j to run FightingICE java version. Please install java by yourself, for py4j, run
```bash
$ pip install py4j
``` 
<br />

port_for to select port if need, run
```bash
$ pip install port_for
``` 
<br />

opencv for python to get display obs if need
```bash
$ pip install opencv-python
``` 
<br /><br />

# Install
First, run
```bash
$ pip install -e .
```
Then, <br />
Download FightingICE from http://www.ice.ci.ritsumei.ac.jp/~ftgaic/index-2.html and extract to one folder. <br />
Set java_env_path when call gym.make() or start your script in the FightingICE installed path or just change the defualt value in the source code.
