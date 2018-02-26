---
layout: post
title:  "A simple neural network module for relational reasoning"
date:   2017-08-07 00:18:23 +0700
categories: [deeplearning]
image: CLEVR.jpg
---

### Implement Paper
A simple neural network module for relational reasoning(Adam Santoro et al., 2017) [논문 링크][1]

이번에 리뷰할 논문은 Deepmind의 논문이며 관계추론 모델을 효율적으로 제시한 논문입니다. 

관계추론(Relation Reasoning)이란 객체를 단순히 기호(문자열, 단어)로만 인식하는 것이 아니라 주어진 환경을 이해하고 인식하는 것입니다. Relation Reasoning 은 예전부터 연구되어져 왔고 Symbolic 방식과 Statistic 방식으로 문제를 해결하려 했습니다.

하지만 Symbolic 방식의 접근은 에이전트가 실제환경에 적용되지 못하는 단점과 작은 데이터셋에서 robust 하지 못하다는 단점을 가지며 
Statistic 방식의 접근은 딥러닝에서 흔히 발생할 수 있는 data-poor problem 의 단점을 지닙니다. 

그렇다면 이 논문에서는 어떠한 방식으로 문제를 해결하려 했을까요??

우선 관계추론을 어디에 적용할 수 있는지 알아보겠습니다. 

![CLEVR](https://raw.githubusercontent.com/kimjeyoung/kimjeyoung.github.io/master/static/img/_posts/CLEVR.jpg  "CLEVR"){: .center-image }

위의 이미지([Data set of CLEVR][2]) 를 보면 다양한 모형들이 존재합니다. 일반적인 분류문제를 예로 든다면 빨간 직육면체가 존재하니? 등을 예로 들 수 있지만
관계추론의 경우 환경과의 상호적인 관계에 대해 추론하는 것을 뜻합니다. 예를 들면 파란색 정육면체 뒤에 있는 도형은 어떤 색을 가지고 있니? 등 이미지 안에서 object 간의 관계를 통해서 답을 유추해 해는 것을 뜻합니다.

이 논문에서는 CLEVR 데이터셋을 사용하였고 이는 각각의 도형들의 집합들이 이미지안에 존재합니다.



[1]: https://arxiv.org/abs/1706.01427
[2]: https://cs.stanford.edu/people/jcjohns/clevr/