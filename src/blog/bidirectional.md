# Bidirectional versioning

Sometimes a dependency doesn't work as expected. A common solution is trying
earlier versions.

[SemVer] does not help with this: the only thing it really guarantees
is that going from `X.Y1.Z1` to `X.Y2.Z2` is safe for `Y1.Z1 > Y2.Z2`.
It says nothing about going in the reverse direction.

Luckily [SemVer] uses more numbers than strictly necessary: MINOR and PATCH
could be the same number. ([ComVer] actually does just that by ignoring
PATCH number completely, only ever incrementing MAJOR and MINOR.)

[SemVer] MAJOR number is only incremented for backwards-incompatible changes.
My proposal is that MINOR number is only incremented for *forward-incompatible*
changes. PATCH is left for changes that are backwards and forward compatible.

In other words, this means that added features should always increment MINOR
while removed features should always increment MAJOR. Or that it's always
safe to move a dependency to a later MAJOR or to an **earlier** MINOR.

Like [ComVer], this scheme is a subset of [SemVer]. The main difference is that
MINOR should not be reset to 0 when MAJOR is incremented: that would imply
forward-compatibility with ALL previous versions.

[SemVer]: https://semver.org/
[ComVer]: https://gitlab.com/staltz/comver
