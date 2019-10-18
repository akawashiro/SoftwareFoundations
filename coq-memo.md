- `inversion`
  Destruct hypothesis.
```coq
S n = 0
```
  If you use `inversion` for this, it reduce to contradiction and goal is proved.
- `unfold`
  Unfold
```coq
not P ===> P -> bottom
```
