# コンピュータ将棋互角局面集

コンピュータ将棋の互角局面集（おそらく互角に近いと思われる局面集）です。  
将棋ソフトの自己対局等にご活用頂ければ幸いです。

※ご使用は自己責任でお願いいたします。

24手目時点の互角局面は[「やねうら互角局面集」](http://yaneuraou.yaneu.com/2016/08/24/%E8%87%AA%E5%B7%B1%E5%AF%BE%E5%B1%80%E7%94%A8%E3%81%AB%E4%BA%92%E8%A7%92%E3%81%AE%E5%B1%80%E9%9D%A2%E9%9B%86%E3%82%92%E5%85%AC%E9%96%8B%E3%81%97%E3%81%BE%E3%81%97%E3%81%9F/)として既に公開されていますので  
ここでは、終盤力の測定用に100手目時点の互角局面集を作成してみました。  
ファイル形式は[「やねうら互角局面集」](http://yaneuraou.yaneu.com/2016/08/24/%E8%87%AA%E5%B7%B1%E5%AF%BE%E5%B1%80%E7%94%A8%E3%81%AB%E4%BA%92%E8%A7%92%E3%81%AE%E5%B1%80%E9%9D%A2%E9%9B%86%E3%82%92%E5%85%AC%E9%96%8B%E3%81%97%E3%81%BE%E3%81%97%E3%81%9F/)と同様です。  
（追記：その後、様々な手数時点の互角局面集を追加で作成しました。）  

- floodgate互角局面集（010手目、評価値±100以内、R3200以上、698局面）.sfen
- floodgate互角局面集（020手目、評価値±100以内、R3200以上、1640局面）.sfen
- floodgate互角局面集（030手目、評価値±100以内、R3200以上、1619局面）.sfen
- floodgate互角局面集（040手目、評価値±100以内、R3200以上、1259局面）.sfen
- floodgate互角局面集（050手目、評価値±100以内、R3200以上、945局面）.sfen
- floodgate互角局面集（060手目、評価値±100以内、R3200以上、683局面）.sfen
- floodgate互角局面集（070手目、評価値±100以内、R3200以上、482局面）.sfen
- floodgate互角局面集（080手目、評価値±100以内、R3200以上、300局面）.sfen
- floodgate互角局面集（090手目、評価値±100以内、R3200以上、199局面）.sfen
- floodgate互角局面集（100手目、評価値±100以内、R3200以上、140局面）.sfen
- floodgate互角局面集（110手目、評価値±100以内、R3200以上、77局面）.sfen
- floodgate互角局面集（120手目、評価値±100以内、R3200以上、45局面）.sfen
- floodgate互角局面集（130手目、評価値±100以内、R3200以上、36局面）.sfen
- floodgate互角局面集（140手目、評価値±100以内、R3200以上、35局面）.sfen
- floodgate互角局面集（150手目、評価値±100以内、R3200以上、24局面）.sfen
- floodgate互角局面集（160手目、評価値±100以内、R3200以上、21局面）.sfen
- floodgate互角局面集（170手目、評価値±100以内、R3200以上、9局面）.sfen
- floodgate互角局面集（180手目、評価値±100以内、R3200以上、6局面）.sfen
- floodgate互角局面集（190手目、評価値±100以内、R3200以上、8局面）.sfen
- floodgate互角局面集（200手目、評価値±100以内、R3200以上、3局面）.sfen
- floodgate互角局面集（210手目、評価値±100以内、R3200以上、2局面）.sfen
- floodgate互角局面集（220手目、評価値±100以内、R3200以上、5局面）.sfen
- floodgate互角局面集（230手目、評価値±100以内、R3200以上、1局面）.sfen
- floodgate互角局面集（240手目、評価値±100以内、R3200以上、2局面）.sfen
- floodgate互角局面集（250手目、評価値±100以内、R3200以上、1局面）.sfen


## 使用方法

- sfenファイルをテキストエディタ等で開き、任意の1行をShogiGUIにコピー＆ペーストして使用することができます。
- sfenファイルをShogiGUIの定跡ファイルに変換すると、互角局面から対局を始めることができるようになります。（詳細は[uuunuuunさんのWebサイト](http://www.uuunuuun.com/single-post/2016/12/11/%E4%B8%AD%E7%B5%82%E7%9B%A4%E3%81%AE%E3%82%BD%E3%83%95%E3%83%88%E3%81%AE%E5%8A%9B%E9%87%8F%E3%81%AE%E6%B8%AC%E5%AE%9A)をご参照ください）


## 作成方法

当局面集は、以下の手順で作成しました。  
（例えば「floodgate互角局面集（080手目、評価値±100以内、R3200以上、300局面）.sfen」の場合）  

（１）[floodgate](http://wdoor.c.u-tokyo.ac.jp/shogi/floodgate)の2015年、2016年（12月中旬まで）の全棋譜から以下の条件で抽出。  
　　・両対局者のレーティングが3200以上であること。  
　　・80手目及び81手目の評価値がともに-100～+100であること。  
　　　ただし、評価値0は除く。（評価値0は千日手やMateの可能性があり、また、常に評価値0を返すソフトもあるため）  
（２）[Blunder.Converter](https://github.com/ak110/Blunder.Converter)でcsaファイルをsfenファイルに変換し、1ファイルに結合。  
（３）結合後のsfenファイルの各行を80手目まででカット。  
（４）重複行を除外。（同一手順で同一局面になったケースは除外されますが、手順違いで同一局面になったケースは除外されていませんのでご留意ください）  


## 先手有利局面集

互角局面集と同じ要領で「先手有利局面集」を作成しました。  
両対局者の評価値がともに先手有利の+400～+600であることを抽出条件としています。  
あえて少し差のある局面から対局させることにより、逆転力の測定や逆転されずに勝ち切る力の測定などができるかもしれません。  

- floodgate先手有利局面集（010手目、評価値+400～+600、R3200以上、0局面）.sfen
- floodgate先手有利局面集（020手目、評価値+400～+600、R3200以上、2局面）.sfen
- floodgate先手有利局面集（030手目、評価値+400～+600、R3200以上、12局面）.sfen
- floodgate先手有利局面集（040手目、評価値+400～+600、R3200以上、41局面）.sfen
- floodgate先手有利局面集（050手目、評価値+400～+600、R3200以上、98局面）.sfen
- floodgate先手有利局面集（060手目、評価値+400～+600、R3200以上、138局面）.sfen
- floodgate先手有利局面集（070手目、評価値+400～+600、R3200以上、185局面）.sfen
- floodgate先手有利局面集（080手目、評価値+400～+600、R3200以上、186局面）.sfen
- floodgate先手有利局面集（090手目、評価値+400～+600、R3200以上、167局面）.sfen
- floodgate先手有利局面集（100手目、評価値+400～+600、R3200以上、110局面）.sfen
- floodgate先手有利局面集（110手目、評価値+400～+600、R3200以上、79局面）.sfen
- floodgate先手有利局面集（120手目、評価値+400～+600、R3200以上、60局面）.sfen
- floodgate先手有利局面集（130手目、評価値+400～+600、R3200以上、47局面）.sfen
- floodgate先手有利局面集（140手目、評価値+400～+600、R3200以上、18局面）.sfen
- floodgate先手有利局面集（150手目、評価値+400～+600、R3200以上、16局面）.sfen
- floodgate先手有利局面集（160手目、評価値+400～+600、R3200以上、8局面）.sfen
- floodgate先手有利局面集（170手目、評価値+400～+600、R3200以上、11局面）.sfen
- floodgate先手有利局面集（180手目、評価値+400～+600、R3200以上、7局面）.sfen
- floodgate先手有利局面集（190手目、評価値+400～+600、R3200以上、1局面）.sfen
- floodgate先手有利局面集（200手目、評価値+400～+600、R3200以上、0局面）.sfen
- floodgate先手有利局面集（210手目、評価値+400～+600、R3200以上、3局面）.sfen
- floodgate先手有利局面集（220手目、評価値+400～+600、R3200以上、1局面）.sfen
- floodgate先手有利局面集（230手目、評価値+400～+600、R3200以上、2局面）.sfen
- floodgate先手有利局面集（240手目、評価値+400～+600、R3200以上、1局面）.sfen
- floodgate先手有利局面集（250手目、評価値+400～+600、R3200以上、3局面）.sfen


## 後手有利局面集

上記「先手有利局面集」の後手版です。  

- floodgate後手有利局面集（010手目、評価値-600～-400、R3200以上、0局面）.sfen
- floodgate後手有利局面集（020手目、評価値-600～-400、R3200以上、2局面）.sfen
- floodgate後手有利局面集（030手目、評価値-600～-400、R3200以上、1局面）.sfen
- floodgate後手有利局面集（040手目、評価値-600～-400、R3200以上、16局面）.sfen
- floodgate後手有利局面集（050手目、評価値-600～-400、R3200以上、27局面）.sfen
- floodgate後手有利局面集（060手目、評価値-600～-400、R3200以上、64局面）.sfen
- floodgate後手有利局面集（070手目、評価値-600～-400、R3200以上、124局面）.sfen
- floodgate後手有利局面集（080手目、評価値-600～-400、R3200以上、134局面）.sfen
- floodgate後手有利局面集（090手目、評価値-600～-400、R3200以上、136局面）.sfen
- floodgate後手有利局面集（100手目、評価値-600～-400、R3200以上、115局面）.sfen
- floodgate後手有利局面集（110手目、評価値-600～-400、R3200以上、89局面）.sfen
- floodgate後手有利局面集（120手目、評価値-600～-400、R3200以上、53局面）.sfen
- floodgate後手有利局面集（130手目、評価値-600～-400、R3200以上、44局面）.sfen
- floodgate後手有利局面集（140手目、評価値-600～-400、R3200以上、25局面）.sfen
- floodgate後手有利局面集（150手目、評価値-600～-400、R3200以上、19局面）.sfen
- floodgate後手有利局面集（160手目、評価値-600～-400、R3200以上、11局面）.sfen
- floodgate後手有利局面集（170手目、評価値-600～-400、R3200以上、10局面）.sfen
- floodgate後手有利局面集（180手目、評価値-600～-400、R3200以上、6局面）.sfen
- floodgate後手有利局面集（190手目、評価値-600～-400、R3200以上、8局面）.sfen
- floodgate後手有利局面集（200手目、評価値-600～-400、R3200以上、3局面）.sfen
- floodgate後手有利局面集（210手目、評価値-600～-400、R3200以上、4局面）.sfen
- floodgate後手有利局面集（220手目、評価値-600～-400、R3200以上、6局面）.sfen
- floodgate後手有利局面集（230手目、評価値-600～-400、R3200以上、2局面）.sfen
- floodgate後手有利局面集（240手目、評価値-600～-400、R3200以上、3局面）.sfen
- floodgate後手有利局面集（250手目、評価値-600～-400、R3200以上、2局面）.sfen


## 評価の分かれる局面集

上記「互角局面集」「先手有利局面集」等は両対局者の局面評価が近いことが抽出条件に含まれますので  
逆に、「評価の分かれる局面集」も作成してみました。  

- floodgate評価の分かれる局面集（010手目、評価値-300以下と+300以上、R3200以上、0局面）.sfen
- floodgate評価の分かれる局面集（020手目、評価値-300以下と+300以上、R3200以上、0局面）.sfen
- floodgate評価の分かれる局面集（030手目、評価値-300以下と+300以上、R3200以上、0局面）.sfen
- floodgate評価の分かれる局面集（040手目、評価値-300以下と+300以上、R3200以上、3局面）.sfen
- floodgate評価の分かれる局面集（050手目、評価値-300以下と+300以上、R3200以上、5局面）.sfen
- floodgate評価の分かれる局面集（060手目、評価値-300以下と+300以上、R3200以上、5局面）.sfen
- floodgate評価の分かれる局面集（070手目、評価値-300以下と+300以上、R3200以上、15局面）.sfen
- floodgate評価の分かれる局面集（080手目、評価値-300以下と+300以上、R3200以上、24局面）.sfen
- floodgate評価の分かれる局面集（090手目、評価値-300以下と+300以上、R3200以上、23局面）.sfen
- floodgate評価の分かれる局面集（100手目、評価値-300以下と+300以上、R3200以上、23局面）.sfen
- floodgate評価の分かれる局面集（110手目、評価値-300以下と+300以上、R3200以上、18局面）.sfen
- floodgate評価の分かれる局面集（120手目、評価値-300以下と+300以上、R3200以上、22局面）.sfen
- floodgate評価の分かれる局面集（130手目、評価値-300以下と+300以上、R3200以上、24局面）.sfen
- floodgate評価の分かれる局面集（140手目、評価値-300以下と+300以上、R3200以上、22局面）.sfen
- floodgate評価の分かれる局面集（150手目、評価値-300以下と+300以上、R3200以上、15局面）.sfen
- floodgate評価の分かれる局面集（160手目、評価値-300以下と+300以上、R3200以上、12局面）.sfen
- floodgate評価の分かれる局面集（170手目、評価値-300以下と+300以上、R3200以上、13局面）.sfen
- floodgate評価の分かれる局面集（180手目、評価値-300以下と+300以上、R3200以上、10局面）.sfen
- floodgate評価の分かれる局面集（190手目、評価値-300以下と+300以上、R3200以上、6局面）.sfen
- floodgate評価の分かれる局面集（200手目、評価値-300以下と+300以上、R3200以上、7局面）.sfen
- floodgate評価の分かれる局面集（210手目、評価値-300以下と+300以上、R3200以上、4局面）.sfen
- floodgate評価の分かれる局面集（220手目、評価値-300以下と+300以上、R3200以上、2局面）.sfen
- floodgate評価の分かれる局面集（230手目、評価値-300以下と+300以上、R3200以上、3局面）.sfen
- floodgate評価の分かれる局面集（240手目、評価値-300以下と+300以上、R3200以上、4局面）.sfen
- floodgate評価の分かれる局面集（250手目、評価値-300以下と+300以上、R3200以上、3局面）.sfen


## 先手反省局面集

互角局面集等と同じような方法で「先手反省局面集」を作成しました。  
例えば「floodgate先手反省局面集（081手目の評価値+300以上、091手目の評価値-300以下、R3200以上、10局面）.sfen」の場合、  
81手目時点では先手の評価値が+300以上で、91手目時点では先手の評価値が-300以下になった棋譜の91手目までのsfen文字列になります。  
互角局面集等と異なり、後手の評価値は抽出条件に使用していません。（後手の対局者のレーティングは抽出条件に使用しています。）  

- floodgate先手反省局面集（011手目の評価値+300以上、021手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate先手反省局面集（021手目の評価値+300以上、031手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate先手反省局面集（031手目の評価値+300以上、041手目の評価値-300以下、R3200以上、1局面）.sfen
- floodgate先手反省局面集（041手目の評価値+300以上、051手目の評価値-300以下、R3200以上、1局面）.sfen
- floodgate先手反省局面集（051手目の評価値+300以上、061手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate先手反省局面集（061手目の評価値+300以上、071手目の評価値-300以下、R3200以上、4局面）.sfen
- floodgate先手反省局面集（071手目の評価値+300以上、081手目の評価値-300以下、R3200以上、9局面）.sfen
- floodgate先手反省局面集（081手目の評価値+300以上、091手目の評価値-300以下、R3200以上、10局面）.sfen
- floodgate先手反省局面集（091手目の評価値+300以上、101手目の評価値-300以下、R3200以上、21局面）.sfen
- floodgate先手反省局面集（101手目の評価値+300以上、111手目の評価値-300以下、R3200以上、14局面）.sfen
- floodgate先手反省局面集（111手目の評価値+300以上、121手目の評価値-300以下、R3200以上、18局面）.sfen
- floodgate先手反省局面集（121手目の評価値+300以上、131手目の評価値-300以下、R3200以上、9局面）.sfen
- floodgate先手反省局面集（131手目の評価値+300以上、141手目の評価値-300以下、R3200以上、20局面）.sfen
- floodgate先手反省局面集（141手目の評価値+300以上、151手目の評価値-300以下、R3200以上、10局面）.sfen
- floodgate先手反省局面集（151手目の評価値+300以上、161手目の評価値-300以下、R3200以上、6局面）.sfen
- floodgate先手反省局面集（161手目の評価値+300以上、171手目の評価値-300以下、R3200以上、6局面）.sfen
- floodgate先手反省局面集（171手目の評価値+300以上、181手目の評価値-300以下、R3200以上、1局面）.sfen
- floodgate先手反省局面集（181手目の評価値+300以上、191手目の評価値-300以下、R3200以上、4局面）.sfen
- floodgate先手反省局面集（191手目の評価値+300以上、201手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate先手反省局面集（201手目の評価値+300以上、211手目の評価値-300以下、R3200以上、3局面）.sfen
- floodgate先手反省局面集（211手目の評価値+300以上、221手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate先手反省局面集（221手目の評価値+300以上、231手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate先手反省局面集（231手目の評価値+300以上、241手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate先手反省局面集（241手目の評価値+300以上、251手目の評価値-300以下、R3200以上、0局面）.sfen


## 後手反省局面集

上記「先手反省局面集」の後手版です。  
互角局面集等と異なり、先手の評価値は抽出条件に使用していません。（先手の対局者のレーティングは抽出条件に使用しています。）  

- floodgate後手反省局面集（010手目の評価値-300以下、020手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate後手反省局面集（020手目の評価値-300以下、030手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate後手反省局面集（030手目の評価値-300以下、040手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate後手反省局面集（040手目の評価値-300以下、050手目の評価値+300以上、R3200以上、1局面）.sfen
- floodgate後手反省局面集（050手目の評価値-300以下、060手目の評価値+300以上、R3200以上、2局面）.sfen
- floodgate後手反省局面集（060手目の評価値-300以下、070手目の評価値+300以上、R3200以上、1局面）.sfen
- floodgate後手反省局面集（070手目の評価値-300以下、080手目の評価値+300以上、R3200以上、3局面）.sfen
- floodgate後手反省局面集（080手目の評価値-300以下、090手目の評価値+300以上、R3200以上、13局面）.sfen
- floodgate後手反省局面集（090手目の評価値-300以下、100手目の評価値+300以上、R3200以上、13局面）.sfen
- floodgate後手反省局面集（100手目の評価値-300以下、110手目の評価値+300以上、R3200以上、10局面）.sfen
- floodgate後手反省局面集（110手目の評価値-300以下、120手目の評価値+300以上、R3200以上、13局面）.sfen
- floodgate後手反省局面集（120手目の評価値-300以下、130手目の評価値+300以上、R3200以上、17局面）.sfen
- floodgate後手反省局面集（130手目の評価値-300以下、140手目の評価値+300以上、R3200以上、9局面）.sfen
- floodgate後手反省局面集（140手目の評価値-300以下、150手目の評価値+300以上、R3200以上、8局面）.sfen
- floodgate後手反省局面集（150手目の評価値-300以下、160手目の評価値+300以上、R3200以上、8局面）.sfen
- floodgate後手反省局面集（160手目の評価値-300以下、170手目の評価値+300以上、R3200以上、2局面）.sfen
- floodgate後手反省局面集（170手目の評価値-300以下、180手目の評価値+300以上、R3200以上、3局面）.sfen
- floodgate後手反省局面集（180手目の評価値-300以下、190手目の評価値+300以上、R3200以上、3局面）.sfen
- floodgate後手反省局面集（190手目の評価値-300以下、200手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate後手反省局面集（200手目の評価値-300以下、210手目の評価値+300以上、R3200以上、1局面）.sfen
- floodgate後手反省局面集（210手目の評価値-300以下、220手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate後手反省局面集（220手目の評価値-300以下、230手目の評価値+300以上、R3200以上、3局面）.sfen
- floodgate後手反省局面集（230手目の評価値-300以下、240手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate後手反省局面集（240手目の評価値-300以下、250手目の評価値+300以上、R3200以上、0局面）.sfen


## 先手逆転局面集

互角局面集等と同じような方法で「先手逆転局面集」を作成しました。  
例えば「floodgate先手逆転局面集（081手目の評価値-300以下、091手目の評価値+300以上、R3200以上、9局面）.sfen」の場合、  
81手目時点では先手の評価値が-300以下で、91手目時点では先手の評価値が+300以上になった棋譜の91手目までのsfen文字列になります。  
互角局面集等と異なり、後手の評価値は抽出条件に使用していません。（後手の対局者のレーティングは抽出条件に使用しています。）  
※「先手逆転局面集」と「後手反省局面集」には同じ棋譜が含まれる場合もありますが、必ずしも両者は一致するとは限らないようです。

- floodgate先手逆転局面集（011手目の評価値-300以下、021手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（021手目の評価値-300以下、031手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（031手目の評価値-300以下、041手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（041手目の評価値-300以下、051手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（051手目の評価値-300以下、061手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（061手目の評価値-300以下、071手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（071手目の評価値-300以下、081手目の評価値+300以上、R3200以上、1局面）.sfen
- floodgate先手逆転局面集（081手目の評価値-300以下、091手目の評価値+300以上、R3200以上、9局面）.sfen
- floodgate先手逆転局面集（091手目の評価値-300以下、101手目の評価値+300以上、R3200以上、3局面）.sfen
- floodgate先手逆転局面集（101手目の評価値-300以下、111手目の評価値+300以上、R3200以上、10局面）.sfen
- floodgate先手逆転局面集（111手目の評価値-300以下、121手目の評価値+300以上、R3200以上、8局面）.sfen
- floodgate先手逆転局面集（121手目の評価値-300以下、131手目の評価値+300以上、R3200以上、8局面）.sfen
- floodgate先手逆転局面集（131手目の評価値-300以下、141手目の評価値+300以上、R3200以上、12局面）.sfen
- floodgate先手逆転局面集（141手目の評価値-300以下、151手目の評価値+300以上、R3200以上、8局面）.sfen
- floodgate先手逆転局面集（151手目の評価値-300以下、161手目の評価値+300以上、R3200以上、4局面）.sfen
- floodgate先手逆転局面集（161手目の評価値-300以下、171手目の評価値+300以上、R3200以上、2局面）.sfen
- floodgate先手逆転局面集（171手目の評価値-300以下、181手目の評価値+300以上、R3200以上、2局面）.sfen
- floodgate先手逆転局面集（181手目の評価値-300以下、191手目の評価値+300以上、R3200以上、1局面）.sfen
- floodgate先手逆転局面集（191手目の評価値-300以下、201手目の評価値+300以上、R3200以上、1局面）.sfen
- floodgate先手逆転局面集（201手目の評価値-300以下、211手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（211手目の評価値-300以下、221手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（221手目の評価値-300以下、231手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（231手目の評価値-300以下、241手目の評価値+300以上、R3200以上、0局面）.sfen
- floodgate先手逆転局面集（241手目の評価値-300以下、251手目の評価値+300以上、R3200以上、0局面）.sfen


## 後手逆転局面集

上記「先手逆転局面集」の後手版です。  
互角局面集等と異なり、先手の評価値は抽出条件に使用していません。（先手の対局者のレーティングは抽出条件に使用しています。）  

- floodgate後手逆転局面集（010手目の評価値+300以上、020手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate後手逆転局面集（020手目の評価値+300以上、030手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate後手逆転局面集（030手目の評価値+300以上、040手目の評価値-300以下、R3200以上、1局面）.sfen
- floodgate後手逆転局面集（040手目の評価値+300以上、050手目の評価値-300以下、R3200以上、1局面）.sfen
- floodgate後手逆転局面集（050手目の評価値+300以上、060手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate後手逆転局面集（060手目の評価値+300以上、070手目の評価値-300以下、R3200以上、3局面）.sfen
- floodgate後手逆転局面集（070手目の評価値+300以上、080手目の評価値-300以下、R3200以上、3局面）.sfen
- floodgate後手逆転局面集（080手目の評価値+300以上、090手目の評価値-300以下、R3200以上、6局面）.sfen
- floodgate後手逆転局面集（090手目の評価値+300以上、100手目の評価値-300以下、R3200以上、11局面）.sfen
- floodgate後手逆転局面集（100手目の評価値+300以上、110手目の評価値-300以下、R3200以上、10局面）.sfen
- floodgate後手逆転局面集（110手目の評価値+300以上、120手目の評価値-300以下、R3200以上、8局面）.sfen
- floodgate後手逆転局面集（120手目の評価値+300以上、130手目の評価値-300以下、R3200以上、11局面）.sfen
- floodgate後手逆転局面集（130手目の評価値+300以上、140手目の評価値-300以下、R3200以上、12局面）.sfen
- floodgate後手逆転局面集（140手目の評価値+300以上、150手目の評価値-300以下、R3200以上、9局面）.sfen
- floodgate後手逆転局面集（150手目の評価値+300以上、160手目の評価値-300以下、R3200以上、4局面）.sfen
- floodgate後手逆転局面集（160手目の評価値+300以上、170手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate後手逆転局面集（170手目の評価値+300以上、180手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate後手逆転局面集（180手目の評価値+300以上、190手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate後手逆転局面集（190手目の評価値+300以上、200手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate後手逆転局面集（200手目の評価値+300以上、210手目の評価値-300以下、R3200以上、2局面）.sfen
- floodgate後手逆転局面集（210手目の評価値+300以上、220手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate後手逆転局面集（220手目の評価値+300以上、230手目の評価値-300以下、R3200以上、0局面）.sfen
- floodgate後手逆転局面集（230手目の評価値+300以上、240手目の評価値-300以下、R3200以上、1局面）.sfen
- floodgate後手逆転局面集（240手目の評価値+300以上、250手目の評価値-300以下、R3200以上、0局面）.sfen


## その他

将棋ソフトの開発で、例えば探索パラメータを変更した際に、通常の自己対局では変更前のソフトに負け越すものの  
終盤互角局面からの対局では変更前のソフトに勝ち越すようなことがあるかもしれません。  
この場合、おそらく序盤は変更前のパラメータの方が適切で、終盤は変更後のパラメータの方が適切なように思われるので  
進行度や手数を使って探索パラメータを動的に変化させることにより、  
通常の自己対局、終盤互角局面からの対局の両方で変更前のソフトに勝ち越せるような調整が可能なのではないかと夢想しています。  


## 参考

- やねうら互角局面集  
http://yaneuraou.yaneu.com/2016/08/24/%E8%87%AA%E5%B7%B1%E5%AF%BE%E5%B1%80%E7%94%A8%E3%81%AB%E4%BA%92%E8%A7%92%E3%81%AE%E5%B1%80%E9%9D%A2%E9%9B%86%E3%82%92%E5%85%AC%E9%96%8B%E3%81%97%E3%81%BE%E3%81%97%E3%81%9F/

- 互角局面集の活用法  
http://www.uuunuuun.com/single-post/2016/12/11/%E4%B8%AD%E7%B5%82%E7%9B%A4%E3%81%AE%E3%82%BD%E3%83%95%E3%83%88%E3%81%AE%E5%8A%9B%E9%87%8F%E3%81%AE%E6%B8%AC%E5%AE%9A

