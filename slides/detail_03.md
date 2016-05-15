## Trailblazerのstack

* `trailblazer` gemが提供するのは先の図でいう`OPERATION`部分
* 基本的に機能毎に、gemが分かれている(View Modelは`cell`等)
  * 正確には`FORM`も`reform` gemに分かれている
  * `trailblazer` gemのdependencyに含まれているのは`reform`だけ。後は必要に応じて追加する形。
* gemはそれ単体で使用出来るようになっている
  * `trailblazer` gemは使用した事無くても、`cell`は使用した事ある、という人もといるのでは
