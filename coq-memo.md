- `inversion`
  Destruct hypothesis.
```coq
S n = 0
```
  If you use `inversion` for this, it reduce to contradiction and goal is proved.
- `unfold`
  Unfold definition.
```coq
not P = P -> bottom
```
- `split`
  You can use `split` tactics not only `and` but also a goal constructed with
  `C` of type `X1 -> X2 -> ... -> Xn -> P`. In that case, you can prove `P`
  by prove `X1, X2, ..., Xn`.
- `left`, `right`
  left, rightはorのみではなく、2つのコンストラクタC : X1 -> X2 -> .. -> Xn ->
  PとD : Y1 -> Y2 -> .. -> Ym -> P からなる任意のゴールPに対して扱うことができ、
  leftの場合は1つめのコンストラクタ、rightの場合は2つめのコンストラクタのすべて
  の引数について証明を行うことで、ゴールPを証明できます。
- SPC m s
  Find a theorem.
  - I want to seach by symbols.
- `eapply`
  `apply`と一緒だが`apply`を適用して決定しなかった変数を存在変数(existential variable)
  としておいておいてくれる。
- `generalize dependent`
  Generalize a variable which is declared in hypothesis.
- `induction`
  Induction on structures. Apply on hypothesis or variable.
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
- `destruct boolean`
  Case analysis on `boolean`
- `unfold`と`fold`を使って関数をちょっと展開して計算した後に畳み込み直せる
- `SPC m p`
  Print the definition
- `C-c C-a C-a`
  SearchAbout
- `Proof with auto` or `Proof with eauto`
  証明の最初の部分を Proof ではなく Proof with (tactic) で始めると、証明の本体部分でタクティックの後に . と書く代わりに ... と書くことで、そのタクティックで生成されたサブゴールすべてを tactic で解くようにすることができます（解けなかった場合には失敗します）。 
- `False_ind`
  forall P. P -> bottom
- You should induction on relation rather than induction on terms.
