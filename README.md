# how-ai-works

AI가 실제로 어떻게 동작하는지 — 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료 모음입니다.

각 주제는 별도의 레포로 관리되며, 모두 GitHub Pages로 배포되어 있어 설치 없이 바로 실험해 볼 수 있습니다.

> [K-DEVCON AI 스터디](https://k-devcon.com/channel/6/post/563)를 준비하며 만들고 있는 자료들입니다. 계속 추가될 예정입니다.

## 📖 용어 사전

- **[dictionary.md](dictionary.md)**
  - 자료를 읽다 막히는 용어를 정리합니다. — 텐서 · 단방향/양방향 RNN(+ DS2의 행 합성곱이 왜 단방향일 때만 붙는가)

## 기초

- **[How Mean and Variance Works](https://github.com/dev-jonghoonpark/how-mean-and-variance-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mean-and-variance-works/)
  - 평균과 분산에서 정규화 층까지 — LRN과 BatchNorm을 이해하는 데 필요한 것들. 편차 합이 왜 항상 0이고 왜 절댓값이 아니라 제곱인지, Min-Max와 Z-score가 **둘 다 아핀 변환이라 모양은 똑같이 보존된다**는 오해 깨기, 그럼에도 정규화 층이 z-score를 쓰는 진짜 이유(표본을 늘리면 범위는 2.1σ→6.5σ로 발산하지만 σ는 1.00으로 수렴), 칸을 클릭해 확인하는 (N,C,H,W) 축 선택기(BN·LN·IN·GN·LRN이 전부 같은 수식이고 축만 다르다는 것), 한 채널을 키우면 이웃이 눌리는 LRN 측면 억제 계산기, γ·β의 존재 이유, σ/√m을 그대로 재현하는 배치 크기별 통계 흔들림, 그리고 VGG의 재현 실패와 BatchNorm 등장으로 LRN이 사라진 경위까지 직접 실험하는 인터랙티브 교육 자료
- **[How Normal Distribution Works](https://github.com/dev-jonghoonpark/how-normal-distribution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-normal-distribution-works/)
  - 정규분포와 중심극한정리 — AI 학습에서 종 모양이 자꾸 나오는 이유. 골턴 보드 라이브 시뮬레이션, 점 드래그로 눈으로 확인하는 표준편차(편차²=정사각형 넓이), μ·σ 곡선 조작과 68–95–99.7 규칙, 임의 분포에서 표본 평균 10,000개를 뽑는 CLT 실험, 합성곱으로 계산한 주사위 합의 정확한 분포, 뉴런 가중합 z=Σwx의 히스토그램과 1/√d 스케일링(Xavier/He), MSE = 가우시안 가정까지 직접 실험하는 인터랙티브 교육 자료
- **[How Gradient Descent Works](https://github.com/dev-jonghoonpark/how-gradient-descent-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gradient-descent-works/)
  - 경사 하강법은 왜 지그재그로 움직이는가 — 학습률 하나로 갈리는 수렴·진동·발산의 네 가지 운명, GD/Momentum/Adam 비교 실험실, 지그재그의 축별 분해, 조건수 κ와 학습률의 딜레마, 증상별 진단 가이드까지 직접 실험하는 인터랙티브 교육 자료
- **[How SGD Works](https://github.com/dev-jonghoonpark/how-sgd-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-sgd-works/)
  - 확률적 경사 하강법은 어떻게 전부 보지 않고 내려가는가 — **GD와의 차이는 알고리즘이 아니라 기울기를 몇 개로 계산하느냐(B) 하나뿐**이라는 것부터. 미니배치 화살표 100개를 뽑아 평균이 진짜 기울기로 수렴하는 것을 보는 불편 추정량 실험실, GD와 SGD를 같은 지형에서 동시에 달려 B=40에서 두 궤적이 정확히 겹치는 것 확인, 2,000회 추출로 실측해 이론과 3% 이내로 맞추는 **1/√B 법칙**(비복원 보정까지 넣어 B=N에서 오차가 정확히 0), x축을 "스텝"이 아니라 **"계산한 샘플 기울기 수"**로 바꿔 다시 붙는 예산 경주(1에폭 시점 남은 거리가 B=1은 0.023, GD는 6.44), ImageNet 90에폭이 GD에겐 90번·SGD에겐 450,450번의 갱신이 되는 계산기, σ=0이면 탈출률 0%인 지역 최솟값 탈출 측정기, η를 1/4로 줄이면 바닥이 2배 낮아지는 **노이즈 볼**과 Robbins–Monro 조건(Ση=∞, Ση²<∞) — 그리고 체크박스 하나로 **실제 DataLoader의 "에폭마다 셔플"이 교과서의 i.i.d. 추출보다 바닥을 더 낮추는 것**(비율 2 → 3.3)까지 직접 실험하는 인터랙티브 교육 자료
- **[How Backprop Works](https://github.com/dev-jonghoonpark/how-backprop-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-backprop-works/)
  - 순전파·손실 함수·역전파 — 필터의 가중치는 어떻게 올바른 값을 찾아가는가. 손실 지형 드래그, 계산 그래프 위에서 한 단계씩 밟아 보는 연쇄 법칙, 실시간으로 사인 곡선을 배우는 신경망, 그리고 난수로 시작한 3×3 합성곱 필터가 손실과 기울기만 보고 소벨 필터로 수렴하는 과정까지 직접 실험하는 인터랙티브 교육 자료
- **[How Convolution Works](https://github.com/dev-jonghoonpark/how-conv-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-conv-work/)
  - 합성곱(Convolution)은 실제로 무엇을 하는가 — "뒤집고·밀고·곱하고·더하기" 수학적 정의부터 임펄스 응답(LTI), 확률분포의 합, 합성곱 정리(DFT 검증), 2D 이미지 필터, 채널과 1×1 conv(ResNet bottleneck의 채널 변환), CNN의 스트라이드·패딩까지 직접 실험하는 인터랙티브 교육 자료
- **[How Fourier Transform Works](https://github.com/dev-jonghoonpark/how-fourier-transform-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-fourier-transform-works/)
  - 푸리에 변환(FT)·DFT·FFT — **FFT는 다른 변환이 아니라 DFT를 N log N에 계산하는 알고리즘**이라는 것부터. 복소평면에서 도는 점의 실수부가 사인파가 되는 회전 데모, 사인파 N개로 사각파·삼각파를 쌓으며 보는 1/n vs 1/n² 수렴과 N=60에서도 남는 약 9%의 깁스 현상, 위상이 90° 어긋나면 cos 탐침만으로는 성분이 0으로 보여 e<sup>−i2πft</sup>가 필요해지는 "곱해서 평균 내기", 신호를 원점 둘레에 감아 무게중심을 재는 감기 기계, 수치 적분으로 확인하는 시간 폭×주파수 폭 = 상수(사각 1.207 · 가우시안 0.883), 12 Hz가 8 Hz로 접히는 에일리어싱, 회전 벡터 8개의 합으로 그리는 **8칸 DFT 계산기**, 짝/홀로 쪼개 X[k] = E[k] ± ω<sup>k</sup>·O[k]로 합치는 **FFT 재귀 실행기**(곱셈 64 → 12)와 순진한 DFT 대비 실측 속도, 누설·Hann 창·제로패딩(패딩으로는 못 가르고 N을 늘려야 갈라지는 두 톤), 평균·고역 커널의 주파수 응답으로 확인하는 합성곱 정리 Y = X·H까지 직접 실험하는 인터랙티브 교육 자료

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
- **[How Bidirectional RNN Works](https://github.com/dev-jonghoonpark/how-bidirectional-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-bidirectional-rnn-works/)
  - 양방향 RNN은 어떻게 동작하는가 — **미래를 보는 대가**. `bidirectional=True` 한 글자가 정확도를 올리는 대신 모델을 실시간에서 추방하는 과정을 축으로, 프레임이 한 칸씩 도착하는 동안 세 구조가 언제 출력할 수 있는지 보는 시간 전개 재생기(양방향은 입력이 끝난 뒤에야 역방향이 오른쪽에서 왼쪽으로 쓸고 내려오고, 출력도 거꾸로 확정돼 **첫 글자가 맨 마지막**에 나온다), 단방향=하삼각·양방향=꽉 참·행 합성곱=하삼각+폭 τ의 띠를 칸 클릭으로 확인하는 의존성 행렬, `/t/`와 `/d/`를 가르는 증거가 자음이 아니라 **다음 모음의 VOT**에 있어 **lookahead 3프레임에서 판정이 뒤집히는** 실험(그리고 τ를 늘리는 것이 늘 이득은 아닌 비단조성), 양방향이 정확히 2배가 아님을 보이는 파라미터 계산기(concat 2.87배 ↔ DS2 식 (6)의 sum·W 공유 1.54배), 역방향 상태에 정답이 들어 있어 언어 모델이 성립하지 않는 **라벨 누수**(BERT의 MLM과 causal mask가 같은 문제의 답), **단방향으로 되돌릴 때만 붙는 층인 행 합성곱**의 상수 지연 예산(τ=19 · 40 ms = 760 ms · 파라미터 51,200개, 채널을 섞었다면 ×2,560), `pack_padded_sequence`를 끄면 역방향이 PAD부터 읽는 패딩 오염 시뮬레이터까지 직접 실험하는 인터랙티브 교육 자료
- **[LSTM Text Generation](https://github.com/dev-jonghoonpark/lstm-text-generation)** · 💻 내 컴퓨터에서 실행
  - 앞의 브라우저 자료들로 원리를 봤다면, 이번엔 직접 학습시켜 보는 쪽 — 정글북 원문으로 문자 단위 LSTM을 돌려 다음 한 글자를 예측하게 만드는 Keras 실습. 학습 데이터 (앞 60자 → 다음 1자) 쌍이 사람 손 없이 27,297개 만들어지는 과정, 2 epoch(`trann`·`brtong`)에서 50 epoch(`the monkeys`·`man-cun`)로 가며 실제로 달라지는 생성 결과, loss 0.5949에서 곡선이 평평해지는 것을 보고 "epoch를 더 늘릴지 `step`을 낮출지" 판단하는 법까지. 원-핫을 밀집 배열로 펼치면 왜 800MB가 되는지, `temperature`가 분포에 무엇을 하는지도 코드에서 짚는다. Python for Microscopists 167번 영상의 예제를 최신 라이브러리에서 돌아가게 고치고(`np.bool` 제거, `.keras` 저장, 동작하지 않던 `temperature` 복원 등 9곳) 한국어 해설을 붙였다

## 음성 인식 (Deep Speech 2)

- **[How Deep Speech 2 Works](https://github.com/dev-jonghoonpark/how-deep-speech-2-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-deep-speech-2-works/)
  - Deep Speech 2는 실제로 어떻게 동작하는가 (Amodei et al., 2015) — 논문 28쪽을 앞에서부터 따라가며 표와 수식이 나올 때마다 그 값을 브라우저에서 직접 계산해 보는 자료. 7초 발화가 순환층 안에서 스텝 350개가 되는 과정을 8단계로 추적하는 **모양 추적기**(스트라이드를 4로 올리면 영어 유니그램의 "토큰당 스텝"이 3.54 → 1.77로 떨어지고 바이그램이 2.82로 되살리는 것, 중국어는 7.61로 여유가 넘치는 것), **브라우저가 FFT를 직접 돌려 만드는 스펙트로그램**과 창 길이의 시간·주파수 해상도 맞교환, 식 (9)의 모든 정렬을 더하는 **CTC 전진 변수 α를 칸칸이 채우는 실행기**(전수 열거와 대조 검증: `cat`/T=7 → 정렬 210개 · `aa`는 blank 때문에 최소 3프레임), 식 7과 식 8이 통계를 재는 범위가 갈리는 이유와 BatchNorm이 **가장 얕은 모델에서는 오히려 해로웠던** 표 1, 첫 에포크 미니배치 구성기로 보는 SortaGrad, `h(t−1)`에 걸리는 **GEMM 3개가 1개로 합쳐지는** GRU 변형과 1억 파라미터에서 바닐라 RNN에 뒤집히는 표 11, 목소리 높이를 비율로 바꿔 보며 **2D 합성곱은 불변이 아니라 국소적으로 강건할 뿐**임을 재는 실험(3% 변화에 위치 그대로는 0.35, 주파수 ±3칸 여유를 주면 0.93), `the cat sat` → `[th, e, ␣, ca, t, ␣, sa, t]` 바이그램 분해기와 표 5, 표 10에 거듭제곱 법칙을 맞춰 목표 WER에 필요한 시간을 역산하기(논문의 "10배당 40%"가 실제로는 구간별 52.8%/38.7%인 것), 논문의 280 MB vs 1.5 GB를 재구성하는 12 GB 메모리 계산기, 11개 테스트셋에서 사람과의 승부, **Batch Dispatch 이산 사건 시뮬레이터**(eager batching이 10 스트림에서 중앙값 45ms를 내고, 배치를 채우려 기다리면 81ms로 나빠지는 것)까지 직접 실험하는 인터랙티브 교육 자료

- **[How Row Convolution Works](https://github.com/dev-jonghoonpark/how-row-convolution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-row-convolution-works/)
  - 행 합성곱(row convolution)은 어떻게 미래를 엿보는가 (Amodei et al., 2015 · 3.7절) — 양방향 RNN이 "말이 끝나야" 시작하는 문제를 세 구조 실시간 재생으로 비교, `/t/` vs `/d/`의 판별 증거가 늦게 도착해 lookahead를 늘려야 예측이 뒤집히는 과정, 식 (11)을 칸 클릭으로 직접 전개하며 확인하는 채널 비혼합(= depthwise 1D conv), τ·스텝 상수 지연 예산(논문 τ=19 · 40ms → 760ms), 채널을 섞었다면 파라미터가 정확히 d배(2,560배) 늘어 순환 스택 전체보다 커지는 계산, lookahead를 여러 층에 나누면 지연이 누적되는 이유, 근사가 양방향보다 CER이 낮았던 배포 결과까지 직접 실험하는 인터랙티브 교육 자료
- **[How CTC Beam Search Works](https://github.com/dev-jonghoonpark/how-ctc-beam-search-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ctc-beam-search-works/)
  - 빔 서치는 무엇을 찾고 있는가 — DS2의 디코딩(3.8절·7.3절) — CTC 축약 2단계와 blank가 글자 경계를 만드는 이유, 4,096개 정렬 전수 열거로 드러나는 greedy의 실패(`"ct"` 0.204 vs `"cat"` 0.425), 접두사마다 `p_b`/`p_nb`를 따로 드는 이유와 **프레임 단위 prefix beam search 스텝 실행기**, 빔 폭 1→50의 포화(폭 2부터 정답·20에서 전수 열거와 100% 일치), `Q(y) = log p_ctc + α log p_lm + β·단어수`의 세 항을 α·β 슬라이더로 뒤집어 보는 재순위와 β가 없으면 단어를 빠뜨리는 이유, 배포 가지치기가 논문의 120만 회 → 8,000회 = 150배를 그대로 재현하는 계산기까지 직접 실험하는 인터랙티브 교육 자료
- **[DS2 My Voice](https://github.com/dev-jonghoonpark/ds2-my-voice)** · [🔗 데모](https://dev-jonghoonpark.github.io/ds2-my-voice/) · 💻 내 컴퓨터에서 학습
  - 앞의 자료들로 부품을 봤다면, 이번엔 DS2를 통째로 조립해 실제로 학습시켜 보는 쪽 — PyTorch로 직접 구현한 축소판 DeepSpeech2(Conv2d 2층 + 양방향 GRU 5층 + CTC, 18.5M)를 Zeroth-Korean 51.7시간으로 RTX 3070 한 장에서 1시간 40분 사전학습(CER 0.776 → 0.171)하고, 화면에 뜬 문장을 읽어 녹음한 **내 목소리 7분**으로 파인튜닝한다. 음절 11,172개 대신 초성·중성·종성 67개로 쪼개는 자모 토크나이저, 짧은 발화부터 학습하는 SortaGrad, 처음 몇 epoch 동안 blank만 내보내는 CTC의 초기 현상까지 코드에서 짚는다. 결과는 학습에 쓰지 않은 내 목소리 19문장에서 CER 0.261 → 0.165(**화자 적응**), 대신 다른 화자 457문장은 0.171 → 0.237로 나빠지는 **망각**. 데모 페이지에서 같은 녹음을 두 모델이 어떻게 받아썼는지 틀린 글자 표시와 함께 들으며 비교할 수 있다

## seq2seq

- **[How seq2seq Works](https://github.com/dev-jonghoonpark/how-seq2seq-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-seq2seq-works/)
  - seq2seq(2014)의 동작 원리 — 인코더·디코더 애니메이션, 고정 길이 병목, 입력 역순 트릭, 브라우저에서 직접 학습하는 미니 LSTM seq2seq(순방향 vs 역순 A/B 실험), 학습된 모델로 돌리는 빔 서치와 퀴즈까지

## Transformer

- **[How Attention Works](https://github.com/dev-jonghoonpark/how-attention-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-attention-works/)
  - Attention Is All You Need — seq2seq 병목과 Bahdanau attention부터 Q·K·V, causal mask, 멀티헤드, 위치 인코딩, Pointer Networks까지 12개 데모와 퀴즈로 직접 실험하며 배우는 인터랙티브 교육 자료

## 강화학습과 탐색 (AlphaGo)

- **[How AlphaGo Works](https://github.com/dev-jonghoonpark/how-alphago-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alphago-works/)
  - AlphaGo는 어떻게 동작하는가 (Silver et al., Nature 2016) — **분류용으로만 알던 CNN이 머리 하나만 바꿔 형세 판단기가 되는 과정**을 축으로 논문 전체를 따라가는 자료. 체스와 바둑의 b<sup>d</sup>를 비교하고 정책망은 너비를, 가치망은 깊이를 줄인다는 것을 보는 탐색 공간 계산기, 9×9 판에 돌을 놓으면 48장의 특징 평면(활로·따내기·자충·합리성)이 0/1 격자로 칠해지는 채널 뷰어와 8가지 대칭, 13층 CNN의 수용 영역(구석은 27×27로도 판 전체를 못 본다 → 축 평면을 손으로 넣은 이유), 브라우저가 실제로 끝까지 두는 롤아웃과 1/√n 신뢰구간, 128판씩 두며 기대 승률은 오르고 엔트로피는 0으로 떨어지는 REINFORCE 실험실, 같은 몸통(약 388만 파라미터)에 정책 머리 553개 ↔ 가치 머리 93,122개를 갈아 끼우는 **머리 바꾸기**, **±1 라벨만으로 MSE 최소점이 진짜 승률에 수렴하는 이유**("라벨은 미래에서 온다"), 한 판에서 뽑는 국면 수만 바꿔 train 0.02 / test 1.40으로 벌어지는 **기보 암기 재현 실험**(논문의 0.19 / 0.37 → 판당 1국면으로 해결), 정책망 1순위가 틀린 트리를 탐색이 뒤집는 **MCTS 선택·확장·평가·백업 단계 실행기**, 가치망과 롤아웃을 섞는 λ 스윕, 1순위가 같아도 뾰족한 RL 사전확률은 탐색이 되돌아오지 못하는 비교, 스레드가 한 후보로 몰리지 않게 하는 가상 손실, Elo → 승률 계산기(230점 = 79%)까지 직접 실험하는 인터랙티브 교육 자료
