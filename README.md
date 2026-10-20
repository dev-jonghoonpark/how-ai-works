# how-ai-works

AI가 실제로 어떻게 동작하는지 — 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료 모음입니다.

각 주제는 별도의 레포로 관리되며, 모두 GitHub Pages로 배포되어 있어 설치 없이 바로 실험해 볼 수 있습니다.

> [K-DEVCON AI 스터디](https://k-devcon.com/channel/6/post/563)를 준비하며 만들고 있는 자료들입니다. 계속 추가될 예정입니다.

## 📖 용어 사전

- **[dictionary.md](dictionary.md)**
  - 자료를 읽다 막히는 용어 정리 — 텐서 · 단방향/양방향 RNN(+ DS2의 행 합성곱) · GRU(+ LSTM과 비교해 잃는 것) · Post-LN/Pre-LN(+ 워밍업이 왜 필요했는가)

## 기초

- **[How Mean and Variance Works](https://github.com/dev-jonghoonpark/how-mean-and-variance-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mean-and-variance-works/)
  - 평균과 분산에서 정규화 층까지 — 편차를 왜 제곱하는지, 정규화 층이 z-score를 쓰는 이유, BN·LN·IN·GN·LRN이 **같은 수식에 축만 다르다**는 것을 칸 클릭 축 선택기로 확인하고, LRN이 BatchNorm에 밀려 사라진 경위까지
- **[How Normal Distribution Works](https://github.com/dev-jonghoonpark/how-normal-distribution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-normal-distribution-works/)
  - 정규분포와 중심극한정리 — AI 학습에서 종 모양이 자꾸 나오는 이유. 골턴 보드, 표본 평균으로 보는 CLT, 가중합의 1/√d 스케일링(Xavier/He), MSE = 가우시안 가정
- **[How Gradient Descent Works](https://github.com/dev-jonghoonpark/how-gradient-descent-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gradient-descent-works/)
  - 경사 하강법은 왜 지그재그로 움직이는가 — 학습률에 따라 갈리는 수렴·진동·발산, GD/Momentum/Adam 비교, 조건수 κ와 학습률의 딜레마, 증상별 진단 가이드
- **[How SGD Works](https://github.com/dev-jonghoonpark/how-sgd-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-sgd-works/)
  - 확률적 경사 하강법 — **GD와의 차이는 기울기를 몇 개로 계산하느냐(B) 하나뿐**. 미니배치 기울기의 불편성, 1/√B 법칙, 같은 계산량으로 다시 붙는 GD vs SGD 경주, 노이즈로 지역 최솟값 탈출하기, 에폭마다 셔플이 i.i.d. 추출보다 나은 이유
- **[How Adam Works](https://github.com/dev-jonghoonpark/how-adam-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-adam-works/)
  - Adam 옵티마이저 (Kingma & Ba, ICLR 2015) — **파라미터마다 따로 재는 보폭**. 이동 평균과 편향 보정, 손실 스케일과 무관한 스텝 크기, Adam이 늘 제일 빠르지는 않은 경우, Adam vs AdamW의 weight decay, AMSGrad를 낳은 Reddi 반례, 학습 메모리의 절반이 m·v인 이유
- **[How Backprop Works](https://github.com/dev-jonghoonpark/how-backprop-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-backprop-works/)
  - 순전파·손실 함수·역전파 — 가중치는 어떻게 올바른 값을 찾아가는가. 계산 그래프 위의 연쇄 법칙, 사인 곡선을 배우는 신경망, 난수에서 시작한 3×3 필터가 소벨 필터로 수렴하는 과정
- **[How Convolution Works](https://github.com/dev-jonghoonpark/how-conv-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-conv-work/)
  - 합성곱은 실제로 무엇을 하는가 — "뒤집고·밀고·곱하고·더하기" 정의에서 임펄스 응답, 합성곱 정리, 2D 이미지 필터, 채널과 1×1 conv, CNN의 스트라이드·패딩까지
- **[How Fourier Transform Works](https://github.com/dev-jonghoonpark/how-fourier-transform-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-fourier-transform-works/)
  - 푸리에 변환·DFT·FFT — **FFT는 다른 변환이 아니라 DFT를 N log N에 계산하는 알고리즘**. 회전하는 점으로 보는 사인파, 깁스 현상, 에일리어싱, 8칸 DFT 계산기와 FFT 재귀 실행기, 창 함수와 제로패딩, 합성곱 정리

## AlexNet

- **[How AlexNet Works](https://github.com/dev-jonghoonpark/how-alexnet-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alexnet-works/)
  - AlexNet은 실제로 어떻게 동작하는가 — 논문의 실제 conv1 커널과 ILSVRC 이미지로 브라우저에서 직접 계산해 보기

## ResNet

- **[How ResNet Works](https://github.com/dev-jonghoonpark/how-resnet-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-resnet-work/)
  - ResNet의 동작 원리를 브라우저에서 직접 실험하며 배우기
- **[ResNet Bottleneck](https://github.com/dev-jonghoonpark/resnet-bottleneck)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-bottleneck/)
  - Bottleneck Block에서 1×1 conv가 하는 일
- **[ResNet의 BatchNorm](https://github.com/dev-jonghoonpark/resnet-batchnorm)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-batchnorm/)
  - 깊은 네트워크는 왜 배치 정규화가 필요한가 — BN 수식과 γ·β, 역전파 흐름, ResNet 블록 안의 위치, BN·skip을 켜고 끄는 30층 신호 전파 시뮬레이션, 학습/추론 모드와 BN folding
- **[ResNet DJL Lab](https://github.com/dev-jonghoonpark/resnet-djl-lab)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-djl-lab/)
  - v1과 v2의 차이는 새 연산이 아니라 **BN·ReLU·덧셈의 순서** 하나 — DJL(Deep Java Library)로 두 버전을 구현해 파라미터 수를 torchvision·논문 값과 대조하고, 고양이 사진 한 장이 순전파 → 역전파 → 가중치 갱신을 한 바퀴 도는 80단계의 실제 값을 Java로 다시 계산해 엔진 값과 나란히 싣는다
- **[How Dilated Convolution Works](https://github.com/dev-jonghoonpark/how-dilated-conv-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-dilated-conv-works/)
  - Dilated Convolution은 어떻게 풀링 없이 시야를 넓히는가 (Yu & Koltun, ICLR 2016) — 수용 영역의 지수적 확장(Figure 1 재현), 컨텍스트 모듈, 항등 초기화, gridding effect

## N-gram

- **[How N-gram Works](https://github.com/dev-jonghoonpark/how-n-gram-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-n-gram-work/)
  - 세는 것만으로 언어를 예측하는 n-gram 언어 모델 — 편집 가능한 코퍼스로 카운트 행렬, 텍스트 생성, 희소성, 스무딩, 퍼플렉시티

## 단어 임베딩

- **[How word2vec Works](https://github.com/dev-jonghoonpark/how-word2vec-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-word2vec-works/)
  - word2vec은 어떻게 "king − man + woman ≈ queen"을 만드는가 — CBOW와 Skip-gram, 계층적 소프트맥스와 네거티브 샘플링, 서브샘플링, **브라우저에서 실제로 도는 SGNS 학습기**와 방금 학습한 벡터로 돌리는 유추 계산기

## RNN

- **[How RNN Works](https://github.com/dev-jonghoonpark/how-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-works/)
  - RNN 부흥기(2014–2016)를 따라가는 인터랙티브 노트 — 브라우저에서 학습하는 min-char-rnn, LSTM 게이트 조작기, 선택적 드롭아웃, Deep Speech 2 빔서치 시뮬레이터, 퀴즈
- **[How char-rnn Works](https://github.com/dev-jonghoonpark/how-char-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-char-rnn-works/)
  - Karpathy 「The Unreasonable Effectiveness of Recurrent Neural Networks」(2015) 한국어 인터랙티브 해설 — step() 한 줄 손으로 따라가기, 온도 슬라이더, 브라우저에서 학습하는 이름 생성기와 셰익스피어 LSTM, 해석 가능한 셀 탐색기
- **[How LSTM Works](https://github.com/dev-jonghoonpark/how-lstm-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-lstm-works/)
  - LSTM은 어떻게 기억하는가 — 기울기 소멸과 셀 상태 레일, 게이트 조작기, 손으로 심은 가중치로 괄호 깊이를 세는 LSTM, 핍홀·결합 게이트·GRU 변형과 파라미터 비교
- **[How GRU Works](https://github.com/dev-jonghoonpark/how-gru-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gru-works/)
  - GRU (Cho et al., EMNLP 2014) — **LSTM에서 게이트 하나를 덜어 낸 값**. 세 번의 수술로 LSTM에서 GRU에 도착하는 과정(가중치가 정확히 3/4), 상태가 볼록 결합이라 (−1, 1)에 갇혀 **세지 못하는** 대가, 브라우저에서 학습시키는 RNN·GRU·LSTM 비교, 프레임워크별 구현 차이
- **[How RNN Dropout Works](https://github.com/dev-jonghoonpark/how-rnn-dropout-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-dropout-works/)
  - 드롭아웃은 왜 순환 연결을 피해 가는가 (Zaremba, Sutskever & Vinyals, 2014) — 정보가 손상되는 횟수(**L+1** vs **L+1+Δt**)를 세어 보는 Figure 2·3 재현, 경로 생존 시뮬레이션, PTB 퍼플렉시티 114.5 → 78.4, Gal & Ghahramani·Zoneout 비교
- **[How Bidirectional RNN Works](https://github.com/dev-jonghoonpark/how-bidirectional-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-bidirectional-rnn-works/)
  - 양방향 RNN — **미래를 보는 대가**. 정확도는 오르지만 실시간에서 쓸 수 없게 되는 이유를 시간 전개 재생기와 의존성 행렬로 확인하고, `/t/`·`/d/`를 가르는 증거가 다음 모음에 있는 실험, 언어 모델의 라벨 누수, 단방향으로 되돌릴 때 붙이는 행 합성곱까지
- **[LSTM Text Generation](https://github.com/dev-jonghoonpark/lstm-text-generation)** · 💻 내 컴퓨터에서 실행
  - 원리를 봤다면 직접 학습시켜 보는 쪽 — 정글북 원문으로 문자 단위 LSTM을 학습하는 Keras 실습. epoch에 따라 달라지는 생성 결과와 `temperature`의 역할을 코드에서 짚는다. Python for Microscopists 167번 예제를 최신 라이브러리에서 돌아가게 고쳤다

## 음성 인식 (Deep Speech 2)

- **[How Deep Speech 2 Works](https://github.com/dev-jonghoonpark/how-deep-speech-2-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-deep-speech-2-works/)
  - Deep Speech 2 (Amodei et al., 2015) — 논문을 앞에서부터 따라가며 표와 수식의 값을 브라우저에서 직접 계산한다. 7초 발화가 스텝 350개가 되는 모양 추적기, FFT 스펙트로그램, CTC 전진 변수 실행기, BatchNorm·SortaGrad·GRU 변형, 스케일링 법칙 역산, 메모리 계산기, Batch Dispatch 시뮬레이터
- **[How Row Convolution Works](https://github.com/dev-jonghoonpark/how-row-convolution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-row-convolution-works/)
  - 행 합성곱은 어떻게 미래를 엿보는가 (DS2 3.7절) — 양방향·단방향·단방향+행 합성곱 세 구조의 실시간 비교, 식 (11)을 칸 클릭으로 전개해 보는 채널 비혼합(= depthwise 1D conv), τ=19 · 760 ms 상수 지연, 근사가 양방향보다 CER이 낮았던 배포 결과
- **[How CTC Beam Search Works](https://github.com/dev-jonghoonpark/how-ctc-beam-search-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ctc-beam-search-works/)
  - 빔 서치는 무엇을 찾고 있는가 (DS2 3.8절·7.3절) — blank와 CTC 축약, 전수 열거로 드러나는 greedy의 실패, 프레임 단위 prefix beam search 실행기, 빔 폭에 따른 포화, α·β로 보는 언어 모델 재순위
- **[DS2 My Voice](https://github.com/dev-jonghoonpark/ds2-my-voice)** · [🔗 데모](https://dev-jonghoonpark.github.io/ds2-my-voice/) · 💻 내 컴퓨터에서 학습
  - 부품을 봤다면 DS2를 통째로 조립해 학습시켜 보는 쪽 — PyTorch로 구현한 축소판 DS2(18.5M)를 Zeroth-Korean으로 사전학습하고 **내 목소리 7분**으로 파인튜닝한다. 내 목소리 CER은 0.261 → 0.165로 좋아지지만(화자 적응) 다른 화자는 0.171 → 0.237로 나빠지는(망각) 결과를 데모에서 들으며 비교

## seq2seq

- **[How seq2seq Works](https://github.com/dev-jonghoonpark/how-seq2seq-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-seq2seq-works/)
  - seq2seq(2014)의 동작 원리 — 인코더·디코더 애니메이션, 고정 길이 병목, 입력 역순 트릭, 브라우저에서 학습하는 미니 LSTM seq2seq, 빔 서치와 퀴즈
- **[How Pointer Network Works](https://github.com/dev-jonghoonpark/how-pointer-network-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-pointer-network-works/)
  - Pointer Networks (Vinyals, Fortunato & Jaitly, NeurIPS 2015) — **어텐션 분포를 섞지 않고 그대로 출력으로 쓰기**. 출력 사전이 고정된 seq2seq의 한계, 점을 찍어 보는 볼록 껍질·TSP, 브라우저에서 학습하는 미니 Ptr-Net, 길이 일반화, pointer-generator의 OOV 복사
- **[How Order Matters Works](https://github.com/dev-jonghoonpark/how-order-matters-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-order-matters-works/)
  - Order Matters (Vinyals, Bengio & Kudlur, ICLR 2016) — **체인 룰은 어떤 순서로 풀어도 같은 확률인데, 왜 순서를 바꾸면 성능이 달라지는가**. 입력 순서 실험, 집합을 순서 없이 읽는 Read-Process-Write, 출력 순서 실험과 조건부 엔트로피, 순서를 모델이 고르게 하는 식 (9)

## 메모리 증강 신경망

- **[How Neural Turing Machines Work](https://github.com/dev-jonghoonpark/how-ntm-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ntm-works/)
  - Neural Turing Machine (Graves, Wayne & Danihelka, 2014) — 기억을 **망 밖의 N × M 행렬**로 꺼내고, 주소를 **모든 칸에 나눈 가중치**로 정해 경사 하강으로 학습할 수 있게 만든 방법. 흐릿한 읽기·쓰기, 내용 → 보간 → 이동 → 샤프닝 주소 파이프라인, 손으로 배선한 NTM의 복사 과제, 내용 주소 = 어텐션이라는 연결

## Transformer

- **[How Attention Works](https://github.com/dev-jonghoonpark/how-attention-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-attention-works/)
  - Attention Is All You Need — seq2seq 병목과 Bahdanau attention부터 Q·K·V, causal mask, 멀티헤드, 위치 인코딩, Pointer Networks까지 12개 데모와 퀴즈
- **[그림으로 보는 Transformer](https://github.com/dev-jonghoonpark/illustrated-transformer-ko)** · [🔗 데모](https://dev-jonghoonpark.github.io/illustrated-transformer-ko/)
  - Jay Alammar의 [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) 순서를 따라 새로 쓴 한국어 해설(원문 번역은 [nlpinkorean](https://nlpinkorean.github.io/illustrated-transformer/)) — **그림 속 숫자를 직접 계산해 보는** 쪽. 셀프 어텐션이 순서를 모른다는 실험, q·k·v 손계산기, √d<sub>k</sub> 스케일링, 멀티헤드, 위치 인코딩, 한 단계씩 생성하는 디코더와 빔 서치
- **[How Transformer Works](https://github.com/dev-jonghoonpark/how-transformer-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-transformer-works/)
  - Transformer (Vaswani et al., NeurIPS 2017) — 앞 자료가 어텐션의 **내부**였다면 이쪽은 **블록과 모델 전체**. 블록의 무게는 FFN에 있고 학습 성패를 가른 건 **잔차와 LayerNorm의 순서**라는 것을 축으로 — 셀프 어텐션 vs 순환 비용, shape 추적기, 위치 인코딩 스케일, Post-LN/Pre-LN 신호 전파, 파라미터 계산기, Noam 스케줄, 레이블 스무딩, KV 캐시
- **[How Positional Encoding Works](https://github.com/dev-jonghoonpark/how-positional-encoding-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-positional-encoding-works/)
  - 위치 인코딩은 왜 sin과 cos를 **함께** 쓰는가 — (sin, cos) 쌍은 도는 시계 바늘이라 "k칸 뒤"가 위치와 무관한 회전 행렬이 된다는 것, sin만으로는 안 되는 이유, 내적이 거리에만 의존하는 성질, 그리고 RoPE까지
- **[How BERT Works](https://github.com/dev-jonghoonpark/how-bert-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-bert-works/)
  - BERT (Devlin et al., NAACL 2019) — GPT와의 구조 차이는 **어텐션 마스크 한 장**, 진짜 기여는 **학습 과제**라는 것을 축으로. ELMo와의 양방향 비교, 마스크를 걷어내면 생기는 누수 경로, WordPiece 입력 조립기, 80/10/10 마스킹, NSP, 파라미터·학습 예산 계산기, SQuAD 구간 점수기
- **[How GPT Works](https://github.com/dev-jonghoonpark/how-gpt-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gpt-works/)
  - GPT는 어떻게 다음 단어를 고르는가 — 3Blue1Brown 딥러닝 5~7장([DL5](https://www.youtube.com/watch?v=g38aoGttLhI) · [DL6](https://www.youtube.com/watch?v=_Z3rXeJahMs) · [DL7](https://www.youtube.com/watch?v=zHQLPJ8-9Qc))을 따라 입력부터 출력까지. 온도와 샘플링, 임베딩 벡터 연산, 어텐션 헤드, 뉴런 네 개짜리 MLP, 고차원 벡터의 거의-직교성, GPT-3 파라미터 계산기
- **[How Universal Transformer Works](https://github.com/dev-jonghoonpark/how-universal-transformer-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-universal-transformer-works/)
  - Universal Transformer (Dehghani et al., ICLR 2019) — **층을 쌓지 말고, 같은 층을 T번**. 같은 층을 반복하면 깊이 방향 RNN이 되어 **파라미터와 연산이 분리된다**는 것을 축으로 — 파라미터·연산 계산기, (위치, 단계) 좌표 임베딩, 고정 깊이의 한계를 보는 누적 패리티, ACT 실행기, 결과 탐색기
- **[Annotated Transformer Modern](https://github.com/dev-jonghoonpark/annotated-transformer-modern)** · 💻 내 컴퓨터에서 학습
  - 코드를 직접 돌려 보는 쪽 — [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/)(Rush 2018, Huang 외 2022 개정)를 최신 라이브러리에서 돌아가게 고쳤다. 개발이 중단된 torchtext를 대체하는 등 **4곳만** 고치고 본문과 코드는 원본 그대로 두었으며, 노트북 전체를 실행한 출력까지 담았다
- **[Annotated Transformer Step by Step](https://github.com/dev-jonghoonpark/annotated-transformer-step-by-step)** · [🔗 데모](https://dev-jonghoonpark.github.io/annotated-transformer-step-by-step/)
  - 위 노트북을 어디서부터 읽을지 막막할 때 — 어텐션 함수 11줄짜리 빈 파일에서 시작해 부품을 하나씩 더하며 **18단계 만에 원본 코드(1,031줄)를 완성**한다. 단계마다 diff·설명·실행 결과를 나란히 보여 준다(←/→)

## 강화학습과 탐색 (AlphaGo)

- **[How AlphaGo Works](https://github.com/dev-jonghoonpark/how-alphago-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alphago-works/)
  - AlphaGo (Silver et al., Nature 2016) — **분류용 CNN이 머리 하나만 바꿔 형세 판단기가 되는 과정**을 축으로. 탐색 공간 계산기, 48장 특징 평면 뷰어, 롤아웃과 REINFORCE, 정책 머리 ↔ 가치 머리 바꾸기, 기보 암기 재현 실험, MCTS 단계 실행기, Elo → 승률 계산기

## 스케일링과 병렬화

- **[How Scaling Laws Work](https://github.com/dev-jonghoonpark/how-scaling-laws-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-scaling-laws-work/)
  - Scaling Laws for Neural Language Models (Kaplan et al., arXiv 2020) — **loss는 규모(N·D·C)의 멱법칙이라 학습하기 전에 계산할 수 있다**. 로그-로그 직선, L(N)·L(D)·L(C) 계산기, 작은 실험으로 175B loss 외삽하기, L(N,D) 과적합 경계, 6ND 연산 계산기, 연산 최적 배분, Chinchilla IsoFLOP 단면으로 보는 배분의 반전, 멱법칙이 깨지는 교차점
- **[How GPipe Works](https://github.com/dev-jonghoonpark/how-gpipe-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gpipe-works/)
  - GPipe (Huang et al., NeurIPS 2019) — **모델은 층으로 자르고, 배치는 마이크로배치로 쪼개고, 갱신은 한 번에 — 그래서 장치를 몇 대로 나누든 학습되는 수학은 같다**. 표 1 메모리 계산기, K·M 파이프라인 타임라인 재생기, 버블 (K−1)/(M+K−1)과 표 2 비교, 셀 분할 DP, 재계산 활성 메모리 추적기, 동기식 누적 vs 지연된 기울기 학습 비교, GPipe vs 1F1B

## 표현과 관계 추론

- **[How VLAE Works](https://github.com/dev-jonghoonpark/how-vlae-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-vlae-works/)
  - Variational Lossy Autoencoder (Chen et al., ICLR 2017) — **잠재 코드에는 디코더가 혼자 모델링할 수 없는 정보만 담긴다**. ELBO 계산기, Bits-Back 코드 장부, posterior collapse 재현, 디코더 창 크기만 바꾼 장난감 VLAE 7개(z 13.0 → 5.6비트, 브라우저 재학습), 압축 해제 뷰어, AF 사전분포 = IAF 사후분포, 비율–왜곡 평면
- **[How Relation Network Works](https://github.com/dev-jonghoonpark/how-relation-network-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-relation-network-works/)
  - A Simple Neural Network Module for Relational Reasoning (Santoro et al., NeurIPS 2017) — **모든 객체 쌍에 같은 함수 g를 적용하고 더한다**. n² 쌍 열거, 합으로 얻는 순서 불변성, 좌표 없는 CNN 칸은 섞어도 구분 못 하는 것, 브라우저에서 학습하는 Sort-of-CLEVR RN vs MLP, CLEVR 95.5% vs 사람 92.6%, 보이지 않는 용수철 찾기, n² 계산량과 셀프 어텐션
- **[How Relational RNN Works](https://github.com/dev-jonghoonpark/how-relational-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-relational-rnn-works/)
  - Relational Recurrent Neural Networks (Santoro et al., NeurIPS 2018) — **메모리 갱신을 [M; x] 위의 셀프 어텐션으로 바꿔, 같은 어텐션 한 번이 입력 받아들이기와 기억끼리의 비교를 함께 한다**. N번째로 먼 점, 슬롯·헤드 슬라이더와 어텐션 히트맵, 슬롯 수와 무관한 파라미터 계산기, 내적으로 거리를 계산하는 어텐션, Learning to Execute 생성기, BoxWorld, 퍼플렉시티 비교(슬롯 1개였다는 단서까지)

## 복잡도와 압축

- **[How Complexodynamics Works](https://github.com/dev-jonghoonpark/how-complexodynamics-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-complexodynamics-works/)
  - The First Law of Complexodynamics (Aaronson, 2011 · Aaronson, Carroll & Ouellette, 2014) — **엔트로피는 상태를 통째로 적는 비용이고, 흥미로운 복잡도는 흐리게 본 뒤에도 남는 것을 적는 비용**. 섀넌 엔트로피와 압축, LZ77로 보는 콜모고로프 복잡도와 무작위의 함정, 두 부분 설명과 정교함, 복잡외연(complextropy), 브라우저에서 돌리는 커피 오토마톤과 엔트로피·복잡도 곡선(그림 2·10 재현), MDL로 보는 압축과 학습
- **[How MDL Works](https://github.com/dev-jonghoonpark/how-mdl-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mdl-works/)
  - Keeping Neural Networks Simple by Minimizing the Description Length of the Weights (Hinton & van Camp, COLT 1993) — **일반화는 압축이다: 가중치에 담긴 정보가 훈련 출력에 담긴 정보보다 훨씬 적어야 한다**. 가중치·미스핏 비트, 가중치별 최적 정밀도, 노이즈 가중치의 KL, bits-back 시뮬레이터, 혼합 사전분포, 브라우저에서 학습하는 벌점 없음·가중치 감쇠·MDL 비교, ELBO·Bayes by Backprop으로의 연결

## 지능의 정의와 안전

- **[How Universal Intelligence Works](https://github.com/dev-jonghoonpark/how-universal-intelligence-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-universal-intelligence-works/)
  - Machine Super Intelligence (Legg, PhD thesis 2008) · Universal Intelligence (Legg & Hutter, 2007) — **보편 지능은 단순한 환경일수록 크게 쳐 준 성적의 가중합**. 지능 정의 71개 탐색기, 솔로모노프 혼합 예측, 장난감 환경 15개 × 에이전트 7개로 계산하는 Υ(π), 가설 8개짜리 작은 AIXI, 예측기를 이기는 적대적 수열, 보상 장악·끄기 스위치 격자 세계, 참조 기계를 바꾸면 뒤집히는 지능 순위

## LLM 레퍼런스 노트

- **[Alisa의 LLM 노트 (한국어 번역)](https://github.com/dev-jonghoonpark/book-of-llms-ko)** · [🔗 읽기](https://dev-jonghoonpark.github.io/book-of-llms-ko/)
  - Alisa Liu의 「[Alisa’s book of LLMs](https://alisawuffles.notion.site/alisa-s-book-of-llms)」 비공식 번역 — 인터랙티브 데모가 아니라 **LLM 전반을 수식으로 정리한 학습 노트**. 역전파 shape 추적, 파라미터·FLOPs·메모리 계산, RMSNorm·SwiGLU·RoPE, KV cache·Flash Attention, scaling law, RLHF·DPO, 병렬화까지. 다른 자료를 읽다 수식이 막힐 때 찾아보는 레퍼런스
