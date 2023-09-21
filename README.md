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