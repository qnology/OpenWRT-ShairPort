This is a Git Branch for building ShairPort from GIT feed, based on jlars. To use this:

1. Add "src-git mikejuni git://github.com/mikejuni/packages.git;master" to feeds.conf
2. Remove the jlars feed (to avoid ShairPort conflict)
3. scripts/feeds update -a
4. scripts/feeds install -a

It will install a ShairPort feed that will only need to depend on alsa-lib.
libao dependency is eliminated by a ShairPort fork from Skaman (skaman/shairport).

This package also removes the net and the lang branch which are not useful in OpenWRT.
- Strongswan4 - Replaced by StrongSwan5
- Perl - Not required as ShairPort C works well.
- 
If you've issue with compilation, please raise an issue here.
If it is an issue with playback, please contact the maintainer of ShairPort.
