This repository is [my](https://github.com/Naereen/) fork of [James Powell's](https://github.com/dutc/) [battlegame](https://github.com/dutc/battlegame) challenge.

## About the challenge
- The [explainations about the game](Instructions.md) are copied from his repository.

## About my solution
- You can find my solutions here: [`battleserver.py`](battleserver.py) and [`battleplayer.py`](battleplayer.py).
- My "server" script implements perfectly what was asked by the exercise, and my "client" script implements a quite naive heuristic: it plays randomly and only tries to keep hitting a ship when it first hit it (my experiments showed it wins in about 60% to 75% lesser number of plays in comparison to the naive purely uniform strategy).
- Both scripts [stand on the shoulder on giants](https://en.wikipedia.org/wiki/Standing_on_the_shoulders_of_giants): [the Python standard library](https://docs.python.org/3/) (`sys`, `string.ascii_uppercase`, `collections.OrderedDict`, `pprint.pprint`), [the Numpy package](http://www.numpy.org/) and the :sparkles: awesome [docopt package](https://github.com/docopt/docopt) for command-line handling. (see [reqirements.txt](requirements.txt)).

----

> TODO

## Examples

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
