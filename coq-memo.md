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
- `split`
  splitはandのみではなく、コンストラクタがC : X1 -> X2 -> .. -> Xn ->
  Pという形の任意のゴールPに対して扱うことができ、X1, X2, ..,
  Xnの証明を与えることでPを証明してくれます。
- `left`, `right`
  left, rightはorのみではなく、2つのコンストラクタC : X1 -> X2 -> .. -> Xn ->
  PとD : Y1 -> Y2 -> .. -> Ym -> P からなる任意のゴールPに対して扱うことができ、
  leftの場合は1つめのコンストラクタ、rightの場合は2つめのコンストラクタのすべて
  の引数について証明を行うことで、ゴールPを証明できます。
- SPC m s
  定理を探す
  二文字では検索できないらしい?
  記号で検索したいな
- `eapply`
  `apply`と一緒だが`apply`を適用して決定しなかった変数を存在変数(existential variable)
  としておいておいてくれる。
