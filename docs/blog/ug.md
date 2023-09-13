# UG in Half an Hour 半小時速通普遍語法

大二春夏學期的一個晚上，《當代語言學》還有半小時下課，但是我已經沒力氣聽了。發消息問芭蕉這時候可以幹什麽打發時間，芭蕉建議我試試半小時速通 Chomsky 先生的 universal grammar，並且把 pdf 格式的原著發給了我。然後我一邊看書，一邊飛速敲鍵盤整理思路，就有了這份速通筆記。

## Introduction

跟 TCS 一樣用集合的視角看待自然語言，Syntax 的意義在於找到 grammar 來生成某語言中的所有句子。Grammar 是基於規則的，不能用 high order of statistical approximation to English 來替代。（喬聖最近也用這個理由反對了 ChatGPT 誒，他那時候就預見到 LLM 會橫掃語言學了？）

## Basic Syntax

DFA & Regular Language

謂詞邏輯，但我們不管其中的語義，只管它 CFG 的形式

## Phrase Structure & its Limitation

自然語言的 CFG（以英語為例）構成語法的基礎部分

但這樣描述自然語言的工具還是不能產生所有合理的句子，故引入 a more powerful model combining phrase structure and grammatical transformation（ToC 意義上的 grammar）嘗試修正，得到“轉換-生成文法”

## On the Goals of Linguistic Theory

從一般語法中歸納出 UG 理論。對 UG 的期望由強至弱：

* 能通過 UG 自動化地從語料庫中歸納語法
* 能用 UG 自動化判定一個語法是否最優地總結了語料庫中的句子
* 能用 UG 自動化判定兩個語法中哪個更符合語料庫中的句子

## The Explanary Power of Linguistic Theory

應該研究語言能力，而不是描述語言行為
