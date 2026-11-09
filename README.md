# how-ai-works

AI가 실제로 어떻게 동작하는지 — 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료 모음입니다.

각 주제는 별도의 레포로 관리되며, 모두 GitHub Pages로 배포되어 있어 설치 없이 바로 실험해 볼 수 있습니다.

> [K-DEVCON AI 스터디](https://k-devcon.com/channel/6/post/563)를 준비하며 만들고 있는 자료들입니다. 계속 추가될 예정입니다.

## 📖 용어 사전

- **[dictionary.md](dictionary.md)**
  - 자료를 읽다 막히는 용어 정리 — 텐서, 단방향/양방향 RNN, GRU, Post-LN/Pre-LN

## 기초

- **[How Mean and Variance Works](https://github.com/dev-jonghoonpark/how-mean-and-variance-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mean-and-variance-works/)
  - 평균과 분산에서 정규화 층까지 — **BN·LN·IN·GN은 같은 수식에 축만 다르다**. 편차를 제곱하는 이유, 칸 클릭 축 선택기
- **[How Normal Distribution Works](https://github.com/dev-jonghoonpark/how-normal-distribution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-normal-distribution-works/)
  - 정규분포와 중심극한정리 — AI에 종 모양이 자꾸 나오는 이유. 골턴 보드, Xavier/He 초기화의 1/√d, MSE = 가우시안 가정
- **[How Gradient Descent Works](https://github.com/dev-jonghoonpark/how-gradient-descent-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gradient-descent-works/)
  - 경사 하강법이 지그재그로 움직이는 이유 — 학습률에 따른 수렴·진동·발산, GD/Momentum/Adam 비교, 조건수 κ
- **[How SGD Works](https://github.com/dev-jonghoonpark/how-sgd-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-sgd-works/)
  - 확률적 경사 하강법 — **GD와의 차이는 기울기를 몇 개로 계산하느냐(B) 하나뿐**. 1/√B 법칙, 노이즈로 지역 최솟값 탈출
- **[How Adam Works](https://github.com/dev-jonghoonpark/how-adam-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-adam-works/)
  - Adam (Kingma & Ba, 2015) — **파라미터마다 따로 재는 보폭**. 이동 평균과 편향 보정, Adam vs AdamW, 학습 메모리의 절반이 m·v인 이유
- **[How Backprop Works](https://github.com/dev-jonghoonpark/how-backprop-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-backprop-works/)
  - 순전파·손실·역전파 — 계산 그래프 위의 연쇄 법칙, 사인 곡선을 배우는 신경망, 난수 필터가 소벨 필터로 수렴하는 과정
- **[How Convolution Works](https://github.com/dev-jonghoonpark/how-conv-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-conv-work/)
  - 합성곱은 실제로 무엇을 하는가 — "뒤집고·밀고·곱하고·더하기"에서 합성곱 정리, 2D 필터, 1×1 conv, 스트라이드·패딩까지
- **[How Fourier Transform Works](https://github.com/dev-jonghoonpark/how-fourier-transform-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-fourier-transform-works/)
  - 푸리에 변환·DFT·FFT — **FFT는 DFT를 N log N에 계산하는 알고리즘**. 깁스 현상, 에일리어싱, FFT 재귀 실행기

## AlexNet

- **[How AlexNet Works](https://github.com/dev-jonghoonpark/how-alexnet-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alexnet-works/)
  - AlexNet — 논문의 실제 conv1 커널과 ILSVRC 이미지로 브라우저에서 직접 계산

## ResNet

- **[How ResNet Works](https://github.com/dev-jonghoonpark/how-resnet-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-resnet-work/)
  - ResNet의 동작 원리 — skip connection을 켜고 끄며 직접 실험
- **[ResNet Bottleneck](https://github.com/dev-jonghoonpark/resnet-bottleneck)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-bottleneck/)
  - Bottleneck Block에서 1×1 conv가 하는 일
- **[ResNet의 BatchNorm](https://github.com/dev-jonghoonpark/resnet-batchnorm)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-batchnorm/)
  - 깊은 네트워크에 배치 정규화가 필요한 이유 — γ·β, 30층 신호 전파 시뮬레이션, 학습/추론 모드와 BN folding
- **[ResNet DJL Lab](https://github.com/dev-jonghoonpark/resnet-djl-lab)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-djl-lab/)
  - ResNet v1/v2를 DJL(Java)로 구현 — 차이는 **BN·ReLU·덧셈의 순서** 하나. 고양이 사진 한 장의 학습 한 바퀴를 80단계로
- **[How Dilated Convolution Works](https://github.com/dev-jonghoonpark/how-dilated-conv-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-dilated-conv-works/)
  - Dilated Convolution (Yu & Koltun, 2016) — 풀링 없이 시야 넓히기. 수용 영역의 지수적 확장, gridding effect

## N-gram

- **[How N-gram Works](https://github.com/dev-jonghoonpark/how-n-gram-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-n-gram-work/)
  - n-gram 언어 모델 — 세는 것만으로 다음 단어 예측. 카운트 행렬, 희소성, 스무딩, 퍼플렉시티

## 단어 임베딩

- **[How word2vec Works](https://github.com/dev-jonghoonpark/how-word2vec-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-word2vec-works/)
  - word2vec — "king − man + woman ≈ queen"이 되는 과정. CBOW·Skip-gram, 네거티브 샘플링, 브라우저 SGNS 학습기

## RNN

- **[How RNN Works](https://github.com/dev-jonghoonpark/how-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-works/)
  - RNN 부흥기(2014–2016) 인터랙티브 노트 — min-char-rnn, LSTM 게이트 조작기, Deep Speech 2 빔서치
- **[How char-rnn Works](https://github.com/dev-jonghoonpark/how-char-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-char-rnn-works/)
  - Karpathy 「The Unreasonable Effectiveness of RNNs」(2015) 해설 — 온도 슬라이더, 셰익스피어 LSTM, 해석 가능한 셀
- **[How LSTM Works](https://github.com/dev-jonghoonpark/how-lstm-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-lstm-works/)
  - LSTM은 어떻게 기억하는가 — 기울기 소멸과 셀 상태 레일, 게이트 조작기, 괄호 깊이를 세는 LSTM
- **[How GRU Works](https://github.com/dev-jonghoonpark/how-gru-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gru-works/)
  - GRU (Cho et al., 2014) — **LSTM에서 게이트 하나를 덜어 낸 값**. 가중치가 정확히 3/4, 세지 못하는 대가
- **[How RNN Dropout Works](https://github.com/dev-jonghoonpark/how-rnn-dropout-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-dropout-works/)
  - 드롭아웃이 순환 연결을 피해 가는 이유 (Zaremba et al., 2014) — 손상 횟수 L+1 vs L+1+Δt, PTB 114.5 → 78.4
- **[How Bidirectional RNN Works](https://github.com/dev-jonghoonpark/how-bidirectional-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-bidirectional-rnn-works/)
  - 양방향 RNN — **미래를 보는 대가**. 정확도는 오르지만 실시간에서 못 쓰는 이유, 행 합성곱으로 되돌리기
- **[LSTM Text Generation](https://github.com/dev-jonghoonpark/lstm-text-generation)** · 💻 내 컴퓨터에서 실행
  - 정글북으로 문자 단위 LSTM을 Keras로 직접 학습 — epoch와 temperature에 따른 생성 결과

## 음성 인식 (Deep Speech 2)

- **[How Deep Speech 2 Works](https://github.com/dev-jonghoonpark/how-deep-speech-2-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-deep-speech-2-works/)
  - Deep Speech 2 (Amodei et al., 2015) — 논문의 표와 수식을 직접 계산. 스펙트로그램, CTC, SortaGrad, 스케일링
- **[How Row Convolution Works](https://github.com/dev-jonghoonpark/how-row-convolution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-row-convolution-works/)
  - 행 합성곱 (DS2 3.7절) — 단방향 RNN이 미래를 조금 엿보는 법. τ=19 · 760 ms 지연
- **[How CTC Beam Search Works](https://github.com/dev-jonghoonpark/how-ctc-beam-search-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ctc-beam-search-works/)
  - CTC 빔 서치 (DS2 3.8절) — greedy가 실패하는 이유, prefix beam search 실행기, 언어 모델 재순위
- **[DS2 My Voice](https://github.com/dev-jonghoonpark/ds2-my-voice)** · [🔗 데모](https://dev-jonghoonpark.github.io/ds2-my-voice/) · 💻 내 컴퓨터에서 학습
  - 축소판 DS2를 Zeroth-Korean으로 학습하고 **내 목소리 7분**으로 파인튜닝 — 화자 적응과 망각 비교

## seq2seq

- **[How seq2seq Works](https://github.com/dev-jonghoonpark/how-seq2seq-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-seq2seq-works/)
  - seq2seq (2014) — 인코더·디코더, 고정 길이 병목, 입력 역순 트릭, 브라우저 학습 미니 seq2seq
- **[How Pointer Network Works](https://github.com/dev-jonghoonpark/how-pointer-network-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-pointer-network-works/)
  - Pointer Networks (Vinyals et al., 2015) — **어텐션 분포를 그대로 출력으로**. 볼록 껍질·TSP, 길이 일반화
- **[How Order Matters Works](https://github.com/dev-jonghoonpark/how-order-matters-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-order-matters-works/)
  - Order Matters (Vinyals et al., 2016) — 같은 확률인데 순서를 바꾸면 성능이 달라지는 이유. Read-Process-Write

## 메모리 증강 신경망

- **[How Neural Turing Machines Work](https://github.com/dev-jonghoonpark/how-ntm-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ntm-works/)
  - Neural Turing Machine (Graves et al., 2014) — 망 밖의 N × M 메모리를 미분 가능하게 읽고 쓰기. 내용 주소 = 어텐션

## Transformer

- **[How Attention Works](https://github.com/dev-jonghoonpark/how-attention-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-attention-works/)
  - Attention Is All You Need — Bahdanau attention부터 Q·K·V, causal mask, 멀티헤드, 위치 인코딩까지
- **[그림으로 보는 Transformer](https://github.com/dev-jonghoonpark/illustrated-transformer-ko)** · [🔗 데모](https://dev-jonghoonpark.github.io/illustrated-transformer-ko/)
  - Jay Alammar 「The Illustrated Transformer」 순서로 새로 쓴 해설 — **그림 속 숫자를 직접 계산**
- **[How Transformer Works](https://github.com/dev-jonghoonpark/how-transformer-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-transformer-works/)
  - Transformer (Vaswani et al., 2017) 블록과 모델 전체 — **잔차와 LayerNorm의 순서**, 파라미터 계산기, KV 캐시
- **[How Positional Encoding Works](https://github.com/dev-jonghoonpark/how-positional-encoding-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-positional-encoding-works/)
  - 위치 인코딩이 sin과 cos를 **함께** 쓰는 이유 — "k칸 뒤"가 회전 행렬이 되는 성질, RoPE까지
- **[How BERT Works](https://github.com/dev-jonghoonpark/how-bert-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-bert-works/)
  - BERT (Devlin et al., 2019) — GPT와의 구조 차이는 **어텐션 마스크 한 장**, 진짜 기여는 학습 과제
- **[How GPT Works](https://github.com/dev-jonghoonpark/how-gpt-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gpt-works/)
  - GPT가 다음 단어를 고르는 과정 — 3Blue1Brown DL5~7을 따라 온도, 임베딩, 어텐션, MLP, 파라미터 계산
- **[How Universal Transformer Works](https://github.com/dev-jonghoonpark/how-universal-transformer-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-universal-transformer-works/)
  - Universal Transformer (Dehghani et al., 2019) — **같은 층을 T번**. 파라미터와 연산의 분리, ACT
- **[Annotated Transformer Modern](https://github.com/dev-jonghoonpark/annotated-transformer-modern)** · 💻 내 컴퓨터에서 학습
  - The Annotated Transformer를 최신 라이브러리에서 돌아가게 4곳만 고친 노트북
- **[Annotated Transformer Step by Step](https://github.com/dev-jonghoonpark/annotated-transformer-step-by-step)** · [🔗 데모](https://dev-jonghoonpark.github.io/annotated-transformer-step-by-step/)
  - 빈 파일에서 시작해 **18단계 만에** Annotated Transformer 원본 코드 완성 — 단계별 diff와 실행 결과

## 강화학습과 탐색 (AlphaGo)

- **[How AlphaGo Works](https://github.com/dev-jonghoonpark/how-alphago-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alphago-works/)
  - AlphaGo (Silver et al., 2016) — 분류용 CNN이 머리만 바꿔 형세 판단기가 되는 과정, MCTS 실행기

## 스케일링과 병렬화

- **[How Scaling Laws Work](https://github.com/dev-jonghoonpark/how-scaling-laws-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-scaling-laws-work/)
  - Scaling Laws (Kaplan et al., 2020) — **loss는 N·D·C의 멱법칙**. 175B loss 외삽, 연산 최적 배분, Chinchilla
- **[How GPipe Works](https://github.com/dev-jonghoonpark/how-gpipe-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gpipe-works/)
  - GPipe (Huang et al., 2019) — 층으로 자르고 마이크로배치로 흘리기. 버블 계산, 파이프라인 타임라인, 재계산
- **[How FSDP Works](https://github.com/dev-jonghoonpark/how-fsdp-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-fsdp-works/)
  - FSDP — **저장은 1/N씩 나누고, 쓸 때만 모은다**. 메모리 → 통신 → DDP → FSDP 순으로 쌓아 올리는 한 스텝 재생기
- **[How Mesh-TensorFlow Works](https://github.com/dev-jonghoonpark/how-mesh-tensorflow-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mesh-tensorflow-works/)
  - Mesh-TensorFlow (Shazeer et al., 2018) — **차원에 이름을 붙여 메시에 나누면 같은 SPMD 프로그램이 모델 병렬**
- **[How Parallelism Works](https://github.com/dev-jonghoonpark/how-parallelism-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-parallelism-works/)
  - 데이터·텐서·파이프라인·컨텍스트·전문가 병렬 — **하이브리드가 표준**. ZeRO 계산기, Llama 3 405B의 4D 병렬화

## 표현과 관계 추론

- **[How VLAE Works](https://github.com/dev-jonghoonpark/how-vlae-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-vlae-works/)
  - Variational Lossy Autoencoder (Chen et al., 2017) — **잠재 코드에는 디코더가 못 하는 정보만**. posterior collapse
- **[How Relation Network Works](https://github.com/dev-jonghoonpark/how-relation-network-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-relation-network-works/)
  - Relation Network (Santoro et al., 2017) — **모든 객체 쌍에 같은 함수 g를 적용하고 더한다**. Sort-of-CLEVR
- **[How Relational RNN Works](https://github.com/dev-jonghoonpark/how-relational-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-relational-rnn-works/)
  - Relational RNN (Santoro et al., 2018) — 메모리 갱신을 셀프 어텐션으로. N번째로 먼 점, BoxWorld

## 복잡도와 압축

- **[How Kolmogorov Complexity Works](https://github.com/dev-jonghoonpark/how-kolmogorov-complexity-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-kolmogorov-complexity-works/)
  - 콜모고로프 복잡도 — **규칙성 = 짧게 적을 수 있음 = 예측할 수 있음**. 불변성 정리, 계산 불가능성
- **[How Complexodynamics Works](https://github.com/dev-jonghoonpark/how-complexodynamics-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-complexodynamics-works/)
  - Complexodynamics (Aaronson, 2011) — 엔트로피와 흥미로운 복잡도의 차이. 커피 오토마톤, 정교함
- **[How MDL Works](https://github.com/dev-jonghoonpark/how-mdl-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mdl-works/)
  - MDL (Hinton & van Camp, 1993) — **일반화는 압축이다**. 가중치·미스핏 비트, bits-back, ELBO로의 연결

## 지능의 정의와 안전

- **[How Universal Intelligence Works](https://github.com/dev-jonghoonpark/how-universal-intelligence-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-universal-intelligence-works/)
  - 보편 지능 (Legg & Hutter, 2007) — **단순한 환경일수록 크게 쳐 준 성적의 가중합**. 작은 AIXI

## LLM 레퍼런스 노트

- **[Alisa의 LLM 노트 (한국어 번역)](https://github.com/dev-jonghoonpark/book-of-llms-ko)** · [🔗 읽기](https://dev-jonghoonpark.github.io/book-of-llms-ko/)
  - Alisa Liu의 LLM 학습 노트 번역 — 파라미터·FLOPs·메모리, RoPE, KV cache, RLHF·DPO, 병렬화 수식 레퍼런스
