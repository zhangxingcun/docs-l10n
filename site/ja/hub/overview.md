<!--* freshness: { owner: 'kempy' reviewed: '2020-09-14' } *-->

# TensorFlow Hub

TensorFlow Hub は、再利用可能な機械学習用のオープンリポジトリとライブラリです。[tfhub.dev](https://tfhub.dev) リポジトリには、テキスト埋め込み、画像分類モデル、TF.js/TFLite モデルなど、事前トレーニング済みのモデルが多数用意されています。このリポジトリは[コミュニティ貢献者](https://tfhub.dev/s?subtype=publisher)に公開されています。

次のように最小限のコードを使って、[`tensorflow_hub`](https://github.com/tensorflow/hub) ライブラリから前述のモデルをダウンロードし、TensorFlow プログラムで再利用することができます。

```python
import tensorflow_hub as hub

model = hub.KerasLayer("https://tfhub.dev/google/nnlm-en-dim128/2")
embeddings = model(["The rain in Spain.", "falls",
                    "mainly", "In the plain!"])

print(embeddings.shape)  #(4,128)
```

## Next Steps

- [tfhub.dev でモデルを検索する](https://tfhub.dev/)
- [tfhub.dev にモデルを公開する](https://gitlocalize.com/repo/4592/ja/site/en-snapshot/hub/publish.md)
- TensorFlow Hub ライブラリ
    - [TensorFlow Hub をインストールする](https://gitlocalize.com/repo/4592/ja/site/en-snapshot/hub/installation.md)
    - [ライブラリの概要](https://gitlocalize.com/repo/4592/ja/site/en-snapshot/hub/lib_overview.md)
- [チュートリアルを実行する](https://gitlocalize.com/repo/4592/ja/site/en-snapshot/hub/tutorials)