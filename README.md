# how-ai-works

AI가 실제로 어떻게 동작하는지 — 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료 모음입니다.

각 주제는 별도의 레포로 관리되며, 모두 GitHub Pages로 배포되어 있어 설치 없이 바로 실험해 볼 수 있습니다.

> [K-DEVCON AI 스터디](https://k-devcon.com/channel/6/post/563)를 준비하며 만들고 있는 자료들입니다. 계속 추가될 예정입니다.

## 기초

- **[How Normal Distribution Works](https://github.com/dev-jonghoonpark/how-normal-distribution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-normal-distribution-works/)
  - 정규분포와 중심극한정리 — AI 학습에서 종 모양이 자꾸 나오는 이유. 골턴 보드 라이브 시뮬레이션, 점 드래그로 눈으로 확인하는 표준편차(편차²=정사각형 넓이), μ·σ 곡선 조작과 68–95–99.7 규칙, 임의 분포에서 표본 평균 10,000개를 뽑는 CLT 실험, 합성곱으로 계산한 주사위 합의 정확한 분포, 뉴런 가중합 z=Σwx의 히스토그램과 1/√d 스케일링(Xavier/He), MSE = 가우시안 가정까지 직접 실험하는 인터랙티브 교육 자료
- **[How Gradient Descent Works](https://github.com/dev-jonghoonpark/how-gradient-descent-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gradient-descent-works/)
  - 경사 하강법은 왜 지그재그로 움직이는가 — 학습률 하나로 갈리는 수렴·진동·발산의 네 가지 운명, GD/Momentum/Adam 비교 실험실, 지그재그의 축별 분해, 조건수 κ와 학습률의 딜레마, 증상별 진단 가이드까지 직접 실험하는 인터랙티브 교육 자료
- **[How Backprop Works](https://github.com/dev-jonghoonpark/how-backprop-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-backprop-works/)
  - 순전파·손실 함수·역전파 — 필터의 가중치는 어떻게 올바른 값을 찾아가는가. 손실 지형 드래그, 계산 그래프 위에서 한 단계씩 밟아 보는 연쇄 법칙, 실시간으로 사인 곡선을 배우는 신경망, 그리고 난수로 시작한 3×3 합성곱 필터가 손실과 기울기만 보고 소벨 필터로 수렴하는 과정까지 직접 실험하는 인터랙티브 교육 자료
- **[How Convolution Works](https://github.com/dev-jonghoonpark/how-conv-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-conv-work/)
  - 합성곱(Convolution)은 실제로 무엇을 하는가 — "뒤집고·밀고·곱하고·더하기" 수학적 정의부터 임펄스 응답(LTI), 확률분포의 합, 합성곱 정리(DFT 검증), 2D 이미지 필터, 채널과 1×1 conv(ResNet bottleneck의 채널 변환), CNN의 스트라이드·패딩까지 직접 실험하는 인터랙티브 교육 자료

## AlexNet

- **[How AlexNet Works](https://github.com/dev-jonghoonpark/how-alexnet-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alexnet-works/)
  - AlexNet은 실제로 어떻게 동작하는가 — 논문의 실제 conv1 커널과 ILSVRC 이미지로 브라우저에서 직접 계산해 보는 인터랙티브 교육 자료

## ResNet

- **[How ResNet Works](https://github.com/dev-jonghoonpark/how-resnet-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-resnet-work/)
  - ResNet의 동작 원리를 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료
- **[ResNet Bottleneck](https://github.com/dev-jonghoonpark/resnet-bottleneck)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-bottleneck/)
  - ResNet Bottleneck Block에서 1x1 conv의 역할을 설명하는 인터랙티브 페이지
- **[ResNet의 BatchNorm](https://github.com/dev-jonghoonpark/resnet-batchnorm)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-batchnorm/)
  - 깊은 네트워크는 왜 배치 정규화가 필요한가 — 정규화 개념부터 BN 수식과 γ·β 분포 데모, 역전파에서 γ·β·W가 업데이트되는 플로우 단계별 시각화, ResNet 블록 안에서 BN의 위치, 브라우저에서 직접 계산하는 30층 신호 전파 시뮬레이션(BN·skip 토글), 학습 vs 추론 모드와 BN folding까지 다루는 페이지
- **[How Dilated Convolution Works](https://github.com/dev-jonghoonpark/how-dilated-conv-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-dilated-conv-works/)
  - Dilated Convolution은 어떻게 풀링 없이 시야를 넓히는가 (Yu & Koltun, ICLR 2016) — 풀링이 분할 마스크를 뭉개는 과정, 확장률에 따른 커널 읽기 위치, 수용 영역의 지수적 확장(논문 Figure 1 재현), 컨텍스트 모듈(Table 1), 무작위 vs 항등 초기화 신호 전파 비교(ResNet과 같은 "항등 근처에서 시작" 논리), gridding effect까지 직접 실험하는 인터랙티브 교육 자료

## N-gram

- **[How N-gram Works](https://github.com/dev-jonghoonpark/how-n-gram-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-n-gram-work/)
  - 세는 것만으로 언어를 예측하는 n-gram 언어 모델 — 편집 가능한 코퍼스로 카운트 행렬, 텍스트 생성, 희소성, 스무딩, 퍼플렉시티까지 직접 실험하는 인터랙티브 교육 자료

## RNN

- **[How RNN Works](https://github.com/dev-jonghoonpark/how-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-works/)
  - RNN 부흥기(2014–2016)를 따라가는 인터랙티브 노트 — 브라우저에서 직접 학습하는 min-char-rnn, LSTM 게이트 조작기, 선택적 드롭아웃 시각화, Deep Speech 2 빔서치 시뮬레이터, 이해도 퀴즈까지

## seq2seq

- **[How seq2seq Works](https://github.com/dev-jonghoonpark/how-seq2seq-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-seq2seq-works/)
  - seq2seq(2014)의 동작 원리 — 인코더·디코더 애니메이션, 고정 길이 병목, 입력 역순 트릭, 브라우저에서 직접 학습하는 미니 LSTM seq2seq(순방향 vs 역순 A/B 실험), 학습된 모델로 돌리는 빔 서치와 퀴즈까지

## Transformer

- **[How Attention Works](https://github.com/dev-jonghoonpark/how-attention-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-attention-works/)
  - Attention Is All You Need — seq2seq 병목과 Bahdanau attention부터 Q·K·V, causal mask, 멀티헤드, 위치 인코딩, Pointer Networks까지 12개 데모와 퀴즈로 직접 실험하며 배우는 인터랙티브 교육 자료
