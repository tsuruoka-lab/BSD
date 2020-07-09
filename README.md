# The Business Scene Dialogue corpus
©2020, The University of Tokyo

# Corpus Description

The Japanese-English business conversation corpus, namely Business Scene Dialogue (BSD) corpus, was constructed in 3 steps: 1) selecting business scenes, 2) writing monolingual conversation scenarios according to the selected scenes, and 3) translating the scenarios into the other language. Half of the monolingual scenarios were written in Japanese and the other half were written in English. The whole construction process was supervised by a person who satisfies the following conditions to guarantee the conversations to be natural:
 - has the experience of being engaged in language learning programs, especially for business conversations
 - is able to smoothly communicate with others in various business scenes both in Japanese and English
 - has the experience of being involved in business

We provide balanced training, development and evaluation splits from BSD corpus. The documents in these sets are balanced in terms of scenes and original languages.

# Corpus Statistics


<table>
<thead>
  <tr>
    <th>Scene</th>
    <th>Scenarios</th>
    <th>Sentences</th>
    <th>Scenarios</th>
    <th>Sentences</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td></td>
    <td align="center" colspan="2">JA-EN</td>
    <td align="center" colspan="2">EN-JA</td>
  </tr>
  <tr>
    <td>Face-to-face</td>
    <td align="right">535</td>
    <td align="right">16,481</td>
    <td align="right">458</td>
    <td align="right">14,858</td>
  </tr>
  <tr>
    <td>Phone call</td>
    <td align="right">279</td>
    <td align="right">8,720</td>
    <td align="right">256</td>
    <td align="right">7,770</td>
  </tr>
  <tr>
    <td>General chatting</td>
    <td align="right">233</td>
    <td align="right">7,674</td>
    <td align="right">239</td>
    <td align="right">7,372</td>
  </tr>
  <tr>
    <td>Meeting</td>
    <td align="right">224</td>
    <td align="right">7,647</td>
    <td align="right">265</td>
    <td align="right">8,952</td>
  </tr>
  <tr>
    <td>Training</td>
    <td align="right">37</td>
    <td align="right">1,379</td>
    <td align="right">47</td>
    <td align="right">1,549</td>
  </tr>
  <tr>
    <td>Presentation</td>
    <td align="right">17</td>
    <td align="right">499</td>
    <td align="right">53</td>
    <td align="right">1,899</td>
  </tr>
  <tr>
    <td>Total</td>
    <td align="right">1,325</td>
    <td align="right">42,400</td>
    <td align="right">1,318</td>
    <td align="right">42,400</td>
  </tr>
</tbody>
</table>


# Corpus Structure

The corpus is structured in json format consisting of documents, which consist of sentence pairs. Each sentence pair has a sentence number, speaker name in English and Japanese, text in English and Japanese, original language, scene of the scenario (tag), and title of the scenario (title).

```json
[
	[
		{
			"no": 14,
			"speaker": "Mr. Sam Lee",
			"ja_speaker": "サム リーさん",
			"en_sentence": "Would you guys consider a different scheme?",
			"ja_sentence": "別の事業案も考慮されますか？",
			"original_language": "en",
			"tag": "phone call",
			"title": "Phone: Review spec and scheme"
		},
		...
	],
	...
]
```

## License
Our dataset is released under the [Creative Commons Attribution-ShareAlike (CC BY-SA) license](https://creativecommons.org/licenses/by-sa/4.0/legalcode).

## Reference
If you use this dataset, please cite the following paper:
Matīss Rikters, Ryokan Ri, Tong Li, and Toshiaki Nakazawa (2019). "[Designing the Business Conversation Corpus](https://www.aclweb.org/anthology/D19-5204.pdf)." In Proceedings of the 6th Workshop on Asian Translation, 2019.
```bibtex
@inproceedings{rikters-etal-2019-designing,
    title = "Designing the Business Conversation Corpus",
    author = "Rikters, Mat{\=\i}ss  and
      Ri, Ryokan  and
      Li, Tong  and
      Nakazawa, Toshiaki",
    booktitle = "Proceedings of the 6th Workshop on Asian Translation",
    month = nov,
    year = "2019",
    address = "Hong Kong, China",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/D19-5204",
    doi = "10.18653/v1/D19-5204",
    pages = "54--61"
}
```