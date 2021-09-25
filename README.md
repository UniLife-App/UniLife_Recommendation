# UniLife_Recommendation

import:

import numpy as np

import pandas as pd

from collections import defaultdict

from sklearn.metrics.pairwise import paired_distances,cosine_similarity


接ＤＢ：

articles = pd.read_csv(r"Article_test1.csv")

articles.drop(columns="genres",inplace=True)

df = pd.read_csv(r"Article_Rating_test1.csv")

df = pd.merge(df, articles, on='ArticleId')


input:

recommend(userId,推薦篇數)


output:

Article ID List--[215, 70, 111, 31, 196]
