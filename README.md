# lexica
Ongoing list of useful lexica in Computational Social Science

`stress_1grams_fbtw.csv`: `Guntuku, S. C., Buffone, A., Jaidka, K., Eichstaedt, J. C., & Ungar, L. H. (2019, July). Understanding and measuring psychological stress using social media. In Proceedings of the International AAAI Conference on Web and Social Media (Vol. 13, No. 01, pp. 214-225).`

Stress score = weight of word in lex * normalized word frequency. 
This lexicon was built on user-level language and evaluated with users with at least 500 words. 
In that scenario, the net score (weight of word in lex * normalized word frequency) ranges from 0-40 (where 40 is most stressed). 

When applied to individual tweets, the absolute value of the score is hard to interpret and can be unreliable. 
but the scores might provide a rough indication of stress-associated language. 

```
@inproceedings{guntuku2019understanding,
  title={Understanding and measuring psychological stress using social media},
  author={Guntuku, Sharath Chandra and Buffone, Anneke and Jaidka, Kokil and Eichstaedt, Johannes C and Ungar, Lyle H},
  booktitle={Proceedings of the International AAAI Conference on Web and Social Media},
  volume={13},
  number={01},
  pages={214--225},
  year={2019}
}
```

`lonely_lex.csv`: `Guntuku, S. C., Schneider, R., Pelullo, A., Young, J., Wong, V., Ungar, L., ... & Merchant, R. (2019). Studying expressions of loneliness in individuals using twitter: an observational study. BMJ open, 9(11).`

Estimates (word_weight in lexica * normalized frequency of word per user) indicate probability of loneliness expressions - higher score represents a higher probability. 

For each user in your target dataset, extract frequencies of unigram tokens relative to the total number of words per user (i.e., freq(token_user) / num_tokens_user). For each word, multiply this relative frequency by the weight of the word in the lexicon, and then sum this value over all words used by the user. The resulting score is the loneliness estimate for that user.   

```
@article{guntuku2019studying,
  title={Studying expressions of loneliness in individuals using twitter: an observational study},
  author={Guntuku, Sharath Chandra and Schneider, Rachelle and Pelullo, Arthur and Young, Jami and Wong, Vivien and Ungar, Lyle and Polsky, Daniel and Volpp, Kevin G and Merchant, Raina},
  journal={BMJ open},
  volume={9},
  number={11},
  year={2019},
  publisher={British Medical Journal Publishing Group}
}
```
