This repository is [my](https://github.com/Naereen/) fork of [James Powell's](https://github.com/dutc/) [battlegame](https://github.com/dutc/battlegame) challenge.

## About the challenge
- The [explainations about the game](Instructions.md) are copied from his repository.

## About my solution
- You can find my solutions here: [`battleserver.py`](battleserver.py) and [`battleplayer.py`](battleplayer.py).
- My "server" script implements perfectly what was asked by the exercise, and my "client" script implements a quite naive heuristic: it plays randomly and only tries to keep hitting a ship when it first hit it (my experiments showed it wins in about 60% to 75% lesser number of plays in comparison to the naive purely uniform strategy).
- Both scripts [stand on the shoulder on giants](https://en.wikipedia.org/wiki/Standing_on_the_shoulders_of_giants): [the Python standard library](https://docs.python.org/3/) (`sys`, `string.ascii_uppercase`, `collections.OrderedDict`, `pprint.pprint`), [the Numpy package](http://www.numpy.org/) and the :sparkles: awesome [docopt package](https://github.com/docopt/docopt) for command-line handling. (see [reqirements.txt](requirements.txt)).

----

## Documentation
### Server
```bash
$ ./battleserver.py --help
Battle Server.

Usage:
    battleserver.py [--carrier=<x,y,dir>] [--battleship=<x,y,dir>] [--cruiser=<x,y,dir>] [--submarine=<x,y,dir>] [--destroyer=<x,y,dir>] [--random] [--size=<xy>] (--show | --play)
    battleserver.py (-h | --help)
    battleserver.py --version

Options:
    -h --help       Show this screen.
    --version       Show version.
    --show          Print the board.
    --play          Let you play a "one player" game interactively.
    --size=<xy>     Set size of the board [default: 5,5].
    --random        Set every ship to a random position.
    --carrier=<x,y,dir>     Place ship Carrier at position x,y and direction (h or v) [default: 1,1,h].
    --battleship=<x,y,dir>     Place ship Battleship at position x,y and direction (h or v) [default: 2,1,h].
    --cruiser=<x,y,dir>     Place ship cRuiser at position x,y and direction (h or v) [default: 3,1,h].
    --submarine=<x,y,dir>     Place ship Submarine at position x,y and direction (h or v) [default: 4,1,h].
    --destroyer=<x,y,dir>     Place ship Destroyer at position x,y and direction (h or v) [default: 5,1,h].
```

### Client
```bash
$ ./battleplayer.py --help
Battle Client.

Usage:
    battleplayer.py [--delay=<t>] [--smart] [--size=<xy>] [--server_command=<cmd>]
    battleplayer.py (-h | --help)
    battleplayer.py --version

Options:
    -h --help       Show this screen.
    --version       Show version.
    --server_command=<cmd>  Play against a server launched by 'cmd' [default: ./battleserver.py --random --play].
    --size=<xy>     Set size of the board [default: 5,5].
    --delay=<t>     Delay between successive plays, in seconds [default: 0.1].
    --smart         Try to be smart when playing. Experimental.
```

----

## Examples
### Server

- We can see two random 5x5 boards:
```bash
$ ./battleserver.py --random --show
ccccc
bbbb-
srrr-
s-d--
s-d--
$ ./battleserver.py --random --show
ccccc
-brrr
sb---
sbd--
sbd--
```

- We can see a random 7x7 board:
```bash
$ ./battleserver.py --size=7,7 --random --show
----sss
--bbbb-
--ccccc
-------
--rrr--
-dd----
-------
```

### Client
```bash
$ ./battleplayer.py --smart --delay=0
bot: 1,4
board: hit carrier
bot: 0,4
board: miss
bot: 2,4
WARNING: was hitting carrier but now hitting battleship
board: hit battleship
bot: 3,4
WARNING: was hitting carrier but now hitting destroyer
board: hit destroyer
bot: 4,4
board: miss
bot: 1,0
board: hit carrier
bot: 1,1
board: hit carrier
bot: 1,2
board: hit carrier
bot: 1,3
board: sunk carrier
bot: 0,3
board: miss
bot: 3,0
WARNING: was hitting None but sunk destroyer
board: sunk destroyer
bot: 3,1
board: hit cruiser
bot: 0,1
board: hit cruiser
bot: 2,1
WARNING: was hitting cruiser but now hitting battleship
board: hit battleship
bot: 4,1
board: sunk cruiser
bot: 4,2
board: hit submarine
bot: 2,2
WARNING: was hitting submarine but now hitting battleship
board: hit battleship
bot: 3,2
board: hit submarine
bot: 4,0
board: miss
bot: 4,3
board: miss
bot: 0,0
board: miss
bot: 2,0
board: miss
bot: 3,3
board: miss
bot: 2,3
WARNING: was hitting submarine but sunk battleship
board: sunk battleship
bot: 0,2
board: sunk submarine
bot: 0,0
board: you win! in 25 moves
VICTORY!
```

----

### :scroll: License ? [![GitHub license](https://img.shields.io/github/license/Naereen/battlegame.svg)](https://github.com/Naereen/badges/blob/master/LICENSE)
[MIT Licensed](https://lbesson.mit-license.org/) (file [LICENSE](LICENSE)).
© [Lilian Besson](https://GitHub.com/Naereen), 2018.

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/battlegame/graphs/commit-activity)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://GitHub.com/Naereen/ama)
[![Analytics](https://ga-beacon.appspot.com/UA-38514290-17/github.com/Naereen/battlegame/README.md?pixel)](https://GitHub.com/Naereen/battlegame/)

[![ForTheBadge uses-badges](http://ForTheBadge.com/images/badges/uses-badges.svg)](http://ForTheBadge.com)
[![ForTheBadge uses-git](http://ForTheBadge.com/images/badges/uses-git.svg)](https://GitHub.com/)

[![forthebadge made-with-python](https://img.shields.io/badge/Made%20with-python-1abc9c.svg)](https://www.python.org/)
[![ForTheBadge built-with-science](http://ForTheBadge.com/images/badges/built-with-science.svg)](https://GitHub.com/Naereen/)
