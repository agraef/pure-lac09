
Pure LAC09 Examples
===================

Git repository: https://github.com/agraef/pure-lac09

You need to have [Pd] (0.43+), [Pure] (0.18+) and the [pd-pure] plugin (0.4+)
installed to run these examples. The `waveplay` patch also requires
[libsndfile], the `bounce` patch needs [Gem].

[Pd]:         http://crca.ucsd.edu/~msp/
[Pure]:       http://pure-lang.googlecode.com
[pd-pure]:    http://code.google.com/p/pure-lang/wiki/Addons#pd-pure
[Gem]:        http://gem.iem.at
[libsndfile]: http://www.mega-nerd.com/libsndfile/

Pd and libsndfile are readily available on most Linux systems. Gem you may
have to compile from source, but it's also included in some distributions of
Pd, such as [Pd-l2ork] and [Purr Data]. Arch and Ubuntu packages for Pure and
pd-pure can be found on the [Pure website], but are also easy to install from
source.

[Pd-l2ork]: http://l2ork.music.vt.edu/main/make-your-own-l2ork/software/
[Purr Data]: https://git.purrdata.net/jwilkes/purr-data
[Pure website]: https://purelang.bitbucket.io/

waveplay.pd
-----------

A simple soundfile player. The accompanying Pure script is in wavefile.pure.
Run this is as `pd -lib pure waveplay.pd` and push the toggle button to
play. You might have to adjust the window size to get rid of dropouts.

bounce.pd + bounce-sound.pd
---------------------------

A bouncing ball animation. Run as `pd -noaudio -lib pure -lib Gem bounce.pd`.
First push the "Graphics window" toggle to start rendering, then the "Bouncing
ball animation" toggle to start the animation.

The second patch adds some sound effects. Run this as `pd bounce-sound.pd` and
push the toggle above the `pd sound` subpatch in the main patch to connect the
two patches. (These are in two separate patches connected via netsend/
netreceive to prevent audio dropouts, see the Gem FAQ for details.)

Try the different acceleration values (corresponding to the gravity of the
[Moon], [Earth] and [Jupiter]). You can also click inside the Gem window to
restart the animation at different positions.

[Moon]:    http://en.wikipedia.org/wiki/Moon
[Earth]:   http://en.wikipedia.org/wiki/Earth
[Jupiter]: http://en.wikipedia.org/wiki/Jupiter

The Pure script implementing the motion of the ball is in ball.pure.
