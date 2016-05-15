## Rails辛い問題

* 気付くとfat controller
 * fat controllerを避けようとした結果、今度はmodelがfatになる
* viewにロジックが定義されている
  * viewから直接DB参照してたり
* ビジネスロジックをどこに書けば良いのかわからない
  * プロジェクト / 人毎にビジネスロジックを定義する場所がバラバラになる
* etc
