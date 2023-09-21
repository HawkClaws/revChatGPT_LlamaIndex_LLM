# revChatGPT_LlamaIndex_LLM

`acheong08/ChatGPT`を利用したLlamaIndexのCustomLLMの実装  
ハイスペックPC不要、無課金で`LlamaIndex`が楽しめます

## 事前準備

### ライブラリインストール

下記２つのライブラリが動作する環境が必要になります

- [llama-index](https://github.com/jerryjliu/llama_index)
- [revChatGPT](https://github.com/acheong08/ChatGPT)


基本的には、下記でインストールすればOK

`pip install llama-index revChatGPT`

### コード上での設定

下記箇所を必要に応じて変更してください

```python

# ChatGPTから502エラーが返る場合は下記をコメントアウト
# from os import environ
# environ['CHATGPT_BASE_URL'] = 'https://ai.fakeopen.com/api/'

# ChatGPTのアクセストークンの入力　詳細は https://github.com/acheong08/ChatGPT#--access-token を参照
ACCESS_TOKEN = "XXXXXXXXX"

```

### データセット

LlamaIndexに読み込ませるデータは`dataset.txt`になっています  
内容は青空文庫の「坊っちゃん」になっていますが、必要に応じて変更してください

## 使い方

下記部分に質問を書きます

`query_engine.query("主人公の家族構成は？")`

下記で実行します

`python revChatGPTLLM.py`

以上

## 結果サンプル

### 出力結果

```
提供された新しい文脈から、主人公の家族構成に関する詳細な情報が明らかになります。主人公の家族構成は以下のようになります：

- おやじ：主人公の父親で、乱暴な性格を持っており、主人公に対して良い感情を抱いておらず、正月に亡くなりました。
- 母：主人公の母親で、病気で亡くなりました。母親は兄を可愛がっており、主人公との仲はあまり良くありませんでした。母は兄が商業学校を卒業した後に亡くなりました。
- 兄：主人公の兄で、主人公とは仲が悪く、喧嘩が絶えない関係でした。兄は九州の会社の支店に赴任するため、家を売却し、家族の財産を片付けて出発しました。兄は主人公に六百円を提供し、その後も五十円を清に渡しました。
- 清（下女）：家族ではないが、十年来の召し使いで、主人公に非常に可愛がっており、お世辞を言ったり贈り物をしたりしています。清は主人公に対して気の毒に思われる存在で、主人公は彼女の態度を不審に思っていました。清は将来の計画を立て、主人公に家を持たせることを夢見ており、主人公に対して賞め言葉をかけています。清は甥の世話もすることを決意し、兄から六百円の資本を提供されました。また、主人公は学校を卒業後、数学の教師として四国の中学校に就職しました。

新たな文脈からは、主人公の家族関係に関する情報に加えて、主人公の出発と別れに関するエピソードも示されています。
```

### 中間データ

https://chat.openai.com/share/0c48ae73-74cd-4896-90a9-06635d66f7f2
