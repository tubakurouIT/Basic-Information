# インデックスレジスタ（Index Register）

## 💡 インデックスレジスタとは？
**インデックスレジスタ（IX）** は、CPU 内にある **特別なレジスタ** で、  
**メモリアドレスを計算するときに使われる** レジスタです。  
特に、**配列のアクセスやループ処理** で大活躍します！  

---

## 🔍 何をするの？
インデックスレジスタの主な役割は、  
**基本アドレス（基準のメモリアドレス）にオフセットを加えて、実際のメモリアドレスを求めること** です。  


## 🟢 インデックスアドレス指定方式（Indexed Addressing）  
**📌 「並んでいるデータを順番に使いたいとき」に便利！**  

👉 **基本アドレス** に **インデックス（番号）** を足して、使うデータの場所を決める方法。  

📖 **イメージ**：本の目次（インデックス）を使って、目的のページを探す感じ！  

### 🏀 例：バスケットボールのチームメンバー  
1. **基本アドレス** → チームの名簿（リストの最初の位置）  
2. **インデックスレジスタ** → 1 人目、2 人目、3 人目...  

| インデックス | 実際のデータ（名前） |
|------------|------------------|
| 0（最初） | 田中 |
| 1（次の人） | 鈴木 |
| 2 | 佐藤 |
| 3 | 高橋 |

💡 **インデックスを 1 ずつ増やせば、次々にメンバーを呼び出せる！**  

---

## 🔵 ベースアドレス指定方式（Base Addressing）  
**📌 「決まった基準の場所からデータを探したいとき」に便利！**  

👉 **ベース（基準）となるアドレス** を決めて、そこからの **距離（オフセット）** で目的のデータを探す方法。  

📖 **イメージ**：引っ越しするとき、家の「住所（ベースアドレス）」を変えるだけで、全部の荷物の位置が変わる感じ！  

### 📦 例：荷物の保管場所  
1. **ベースアドレス** → 倉庫の住所（出発点）  
2. **オフセット** → 荷物の棚番号（何番目の棚か）  

| オフセット | 実際の場所（荷物のある棚） |
|----------|--------------------|
| 0 | 入口すぐの棚 |
| 1 | 2 番目の棚 |
| 2 | 3 番目の棚 |

💡 **ベースアドレスを変えるだけで、すべてのデータの位置が変わるので、管理が簡単！**  

---

## 🔴 相対アドレス指定方式（Relative Addressing）  
**📌 「今いる場所を基準に、次の目的地を決めたいとき」に便利！**  

👉 **現在のアドレス（PC = プログラムカウンタ）** を基準にして、そこからの **距離（オフセット）** で次のアドレスを決める方法。  

📖 **イメージ**：カーナビで「あと 500m 進んで右！」みたいに、今の位置を基準に道を決める感じ！  

### 🚗 例：カーナビの案内  
1. **プログラムカウンタ（PC）** → 今いる場所  
2. **オフセット** → 目的地までの距離  

| オフセット | 目的地 |
|----------|------|
| +500m | 交差点 |
| +1km | ガソリンスタンド |
| -200m | 戻る（行きすぎた！） |

💡 **プログラムを移動しても「今の位置＋どれだけ動くか」だけで動けるので、柔軟に動作できる！**  

---

## 🎯 まとめ  

| 方式 | どんなときに使う？ | 例え |
|------|----------------|----|
| **インデックスアドレス指定方式** | **順番に並んだデータを扱う** | チームの名簿（リスト） |
| **ベースアドレス指定方式** | **基準の場所を決めてデータを探す** | 倉庫の棚（保管場所） |
| **相対アドレス指定方式** | **今いる場所からの距離で動く** | カーナビの案内 |

---