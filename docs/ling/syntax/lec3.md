# Lec3 Phrase-Structure Rules & Constituency Tests

PS-rules are the formal devices which generate constituent structure, by specifying all and only the possible ways in which categories can combine

## History of Grammar

最古老的传统语法分析：Immediate Constituency Analysis 直接成分分析法。类似初等教育中语文课教的，给句子成分分主谓、述宾、述补、偏正……关系

二十世纪中期的 Formal Science 浪潮中，发生了 a cognitive revolution，诞生了 the computational theory of mind (CTM)。New concept of grammar: grammar is taken as a formal device to generate sentences，被 Chomsky 称为 Finite-State Grammar（正则表达式与有限状态机），后来这个概念被 Shannon 采用进入 EECS。此时此刻计算机学院那边，我同年级的 peers 也在《计算理论》课上听这些吧？我去年就上完了，嘻嘻

然后 Chomsky 说：Human language is not a finite-state language. Finite-State Grammar 在遇到一个 loop 时必然遗忘之前的所有 loop，而人类语言是可以产生 anti-missile missile, anti-(anti-missile missile) missile 这样的串的，即 $anti^n missle^{n+1}$，需要在后一个 loop 时记得前一个 loop 循环了几轮

参考我的[半小时速通 UG 记录](../../blog/posts/ug.md)

## Phrase-Structure Rules

升级改造 finite-state grammar：Phrase-Structure Rules，Generative Grammar。每条 rule / derivation 的箭头左边是句法树里的 mother node，右边是 daughter nodes，这一组 CFG 规则表示的是句法树里每一个 node 可以 dominate 什么样的成分

$$
\begin{cases}
S → NP\ VP \\
NP → N \\
VP → V \\
N → Mary \\
V → runs \\
\end{cases}
$$

non-terminal symbols: 类似 S NP VP N V 这种，出现在句法树的 non-terminal nodes 上的符号

terminal symbols: 类似 Mary runs 这样具体的单词，出现在句法树的 terminal nodes 上

VP → V (NP) (PP) 这样的 rule 中，brankets indicate optional categories

PS-rules provides 3 kinds of information:

* vertical: hierarchical structure
* horizontal: linear precedence
* categorial: the category labels of nodes in a syntax tree

出现在 PS-rules 的某一条 rule 箭头左边的符号，如果出现在另一条 rule 箭头右边，那么这组 PS-rules 可以产生循环的句子，称为 recursion。比如 the box in [the box in [the box in [the box in [the ...]]]]，就是 NP 不断 derivate 出新的 NP。Recursion brings infinity to language.

$$
\begin{cases}
NP → D\ N\ PP\\
PP → Prep\ NP\\
\end{cases}
$$

## Chomsky Hierarchy

当代 AI 还在 finite-state grammar（也就是计算机上的 regular grammar）上运行，事实上 FS grammar 能做的比我们想的多多了。上面的 PS grammar 就是计算机上的 Context Free Grammar，比 FS / regular grammar 要复杂一个等级，而人类语言是不是 PS grammar 能描述的还有待商榷，因此目前基于 FS grammar 的人工智能只能很像地模仿人类语言，不可能完全一样。

strongly / weakly generate: 人和人工智能生成句子的方式

## Constituency Test

不管以后学到什么高深的句法理论，constituency test 永远是判断短语成分的层次关系的唯一标准

diagnotics: 一切分析句法结构的手段，除了 constituency test 之外还包括肉眼观察歧义句等比较不通用的方法

base-generated 基础生成的: certain elements in a sentence are generated or derived directly at the initial stage of sentence formation, before any transformations or movement operations take place，比如我们在初等教育中学英语学到的主动宾、主系表，就是 base-generated，而更细粒度的成分就不算 base-generated 了。

Adjuncts are PPs (e.g. I run on Wednesdays) that do not affect grammaticality, while arguments are selected by the V and must form part of the VP with the V (e.g. John put the car in the garage. As a verb, _put_ categorially selects for a direct-object NP and a locative PP.)

* movement (permutation): Only constituents can be moved as a single unit.
  * wh-test，英语允许用 wh- 开头的特殊疑问词对成分提问。Movement leaves a silent copy, previously called trace (t, 语迹), in the original place. e.g. To whom did the party chairman send a book _t_?
  * topicalization: The fronting of a sentence-internal phrase to the beginning of the sentences. e.g. The new car, Mary hopes that John will like _t_.
  * clefting: the permutation of the order of elements，在英语里就是用 it 形式主语来改语序
* substitution (pronomialization): a pronoun substitutes a entire phrase. e.g. [He] has done [so] too. I 和 so 都是代词，分别代替 NP 和 VP
* deletion (ellipsis): e.g. John can [do sth] and Mary can too.
* conjunction: only constituents of the same type can be coordinated
* fragments: a constituent can serve as a short answer to questions.

Failing in a test does not mean a fragment is not a constituent, but passing a test means the fragment is a constituent. e.g. - What has the president done? - Has resigned. (Wrong reply! Should be "Resigned.", but it is a constituent)

Recoverablity condition: substitution 和 ellipsis 的时候，要求产生的新句子在语义上可以看出什么成分被替换 / 删除了

NP Aux VP 的句子怎么划分？constituency test 表明助动词和 VP 是分开的，但是跟 VP 比跟 NP 更紧密。Aux VP 构成了一个什么词组？后面再细说
