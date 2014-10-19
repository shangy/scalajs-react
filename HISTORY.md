History
=======

### 0.5.0

* Documented [most types](https://github.com/japgolly/scalajs-react/blob/master/TYPES.md).
* Just as umounted Scala and JS components are denoted by `ReactComponentU` and `ReactComponentU_` respectively,
  mounted Scala and JS components are now denoted by `ReactComponentM` and `ReactComponentM_`.
* `ReactComponentB` accepts an optional DOM node type, which is propagated to `ReactComponentU` and `ReactComponentM`.
* Type changes.
  * `ReactComponentB` innards reworked. Use `ReactComponentB[P,S,B]` in place of `ReactComponentB[P]#B2[S]#B3[B]#B4[C]`.
  * `CompCtor`   → `ReactComponentC`
  * `CompCtorP`  → `ReactComponentC.ReqProps`
  * `CompCtorOP` → `ReactComponentC.DefaultProps`
  * `CompCtorNP` → `ReactComponentC.ConstProps`
  * `ReactComponentM` → `ReactComponentM_`
  * `ComponentConstructor_` → `ReactComponentC_`
  * `ComponentConstructor` → `ReactComponentCU`
* Renamed and deprecated the old:
  * `ReactComponentB.create` → `build`
  * `ReactComponentB.createU` → `buildU`
  * `ReactComponentB.propsAlways` → `propsConst`
  * `Nop` → `EmptyTag`
* Added `Simulation` for composition and abstraction of `ReactTestUtils.Simulate` procedures.
* Bugfix for tag attributes with primitive values.
  Eg. `input(tpe := "checkbox", checked := false)` works now.
* Added `ScalazReact.ReactS.liftR` of type `(S ⇒ ReactST[M,S,A]) ⇒ ReactST[M,S,A]`.
* `ScalazReact`'s `~~>` and `runState` functions are now lazy.
* Upgrade [Scalatags](https://github.com/lihaoyi/scalatags) to 0.4.2.
* Added `Sel` to easily lookup DOM in your tests. [Examples](https://github.com/japgolly/scalajs-react/blob/master/test/src/test/scala/japgolly/scalajs/react/test/SelTest.scala).

### 0.4.1 ([commit log](https://github.com/japgolly/scalajs-react/compare/v0.4.0...v0.4.1))

* Upgrade to scalatags 0.4.0.
* Component builder supports multiple callbacks.
* JS source maps point to Github.

### 0.4.0 ([commit log](https://github.com/japgolly/scalajs-react/compare/v0.2.0...v0.4.0))
* Major overhaul.
* Modules for Scalaz and testing.

### 0.2.0 ([commit log](https://github.com/japgolly/scalajs-react/compare/v0.1.0...v0.2.0))

### 0.1.0 ([commit log](https://github.com/japgolly/scalajs-react/compare/55a19e7...v0.1.0))
