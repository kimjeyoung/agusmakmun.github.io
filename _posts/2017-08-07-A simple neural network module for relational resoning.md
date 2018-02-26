---
layout: post
title:  "A simple neural network module for relational reasoning"
date:   2017-08-07 00:18:23 +0700
categories: [deeplearning]
---

### Implement Paper
A simple neural network module for relational reasoning(Adam Santoro et al., 2017) [논문 링크][1]

이번에 리뷰할 논문은 Deepmind의 논문이며 관계추론 모델을 효율적으로 제시한 논문입니다. 

관계추론(Relation Reasoning)이란 객체를 단순히 기호(문자열, 단어)로만 인식하는 것이 아니라 주어진 환경을 이해하고 인식하는 것입니다. Relation Reasoning 은 예전부터 연구되어져 왔고 Symbolic 방식과 Statistic 방식으로 문제를 해결하려 했습니다.

하지만 Symbolic 방식의 접근은 에이전트가 실제환경에 적용되지 못하는 단점과 작은 데이터셋에서 robust 하지 못하다는 단점을 가지며 
Statistic 방식의 접근은 딥러닝에서 흔히 발생할 수 있는 data-poor problem 의 단점을 지닙니다. 

그렇다면 이 논문에서는 어떠한 방식으로 문제를 해결하려 했을까요??

우선 관계추론을 어디에 적용할 수 있는지 알아보겠습니다. 

![Screenshot broadcast](https://kimjeyoung.github.io/master/static/img/_posts/CLEVR.png  "Screenshot broadcast")

[1]: https://arxiv.org/abs/1706.01427
