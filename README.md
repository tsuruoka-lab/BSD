# The Business Scene Dialogue corpus
©2020, The University of Tokyo

# Corpus Description

The Japanese-English business conversation corpus, namely Business Scene Dialogue (BSD) corpus, was constructed in 3 steps: 1) selecting business scenes, 2) writing monolingual conversation scenarios according to the selected scenes, and 3) translating the scenarios into the other language. Half of the monolingual scenarios were written in Japanese and the other half were written in English. The whole construction process was supervised by a person who satisfies the following conditions to guarantee the conversations to be natural:
 - has the experience of being engaged in language learning programs, especially for business conversations
 - is able to smoothly communicate with others in various business scenes both in Japanese and English
 - has the experience of being involved in business

We provide balanced training, development and evaluation splits from BSD corpus. The documents in these sets are balanced in terms of scenes and original languages. In this repository we publicly share the full development and evaluation sets and a part of the training data set.

|        	| Training 	| Development 	| Evaluation 	|
|--------	|---------:	|:-----------:	|:----------:	|
| Sentences |   20,000 	|       2,051 	|      2,120 	|
| Scenarios |   670 	|       69	 	|      69	 	|

# Corpus Statistics


<table>
<thead>
  <tr>
    <th>Data Set</th>
    <th>Scene</th>
    <th>Scenarios</th>
    <th>Sentences</th>
    <th>Scenarios</th>
    <th>Sentences</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td align="center" colspan="2"></td>
    <td align="center" colspan="2">JA-EN</td>
    <td align="center" colspan="2">EN-JA</td>
  </tr>
  <tr>
    <td rowspan="7">Training</td>
    <td>Face-to-face</td>
    <td align="right">122</td>
    <td align="right">3525</td>
    <td align="right">103</td>
    <td align="right">2986</td>
  </tr>
  <tr>
    <td>Phone call</td>
    <td align="right">68</td>
    <td align="right">1944</td>
    <td align="right">75</td>
    <td align="right">2175</td>
  </tr>
  <tr>
    <td>General chatting</td>
    <td align="right">61</td>
    <td align="right">1915</td>
    <td align="right">72</td>
    <td align="right">1883</td>
  </tr>
  <tr>
    <td>Meeting</td>
    <td align="right">56</td>
    <td align="right">1964</td>
    <td align="right">58</td>
    <td align="right">1787</td>
  </tr>
  <tr>
    <td>Training</td>
    <td align="right">12</td>
    <td align="right">562</td>
    <td align="right">19</td>
    <td align="right">463</td>
  </tr>
  <tr>
    <td>Presentation</td>
    <td align="right">6</td>
    <td align="right">607</td>
    <td align="right">18</td>
    <td align="right">189</td>
  </tr>
  <tr>
    <td>Total</td>
    <td align="right">325</td>
    <td align="right">10,000</td>
    <td align="right">345</td>
    <td align="right">10,000</td>
  </tr>
  <tr>
    <td rowspan="7">Development</td>
    <td>Face-to-face</td>
    <td align="right">11</td>
    <td align="right">319</td>
    <td align="right">12</td>
    <td align="right">314</td>
  </tr>
  <tr>
    <td>Phone call</td>
    <td align="right">6</td>
    <td align="right">176</td>
    <td align="right">7</td>
    <td align="right">185</td>
  </tr>
  <tr>
    <td>General chatting</td>
    <td align="right">7</td>
    <td align="right">223</td>
    <td align="right">8</td>
    <td align="right">248</td>
  </tr>
  <tr>
    <td>Meeting</td>
    <td align="right">7</td>
    <td align="right">240</td>
    <td align="right">7</td>
    <td align="right">219</td>
  </tr>
  <tr>
    <td>Training</td>
    <td align="right">1</td>
    <td align="right">40</td>
    <td align="right">1</td>
    <td align="right">23</td>
  </tr>
  <tr>
    <td>Presentation</td>
    <td align="right">1</td>
    <td align="right">31</td>
    <td align="right">1</td>
    <td align="right">33</td>
  </tr>
  <tr>
    <td>Total</td>
    <td align="right">34</td>
    <td align="right">997</td>
    <td align="right">35</td>
    <td align="right">1054</td>
  </tr>
  <tr>
    <td rowspan="7">Evaluation</td>
    <td>Face-to-face</td>
    <td align="right">12</td>
    <td align="right">381</td>
    <td align="right">11</td>
    <td align="right">345</td>
  </tr>
  <tr>
    <td>Phone call</td>
    <td align="right">6</td>
    <td align="right">163</td>
    <td align="right">7</td>
    <td align="right">212</td>
  </tr>
  <tr>
    <td>General chatting</td>
    <td align="right">7</td>
    <td align="right">211</td>
    <td align="right">8</td>
    <td align="right">212</td>
  </tr>
  <tr>
    <td>Meeting</td>
    <td align="right">7</td>
    <td align="right">228</td>
    <td align="right">7</td>
    <td align="right">229</td>
  </tr>
  <tr>
    <td>Training</td>
    <td align="right">1</td>
    <td align="right">38</td>
    <td align="right">1</td>
    <td align="right">30</td>
  </tr>
  <tr>
    <td>Presentation</td>
    <td align="right">1</td>
    <td align="right">31</td>
    <td align="right">1</td>
    <td align="right">40</td>
  </tr>
  <tr>
    <td>Total</td>
    <td align="right">34</td>
    <td align="right">1052</td>
    <td align="right">35</td>
    <td align="right">1068</td>
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
Our dataset is released under the [Creative Commons Attribution-NonCommercial-ShareAlike (CC BY-NC-SA) license](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en).

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

## Acknowledgements
This work was supported by "Research and Development of Deep Learning Technology for Advanced Multilingual Speech Translation", the Commissioned Research of National Institute of Information and Communications Technology (NICT), JAPAN.
