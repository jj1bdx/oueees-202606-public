theme: Zurich
footer: Kenji Rikitake / oueees 20260623 topic01
slidenumbers: true
autoscale: true

# oueees-202606 topic 01:

- Internetworking behind AI
- or how to build the gigantic computing infrastructure

<!-- Use Deckset 2.0, 16:9 aspect ratio -->

^ ここ数年、日本語では人工知能と称される、Artificial Intelligence (AI)の発展、およびその技術的社会的影響が話題になっています。今回は、本講義のテーマである「インターネットの情報伝送」の視点から、AIの背後にあるインターネットワーキングあるいは相互接続の技術について、ざっと見ていきます。

---

# Kenji Rikitake

23-JUN-2026
School of Engineering Science, The University of Osaka
On the internet
@jj1bdx

Copyright ©2018-2026 Kenji Rikitake.
This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

^ 講師の力武 健次です。よろしくお願いします。

---

# CAUTION

The University of Osaka School of Engineering Science prohibits copying/redistribution of the lecture series video/audio files used in this lecture series.

大阪大学基礎工学部からの要請により、本講義で使用するビデオ/音声ファイルの複製や再配布は禁止されています。

^ 大阪大学基礎工学部からの要請により、本講義で使用するビデオ/音声ファイルの複製や再配布は禁止されています。ご注意ください。

---

# Lecture notes and reporting

* <https://github.com/jj1bdx/oueees-202606-public/>
* Check out the README.md file and the issues!
* Keyword at the end of the talk
* URL for submitting the report at the end of the talk

^ スライド等が読みにくい場合は、レクチャーノートをご利用ください。

---

# Topic of this video:
# [fit] Internetworking behind AI

^ 今回は、AIの背景にあるインターネットワーキングの技術とはどんなものなのかについて、基本的なことを解説していきます。

---

# What we call AI is a computing service

- ChatGPT, Claude, Gemini are NOT on a single computer; they are *distributed*
- AI is a collective service running on *massive number of clusters of computers*
- Localized AI exists, but the scale is smaller than commercial AI services

^ 私達がAIと普段呼んでいるもの、たとえばOpenAIのChatGPT, AnthropicのClaude, そしてGoogleのGeminiは、単独のコンピュータで動いているわけではなく、分散した複数のコンピュータ上で動いています。これらは大量のコンピュータを集めたクラスタの上で動く集合的サービスとして実現されています。もちろんパソコンや組織内のコンピュータシステム上でローカルに同じようなサービスを実現はできますが、その規模は商用AIサービスに比べて小さくならざるを得ません。

---

# What do AI services actually?

- They compute huge models of neural networks of an undisclosed scale
- They run Large Language Models (LLMs)
- Open-source models include 1-trillion parameters with active 30- to 50-billion ones [^1]


[^1]: [Carolyn Weitz, "Best Open Source LLMs: Benchmarks, Licenses, Local Deployment and Enterprise Use Cases", AceCloud, Last Updated: May 13, 2026](https://acecloud.ai/blog/best-open-source-llms/)

^ AIのサービスは実際に何をやっているのかについて説明します。非常に大きな規模のニューラルネットワークの計算をやっていることは確かですが、著名なAIサービスの多くはその規模を開示していません。その上で走っているのは大規模言語モデル（LLM）の計算です。オープンソースのモデルでもパラメータ数は1兆におよび、そのうち有効なものは30億から50億あるとされています。つまり数十億次元の規模の行列計算をやっているのだと考えると、その複雑さが想像できるでしょう。

---

# What does AI compute for the neural networks?

- Linear algebra + statistical functions
- Equivalent to huge (> 1B x 1B) matrix computation
- Randomization during the computation involves
- *Non-deterministic output for the same input*

^ AIはニューラルネットワークのためにどんな計算をしているのでしょうか。実際には10億次元以上の行列計算に相当する計算を、より小さな行列と統計的関数の計算に分解して行っています。この際結果を固定しないために、計算の過程でランダム化も導入されています。つまり、同じ入力に対して、同じ結果が決定的に返ってくるわけではありません。

---

# Photo and image credits

* All photos and images are modified and edited by Kenji Rikitake
* Photos are from Unsplash.com unless otherwise noted

<!-- Photo and image credits here -->

<!--
Local Variables:
mode: markdown
coding: utf-8
End:
-->
