# how-ai-works

AI가 실제로 어떻게 동작하는지 — 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료 모음입니다.

각 주제는 별도의 레포로 관리되며, 모두 GitHub Pages로 배포되어 있어 설치 없이 바로 실험해 볼 수 있습니다.

> [K-DEVCON AI 스터디](https://k-devcon.com/channel/6/post/563)를 준비하며 만들고 있는 자료들입니다. 계속 추가될 예정입니다.

## 📖 용어 사전

- **[dictionary.md](dictionary.md)**
  - 자료를 읽다 막히는 용어를 정리합니다.

## 기초

- **[How Mean and Variance Works](https://github.com/dev-jonghoonpark/how-mean-and-variance-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mean-and-variance-works/)
  - 평균과 분산에서 정규화 층까지 — LRN과 BatchNorm을 이해하는 데 필요한 것들. 편차 합이 왜 항상 0이고 왜 절댓값이 아니라 제곱인지, Min-Max와 Z-score가 **둘 다 아핀 변환이라 모양은 똑같이 보존된다**는 오해 깨기, 그럼에도 정규화 층이 z-score를 쓰는 진짜 이유(표본을 늘리면 범위는 2.1σ→6.5σ로 발산하지만 σ는 1.00으로 수렴), 칸을 클릭해 확인하는 (N,C,H,W) 축 선택기(BN·LN·IN·GN·LRN이 전부 같은 수식이고 축만 다르다는 것), 한 채널을 키우면 이웃이 눌리는 LRN 측면 억제 계산기, γ·β의 존재 이유, σ/√m을 그대로 재현하는 배치 크기별 통계 흔들림, 그리고 VGG의 재현 실패와 BatchNorm 등장으로 LRN이 사라진 경위까지 직접 실험하는 인터랙티브 교육 자료
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
- **[ResNet DJL Lab](https://github.com/dev-jonghoonpark/resnet-djl-lab)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-djl-lab/)
  - v1과 v2의 차이는 새로운 연산이 아니라 **BN·ReLU·덧셈의 순서** 하나다 — DJL(Deep Java Library) 블록 API로 두 버전을 직접 구현해 파라미터 수를 torchvision·논문 값과 대조하고(ImageNet-18 11,689,512 / CIFAR-20 0.27M 정확히 일치), 잔차 경로의 conv 가중치를 0으로 만들면 출력이 입력과 **비트 단위로** 같아지는 항등 사상을 테스트로 증명한다. 배포된 페이지는 여기서 한 걸음 더 들어가, **고양이 사진 한 장이 순전파 → 손실 → 역전파 → 가중치 갱신 → 재순전파를 한 바퀴 도는 동안 실제로 나온 값**을 80단계 전부 받아 적은 것이다 — 단계마다의 특징 맵·값 범위·0이 된 칸의 비율, conv 출력 한 칸을 만드는 곱셈 27개, BatchNorm의 μ·σ²·γ·β 대입, 평균 풀링 64칸, Linear 내적 64항, `dL/dz = softmax(z) − onehot`, SGD 한 스텝의 `w − lr(g + wd·w)`까지 전부 Java에서 손으로 다시 계산해 엔진 값과 나란히 싣는다(그래디언트 640개를 뺀 나머지는 차이 0). v1/v2 토글로 post-activation과 pre-activation이 같은 이미지에서 어떻게 갈라지는지 볼 수 있다
- **[How Dilated Convolution Works](https://github.com/dev-jonghoonpark/how-dilated-conv-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-dilated-conv-works/)
  - Dilated Convolution은 어떻게 풀링 없이 시야를 넓히는가 (Yu & Koltun, ICLR 2016) — 풀링이 분할 마스크를 뭉개는 과정, 확장률에 따른 커널 읽기 위치, 수용 영역의 지수적 확장(논문 Figure 1 재현), 컨텍스트 모듈(Table 1), 무작위 vs 항등 초기화 신호 전파 비교(ResNet과 같은 "항등 근처에서 시작" 논리), gridding effect까지 직접 실험하는 인터랙티브 교육 자료

## N-gram

- **[How N-gram Works](https://github.com/dev-jonghoonpark/how-n-gram-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-n-gram-work/)
  - 세는 것만으로 언어를 예측하는 n-gram 언어 모델 — 편집 가능한 코퍼스로 카운트 행렬, 텍스트 생성, 희소성, 스무딩, 퍼플렉시티까지 직접 실험하는 인터랙티브 교육 자료

## 단어 임베딩

- **[How word2vec Works](https://github.com/dev-jonghoonpark/how-word2vec-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-word2vec-works/)
  - word2vec은 어떻게 "king − man + woman ≈ queen"을 만드는가 — 원-핫의 직교성 문제와 분포 가설, 윈도우로 학습 쌍 만들기(CBOW vs Skip-gram), 은닉층 없는 행렬 두 개, 소프트맥스 병목을 푸는 계층적 소프트맥스(허프만 트리 경로 시각화)와 네거티브 샘플링, 빈도의 3/4 제곱 노이즈 분포, 서브샘플링 곡선, **브라우저에서 실제로 도는 SGNS 학습기**(주성분 2D 단어 지도·손실 곡선·최근접 이웃)와 방금 학습한 벡터로 계산하는 유추 계산기, 구(phrase) 병합 점수까지 직접 실험하는 인터랙티브 교육 자료

## RNN

- **[How RNN Works](https://github.com/dev-jonghoonpark/how-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-works/)
  - RNN 부흥기(2014–2016)를 따라가는 인터랙티브 노트 — 브라우저에서 직접 학습하는 min-char-rnn, LSTM 게이트 조작기, 선택적 드롭아웃 시각화, Deep Speech 2 빔서치 시뮬레이터, 이해도 퀴즈까지
- **[How char-rnn Works](https://github.com/dev-jonghoonpark/how-char-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-char-rnn-works/)
  - Karpathy 「The Unreasonable Effectiveness of Recurrent Neural Networks」(2015) 한국어 인터랙티브 해설 — 다섯 가지 시퀀스 처리 방식, step() 한 줄을 손으로 따라가기, 역전파 한 번에 확신도가 오르는 "hello" 실험실(순환 연결을 끊으면 손실이 이론적 하한에 갇힌다), PG·셰익스피어·위키백과·LaTeX·리눅스 다섯 실험의 설정과 실수, 온도 슬라이더, 브라우저에서 학습하는 아기 이름 생성기, 반복 100→4,000 샘플의 진화를 직접 재현하는 셰익스피어 LSTM, 예측 히트맵, 해석 가능한 셀을 상관계수로 찾아내는 셀 탐색기까지 직접 실험하는 인터랙티브 교육 자료
- **[How LSTM Works](https://github.com/dev-jonghoonpark/how-lstm-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-lstm-works/)
  - LSTM은 어떻게 기억하는가 — 야코비안이 반복 곱해지며 생기는 기울기 소멸(λ^k vs f^k 로그 차트), 원소별 곱·덧셈만 지나는 셀 상태 레일, 망각·입력·갱신·출력 4단계 다이어그램, 게이트 조작기(유지·덮어쓰기·지우기·누적), 사람이 직접 심은 가중치로 괄호 깊이를 세는 LSTM 실행기, 핍홀·결합 게이트·GRU 변형과 파라미터 비교(4:3:1), 퀴즈 7문항까지 직접 실험하는 인터랙티브 교육 자료
- **[How RNN Dropout Works](https://github.com/dev-jonghoonpark/how-rnn-dropout-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-dropout-works/)
  - 드롭아웃은 왜 순환 연결을 피해 가는가 (Zaremba, Sutskever & Vinyals, 2015) — 시간 축으로 펼친 격자에서 세로(비순환)와 가로(순환) 연결 구분, 수식 위 `D(h_t^{l-1})`의 위치, 정보가 손상되는 횟수를 직접 세는 논문 Figure 2·3 재현(**L+1** vs **L+1+Δt**)과 경로 생존 확률 로그 차트, 35스텝을 건너는 유닛 200개의 몬테카를로 생존 시뮬레이션, n=4 미니 LSTM 한 스텝을 실제로 계산하며 보는 게이트 손상, PTB 퍼플렉시티 114.5→78.4와 음성·번역 결과, Gal & Ghahramani·Zoneout의 마스크 샘플링 비교와 PyTorch 구현 주의점까지 직접 실험하는 인터랙티브 교육 자료
- **[LSTM Text Generation](https://github.com/dev-jonghoonpark/lstm-text-generation)** · 💻 내 컴퓨터에서 실행
  - 앞의 브라우저 자료들로 원리를 봤다면, 이번엔 직접 학습시켜 보는 쪽 — 정글북 원문으로 문자 단위 LSTM을 돌려 다음 한 글자를 예측하게 만드는 Keras 실습. 학습 데이터 (앞 60자 → 다음 1자) 쌍이 사람 손 없이 27,297개 만들어지는 과정, 2 epoch(`trann`·`brtong`)에서 50 epoch(`the monkeys`·`man-cun`)로 가며 실제로 달라지는 생성 결과, loss 0.5949에서 곡선이 평평해지는 것을 보고 "epoch를 더 늘릴지 `step`을 낮출지" 판단하는 법까지. 원-핫을 밀집 배열로 펼치면 왜 800MB가 되는지, `temperature`가 분포에 무엇을 하는지도 코드에서 짚는다. Python for Microscopists 167번 영상의 예제를 최신 라이브러리에서 돌아가게 고치고(`np.bool` 제거, `.keras` 저장, 동작하지 않던 `temperature` 복원 등 9곳) 한국어 해설을 붙였다 세로(비순환)와 가로(순환) 연결 구분, 수식 위 `D(h_t^{l-1})`의 위치, 정보가 손상되는 횟수를 직접 세는 논문 Figure 2·3 재현(**L+1** vs **L+1+Δt**)과 경로 생존 확률 로그 차트, 35스텝을 건너는 유닛 200개의 몬테카를로 생존 시뮬레이션, n=4 미니 LSTM 한 스텝을 실제로 계산하며 보는 게이트 손상, PTB 퍼플렉시티 114.5→78.4와 음성·번역 결과, Gal & Ghahramani·Zoneout의 마스크 샘플링 비교와 PyTorch 구현 주의점까지 직접 실험하는 인터랙티브 교육 자료

## 음성 인식 (Deep Speech 2)

- **[How Row Convolution Works](https://github.com/dev-jonghoonpark/how-row-convolution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-row-convolution-works/)
  - 행 합성곱(row convolution)은 어떻게 미래를 엿보는가 (Amodei et al., 2015 · 3.7절) — 양방향 RNN이 "말이 끝나야" 시작하는 문제를 세 구조 실시간 재생으로 비교, `/t/` vs `/d/`의 판별 증거가 늦게 도착해 lookahead를 늘려야 예측이 뒤집히는 과정, 식 (11)을 칸 클릭으로 직접 전개하며 확인하는 채널 비혼합(= depthwise 1D conv), τ·스텝 상수 지연 예산(논문 τ=19 · 40ms → 760ms), 채널을 섞었다면 파라미터가 정확히 d배(2,560배) 늘어 순환 스택 전체보다 커지는 계산, lookahead를 여러 층에 나누면 지연이 누적되는 이유, 근사가 양방향보다 CER이 낮았던 배포 결과까지 직접 실험하는 인터랙티브 교육 자료
- **[How CTC Beam Search Works](https://github.com/dev-jonghoonpark/how-ctc-beam-search-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ctc-beam-search-works/)
  - 빔 서치는 무엇을 찾고 있는가 — DS2의 디코딩(3.8절·7.3절) — CTC 축약 2단계와 blank가 글자 경계를 만드는 이유, 4,096개 정렬 전수 열거로 드러나는 greedy의 실패(`"ct"` 0.204 vs `"cat"` 0.425), 접두사마다 `p_b`/`p_nb`를 따로 드는 이유와 **프레임 단위 prefix beam search 스텝 실행기**, 빔 폭 1→50의 포화(폭 2부터 정답·20에서 전수 열거와 100% 일치), `Q(y) = log p_ctc + α log p_lm + β·단어수`의 세 항을 α·β 슬라이더로 뒤집어 보는 재순위와 β가 없으면 단어를 빠뜨리는 이유, 배포 가지치기가 논문의 120만 회 → 8,000회 = 150배를 그대로 재현하는 계산기까지 직접 실험하는 인터랙티브 교육 자료

## seq2seq

- **[How seq2seq Works](https://github.com/dev-jonghoonpark/how-seq2seq-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-seq2seq-works/)
  - seq2seq(2014)의 동작 원리 — 인코더·디코더 애니메이션, 고정 길이 병목, 입력 역순 트릭, 브라우저에서 직접 학습하는 미니 LSTM seq2seq(순방향 vs 역순 A/B 실험), 학습된 모델로 돌리는 빔 서치와 퀴즈까지

## Transformer

- **[How Attention Works](https://github.com/dev-jonghoonpark/how-attention-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-attention-works/)
  - Attention Is All You Need — seq2seq 병목과 Bahdanau attention부터 Q·K·V, causal mask, 멀티헤드, 위치 인코딩, Pointer Networks까지 12개 데모와 퀴즈로 직접 실험하며 배우는 인터랙티브 교육 자료
