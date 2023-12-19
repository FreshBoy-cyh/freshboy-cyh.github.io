# Lec2 Constituents & Categories

## Lexical / Functional Category

lexical category: 实词

1. open in membership 数量可能增减
2. do not vary greatly across langs
3. typically contentful
4. (at least) one of the syllables is frequently stressed, 程工老师的工字被轻读所以被误认为是工程师

the study of lexical categories concentrate on 4 categories of words, divided according to their binary features [N] and [V]

* N. 名词：[+N, -V]
* V. 动词：[-N, +V]
* Adj. 形容词：[+N, +V]
* P. 介词：[-N, -V]，英语的介词和汉语的不太一样，是有实际意义的，以后会讲

functional category: 虚词，include determiner (D), demonstrative, Num, mood, tense (T), aspect (Asp.), agreement (Agr.，person + gender + number), complementizer (C)

1. closed in membership
2. semantically abstract, denoting mostly grammatical functions
3. vary a lot across langs
4. unstressed

## Diagnotics for Categories

declension: 变格，名词的屈折变化，可能有人称、性、数（agreement）、格（case）……

synthetic/analytic 屈折的/分析的

* morphological criteria: inflection / derivational morphemes
* syntactic criteria: guess the word category from the categories of its context
* phonological criteria: 'increase', 'servey', 'record', which syllable is stressed?
* semantic criteria

Some Cross-Linguistic Comparisons:

* 浙大外院前段时间有亚洲语言研讨会，讨论了东亚的量词语言，认为 agreement + case 和 classifer 的用途是互补的，都是给名词分类。这两类语法范畴永远不出现在同一个语言里
* 汉语单词间的界限不明显，可能是因为汉语没有很复杂的屈折变化来提示单词界限。因此汉语传统的书写系统是没有空格的

## Constituent Structure

Tree Diagram terminologies

* root / terminal (相当于数据结构上说的叶子节点) / non-terminal nodes (neither root nor terminal)
* branch: each single line in a tree diagram
* mother / daughter / grand daughter /sister node
* dominance / constituency: if there exists a continuous decending path from a higher node to a lower one, then we say the higher one dominates the lower one, and the lower one is a constituent of the higher one
* immediate dominance: no other nodes intervenes the higher and lower nodes, e.g. a pair of mother and daughter node

句法树：

$$
\left[_{S}\left[_{NP1}\left[_{N1}Boris\right]\right]\left[_{VP}\left[_{V}talked\right]\left[_{PP1}\left[_{P1}to\right]\left[_{NP2}\left[_{D}the\right]\left[_{N}reporter\right]\right]\right]\left[_{PP2}\left[_{P2}about\right]\left[_{NP3}\left[_{Pronoun}himself\right]\right]\right]\right]\right]
$$

It is not good to use ternary or more complex branch in tree diagrams. We will learn advanced mothods in the future.
