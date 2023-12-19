# Lec4 X' Theory

## Why we need X' Theory

评价语法的标准：

* descriptive / explanatory adequacy 描写/解释充分性，可以解释一门语言的句法，和更加普遍的句法
* endocentric / exocentric 向/离心结构，也就是 XP 里有没有 X（称为 head）成分

之前学的 PS rules 是描写充分的，但不符合解释充分性的要求。它只能描述英语（language-specific），对每种成分都要编写互相无关联的规则（construction-specific），而且不能解释句法背后的心理机制。解释充分性的句法应满足：

* universal
* maximally constrained
* psychologically plausible

X' theory (read as "X-bar theory"，中文叫 X 阶标理论) 是解释充分性的语法，所有语言，所有词类都有类似的规则。X' theory 有 endocentricity（向心性），every phrase should have a head；而理论上 PS rule 并没有限制 NP → V AP 这种荒谬的句法不能出现在其中，它是 exocentric 的。此外，X' theory 通过区分 specifer 和 complement，解决了 PS rules 出现三分支甚至多分支的情况。所以 X' theory 解决了 PS rules 的短板。

X' theory 的句法树：$XP→ZP\ [_{X'}X\ YP]$。其中 X 叫中心语（head），可以是 V、N 等任意词类；ZP 是标志语（specifier / modifier），可简写为 Spec；YP 是补足语（complement）。Specifier 表示冠词、very 等联系相对不紧密的修饰语，一般可省略，起到一个造型上的作用；complement 一般不可省略，省掉之后语义就大变样了，而且 typically the arguments are categorially selected (C-selected，语类选择) by the head，比如说 X 是及物动词，那么它后面跟的 complement 的词性就得是 NP。这种词类搭配的规则叫 categorial features，而 XP 的 categorial features 和下面的 X'、X 必须一样，这种现象叫做 the projection of categorial features。因为 projection 的存在，所以有了这些术语：XP is the maximal projection of X, X' is the intermidiate projection of X, X is the minimal projection (head) of X' and XP。

lexicon 词库: the mental dictionary containing idiosyncratic information about the words in a language

e.g. a book of poems，PP 是 complement；a book with blue cover，PP 是 specifier / modifier。用 constituent test 来验证到哪里算是 XP，其中哪些是联系更紧密的 X'，哪些可以丢到 specifier 里

如果一个短语有多个 complement 怎么办？规定 X' 也可以继续分化出 X'，例如：$NP→[_Dthe][_{N'}[_{N'}[_Nbook][_{PP}of\ stories]][_{PP}with\ the\ blue\ cover]].$

## Functional Categories: The Structure of the Clause

这一节讲的问题是，X' theory 对 NP、VP、AP、PP 显然适用，那么它是否可以解释句子和从句？

首先解决 Aux VP 结构，沿着这样的思路尝试用 X' theory 解释 Aux VP：

1. 最原始的，S→NP Aux VP，这不符合 X' schema
2. 也许 Aux 是 specifier V'，而 VP 是 V'？不对，specifier 应该是 optional 的，助动词有没有会严重影响表意；VP 的行为比起 X' 更像 XP；此外，auxiliaries carry sentential information regarding negation and interrogatives，而 Spec V' 不是句子层次的结构
3. 也许可以把句子视为 AuxP，那么就可以得到符合 X' schema 的句法树 $AuxP→NP\ [_{Aux'}Aux\ VP]$。但是把助动词当成句子的中心成分，显然高估了其地位
4. 把 AuxP 重新解释成 TP，其中 T 表示 tense，就合理多了。

最终我们对陈述语序的句子的解释是：$TP→NP[_{T'}T\ VP]$，所有语言的每个句子都有一个全局的 tense，英语里的 tense 有 past 和 non-past 两种。$[_{TP}[_{NP}he][_{T'}[_Tshould][_{VP}talk\ to\ this\ man]]]$

对从句、疑问句的解释：它们都是补语化成分（complementizer）短语，CP → Comp TP，从句的引导词和疑问句的一般疑问词。Comp（C）的取值可分为 ±Q，表示该引导词是否有疑问语义，比如 whether、that 分别属于 +Q 和 -Q。写成 X' theory 的形式是 $CP→ZP\ [_{C'}C\ TP]$。e.g.

* 从句：$CP→Spec\ [_{C'}[_{C[-Q]}for]\ [_{TP}John\ to\ leave]].$
* 疑问句：$CP→[_{Spec}who][_{C'}[_{C[+Q]}did][_{TP}Mary\ t\ see\ t]]?$

对 non-finite (infinitival) clause 的解释：T 可以取值 -T，表示没有 tense，并且导致 PRO subject，比如 $John\ tried\ [_{S'}[_{TP}[_{NP}PRO_i][_{T'}[_{T}to][_{VP}leave]]]]$。这里的 PRO 用来描述存在 pronoun dropping 现象的句法，表示一个空代词。下标 i 是 co-indexation 标记，表示的是 named entity（终于和 NLP 的知识串起来了！），一个句子中所有下标相同的 constituents 表示的是同一个 co-indexation。

不定式从句还可以根据 PRO subject 指代的对象分为不同的 control sentence：

* Subject control: $John_i\ tried\ [_{S'}[_{TP}PRO_i\ to\ leave]]$
* Object control: $John_i\ persuaded\ Bill_j\ [_{S'}[_{TP}PRO_j\ to\ leave]]$
* Arbitrary control: $It\ is\ difficult\ [_{S'}[_{TP}PRO\ to\ leave]]$

对 Gerundive clause 的解释（gerund 是动名词）：$John\ dislikes\ [_{S'}[_{TP}PRO_i\ eating\ in\ public.]]$

## Adjuncts in X' theory

In X-bar theory, a structural distinction between arguments and adjuncts can be properly represented. We can treat arguments as sister of X (complement), and adjuncts as sister of X' (specifier). 而在 PS rule 中，不管是 argument 还是 adjunct 都是 sister，由 XP 直接分化出来，体现不出我们在 constituent test 中发现的规律：XP 中的 argument 比起 adjunct 跟 head 的关系更紧密

英语有两种从句，差别体现在句法上就是从句算 adjunct 还是 argument：

* 补足语从句 complement clause：$NP→[_{Spec}the][_{N'}[_Nsuggestion][_{CP}that\ John\ should\ resign]]$
* 关系从句 relative clause：$NP→[_{Spec}the][_{N'}[_{N'}[_Nsuggestion]][_{CP}that\ John\ made]]$
