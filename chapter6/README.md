# 6章 トランスフォーマー

## 37節 回帰型ニューラルネットワーク

|図|説明|
|----|----|
|[![画像をベクトルに変換する](thumbs/chatgpt-book-ch6-37-1-image-to-vector.png)](chatgpt-book-ch6-37-1-image-to-vector.png)|画像をベクトルに変換|
|[![パディングによる文長の統一](thumbs/chatgpt-book-ch6-37-2-padding-tokens.png)](chatgpt-book-ch6-37-2-padding-tokens.png)|パディングして可変長の入力に対応（文長の統一）|
|[![RNNの逐次処理構造](thumbs/chatgpt-book-ch6-37-3-rnn-sequence.png)](chatgpt-book-ch6-37-3-rnn-sequence.png)|RNNの基本公正（逐次処理の構造）|
|[![多層RNNと双方向RNNの比較](thumbs/chatgpt-book-ch6-37-4-rnn-variants.png)](chatgpt-book-ch6-37-4-rnn-variants.png)|RNNの構成例（多層RNNと双方向RNNの比較）|
|[![RNNによる文章生成の流れ](thumbs/chatgpt-book-ch6-37-5-rnn-text-generation.png)](chatgpt-book-ch6-37-5-rnn-text-generation.png)|言語モデルとしてのRNN（文章生成の流れ）|
|[![トークンの処理深度の可視化](thumbs/chatgpt-book-ch6-37-6-transformer-layers.png)](chatgpt-book-ch6-37-6-transformer-layers.png)|本当は深いRNN（トークンの処理深度の可視化）|
|[![RNNとLSTMの構造比較](thumbs/chatgpt-book-ch6-37-7-rnn-vs-lstm.png)](chatgpt-book-ch6-37-7-rnn-vs-lstm.png)|LSTMの基本構成（RNNとLSTMの比較）|
|[![翻訳タスクのエンコーダ・デコーダ構造](thumbs/chatgpt-book-ch6-37-8-rnn-encoder-decoder.png)](chatgpt-book-ch6-37-8-rnn-encoder-decoder.png)|RNNによるエンコーダー・デコーダー（翻訳タスクを例に）|



## 38節 注意機構（Attention）

|図|説明|
|----|----|
|[![Attentionによる質問応答の仕組み](thumbs/chatgpt-book-ch6-38-1-attention-mechanism.png)](chatgpt-book-ch6-38-1-attention-mechanism.png)|Memory Networkのモデル概要（シンプルなAttentionによる質問応答の仕組み）|
|[![基本的な翻訳モデルの構造](thumbs/chatgpt-book-ch6-38-2-rnn-translation.png)](chatgpt-book-ch6-38-2-rnn-translation.png)|RNNによるエンコーダー・デコーダー（Attentionを組み込む前）|
|[![Attention付き翻訳の処理流れ](thumbs/chatgpt-book-ch6-38-3-seq2seq-attention.png)](chatgpt-book-ch6-38-3-seq2seq-attention.png)|RNNエンコーダー・デコーダーと注意機構|


## 39節 注意機構の計算

|図|説明|
|----|----|
|[![Q・K・Vの生成方法](thumbs/chatgpt-book-ch6-39-1-rnn-qkv-extraction.png)](chatgpt-book-ch6-39-1-rnn-qkv-extraction.png)|RNNブロックから検索キーK、値V、質問Qを生成|
|[![QueryとKeyの類似度計算](thumbs/chatgpt-book-ch6-39-2-attention-similarity.png)](chatgpt-book-ch6-39-2-attention-similarity.png)|検索キーKと質問Qの類似度計算|
|[![Attentionによる重み付き和](thumbs/chatgpt-book-ch6-39-3-attention-weighted-sum.png)](chatgpt-book-ch6-39-3-attention-weighted-sum.png)|値VのAttention重み付き平均と元のブロックの出力の和を取る|
|[![翻訳におけるAttentionの学習](thumbs/chatgpt-book-ch6-39-4-attention-learning.png)](chatgpt-book-ch6-39-4-attention-learning.png)|注意機構の学習|


## 40節 トランスフォーマー（Transformer）

|図|説明|
|----|----|
|[![LSTMとTransformerの比較](thumbs/chatgpt-book-ch6-40-1-lstm-vs-transformer.png)](chatgpt-book-ch6-40-1-lstm-vs-transformer.png)|LSTM（RNN）とTransformerの基本構成を比較|
|[![Transformerブロックの構成](thumbs/chatgpt-book-ch6-40-2-transformer-block.png)](chatgpt-book-ch6-40-2-transformer-block.png)|シンプルなTransformerブロックの構成|
|[![位置情報の加算とレイヤー構造](thumbs/chatgpt-book-ch6-40-3-positional-encoding.png)](chatgpt-book-ch6-40-3-positional-encoding.png)|位置エンコーディング（絶対位置）の加算|
|[![HDDの読み取りの仕組み](thumbs/chatgpt-book-ch6-40-4-hdd-head.png)](chatgpt-book-ch6-40-4-hdd-head.png)|HDD（ハードディスク）の読み取りヘッド（マルチ「ヘッド」の用語の説明として）|
|[![マルチヘッドAttentionの動作](thumbs/chatgpt-book-ch6-40-5-multihead-attention.png)](chatgpt-book-ch6-40-5-multihead-attention.png)|マルチヘッドAttentionの動作|


## 41節 BERT

|図|説明|
|----|----|
|[![BERTの事前学習と応用](thumbs/chatgpt-book-ch6-41-1-bert-finetuning-flow.png)](chatgpt-book-ch6-41-1-bert-finetuning-flow.png)|BERTによる基盤モデルの事前学習とファインチューニング|
|[![BERTによるマスク予測](thumbs/chatgpt-book-ch6-41-2-bert-masked-lm.png)](chatgpt-book-ch6-41-2-bert-masked-lm.png)|BERTの事前学習（Masked言語モデル）|
|[![BERTによる文のつながり判定](thumbs/chatgpt-book-ch6-41-3-next-sentence-prediction.png)](chatgpt-book-ch6-41-3-next-sentence-prediction.png)|BERTの事前学習（次文章予測）|


## 42節 GPT（Generative Pretrained Transformer）

|図|説明|
|----|----|
|[![デコーダのマスク付き自己Attention](thumbs/chatgpt-book-ch6-42-1-masked-attention.png)](chatgpt-book-ch6-42-1-masked-attention.png)|GPT（Generative Pretrained Transformer）の基本構成|
|[![Mixture of Expertsの動的選択](thumbs/chatgpt-book-ch6-42-2-mixture-of-experts.png)](chatgpt-book-ch6-42-2-mixture-of-experts.png)|Mixture of Expertsの模式図|

