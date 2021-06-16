# WordEmbedding
本筆記詞嵌⼊的概念由Mikolov等⼈在2013年提出，詳⾒" 📄 Distributed Representations of Words and Phrases and their
Compositionality "。
詞嵌⼊的出現是為了改善One-hot編碼，因為單詞經過One-hot編碼後的詞向量太過稀疏，彼此間缺乏了相關性；⽽詞嵌⼊的出現⼀
⽅⾯可以將單詞以更好的⽅式編碼來展現出詞和詞之間的關聯性，另⼀⽅⾯，以詞嵌⼊來編碼可以降低詞向量的維度，讓神經網路模
型以更有效率得學習。
以我的理解和練習過後，⽐起把Embedding當成⼀個模型，不如說Embedding是⼀個單字的查找表，可以將One-hot的詞向量透過
Embedding來找出對應的詞嵌⼊向量。在論⽂中作者提出了兩種⽅法來訓練詞向量，分別是CBOW和Skip-gram。
在程式部分，我實現了⽤兩種不同的⽅式來訓練Embedding，不管是哪種⽅法，我所使⽤的模型都是⻑得⼀樣的，⼀個簡單的兩層
全連接網路，而我所使用的Dataset為卡通辛普森家庭的腳色台詞。
在預處理階段我必須對每一個句子去做斷詞，對於不同的window size要組成多樣化的Training Data...等等，有許多必須顧慮到的小細節。
總之在實現完WordEmbedding之後，我認為這次的小實驗對資料的預處理比對模型的搭建還要複雜許多
