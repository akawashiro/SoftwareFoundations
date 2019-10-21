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
- `generalize dependent`
  文脈で仮定した変数を再び全称量化するタクティック
- `induction`
  仮定に対して適用する。構造に関する帰納法
- `rewrite`
  - Rewrite goal with the hypothesis.
  - Usually, it rewrite the left hand side with the right hand side.
    But you can vice versa with `rewrite <-`
  - Can rewrite other hypothesis `Ho` with `in Ho`.
- We can apply a term to a proposition which is generalized by forall.
- `subst`
- Want to know the type of the word under the cursor
  `SPC m ?`
- `destruct`
  Case analysis on a term which is defined using algebraic data type.
- `exists` `term`
  Tell the coq to use `term` in a proposition with existential.
- `destruct` `boolean`
  Case analysis on `boolean`
- `unfold`と`fold`を使って関数をちょっと展開して計算した後に畳み込み直せる
