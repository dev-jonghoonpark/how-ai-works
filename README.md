# how-ai-works

AI가 실제로 어떻게 동작하는지 — 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료 모음입니다.

각 주제는 별도의 레포로 관리되며, 모두 GitHub Pages로 배포되어 있어 설치 없이 바로 실험해 볼 수 있습니다.

> [K-DEVCON AI 스터디](https://k-devcon.com/channel/6/post/563)를 준비하며 만들고 있는 자료들입니다. 계속 추가될 예정입니다.

## 📖 용어 사전

- **[dictionary.md](dictionary.md)**
  - 자료를 읽다 막히는 용어 정리

## 기초

- **[How Mean and Variance Works](https://github.com/dev-jonghoonpark/how-mean-and-variance-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mean-and-variance-works/)
  - 평균·분산에서 정규화 층까지 — BN·LN·GN은 같은 수식, 축만 다르다
- **[How Normal Distribution Works](https://github.com/dev-jonghoonpark/how-normal-distribution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-normal-distribution-works/)
  - 정규분포와 중심극한정리 — AI에 종 모양이 자꾸 나오는 이유
- **[How Gradient Descent Works](https://github.com/dev-jonghoonpark/how-gradient-descent-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gradient-descent-works/)
  - 경사 하강법 — 학습률에 따라 갈리는 수렴·진동·발산
- **[How SGD Works](https://github.com/dev-jonghoonpark/how-sgd-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-sgd-works/)
  - SGD — GD와의 차이는 기울기를 몇 개로 계산하느냐 하나뿐
- **[How Adam Works](https://github.com/dev-jonghoonpark/how-adam-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-adam-works/)
  - Adam — 파라미터마다 따로 재는 보폭
- **[How Backprop Works](https://github.com/dev-jonghoonpark/how-backprop-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-backprop-works/)
  - 역전파 — 계산 그래프 위의 연쇄 법칙
- **[How Convolution Works](https://github.com/dev-jonghoonpark/how-conv-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-conv-work/)
  - 합성곱 — 뒤집고·밀고·곱하고·더하기에서 CNN까지
- **[How Fourier Transform Works](https://github.com/dev-jonghoonpark/how-fourier-transform-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-fourier-transform-works/)
  - 푸리에 변환 — FFT는 DFT를 빠르게 계산하는 알고리즘

## AlexNet

- **[How AlexNet Works](https://github.com/dev-jonghoonpark/how-alexnet-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alexnet-works/)
  - AlexNet — 논문의 실제 conv1 커널로 직접 계산

## ResNet

- **[How ResNet Works](https://github.com/dev-jonghoonpark/how-resnet-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-resnet-work/)
  - ResNet의 skip connection 실험
- **[ResNet Bottleneck](https://github.com/dev-jonghoonpark/resnet-bottleneck)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-bottleneck/)
  - Bottleneck Block에서 1×1 conv가 하는 일
- **[ResNet의 BatchNorm](https://github.com/dev-jonghoonpark/resnet-batchnorm)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-batchnorm/)
  - 깊은 네트워크에 배치 정규화가 필요한 이유
- **[ResNet DJL Lab](https://github.com/dev-jonghoonpark/resnet-djl-lab)** · [🔗 데모](https://dev-jonghoonpark.github.io/resnet-djl-lab/)
  - ResNet v1/v2를 DJL(Java)로 구현 — 차이는 BN·ReLU·덧셈의 순서
- **[How Dilated Convolution Works](https://github.com/dev-jonghoonpark/how-dilated-conv-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-dilated-conv-works/)
  - Dilated Convolution — 풀링 없이 시야를 넓히기

## N-gram

- **[How N-gram Works](https://github.com/dev-jonghoonpark/how-n-gram-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-n-gram-work/)
  - n-gram — 세는 것만으로 다음 단어 예측

## 단어 임베딩

- **[How word2vec Works](https://github.com/dev-jonghoonpark/how-word2vec-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-word2vec-works/)
  - word2vec — king − man + woman ≈ queen이 되는 과정

## RNN

- **[How RNN Works](https://github.com/dev-jonghoonpark/how-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-works/)
  - RNN 부흥기(2014–2016) 인터랙티브 노트
- **[How char-rnn Works](https://github.com/dev-jonghoonpark/how-char-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-char-rnn-works/)
  - Karpathy char-rnn(2015) 해설
- **[How LSTM Works](https://github.com/dev-jonghoonpark/how-lstm-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-lstm-works/)
  - LSTM — 셀 상태와 게이트로 기억하기
- **[How GRU Works](https://github.com/dev-jonghoonpark/how-gru-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gru-works/)
  - GRU — LSTM에서 게이트 하나를 덜어 낸 값
- **[How RNN Dropout Works](https://github.com/dev-jonghoonpark/how-rnn-dropout-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-rnn-dropout-works/)
  - 드롭아웃이 순환 연결을 피해 가는 이유 (Zaremba 2014)
- **[How Bidirectional RNN Works](https://github.com/dev-jonghoonpark/how-bidirectional-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-bidirectional-rnn-works/)
  - 양방향 RNN — 미래를 보는 대가
- **[LSTM Text Generation](https://github.com/dev-jonghoonpark/lstm-text-generation)** · 💻 내 컴퓨터에서 실행
  - 문자 단위 LSTM을 Keras로 직접 학습

## 음성 인식 (Deep Speech 2)

- **[How Deep Speech 2 Works](https://github.com/dev-jonghoonpark/how-deep-speech-2-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-deep-speech-2-works/)
  - Deep Speech 2 — 논문의 표와 수식을 직접 계산
- **[How Row Convolution Works](https://github.com/dev-jonghoonpark/how-row-convolution-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-row-convolution-works/)
  - 행 합성곱 — 단방향 RNN이 미래를 조금 엿보는 법
- **[How CTC Beam Search Works](https://github.com/dev-jonghoonpark/how-ctc-beam-search-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ctc-beam-search-works/)
  - CTC 빔 서치 — greedy가 실패하는 이유
- **[DS2 My Voice](https://github.com/dev-jonghoonpark/ds2-my-voice)** · [🔗 데모](https://dev-jonghoonpark.github.io/ds2-my-voice/) · 💻 내 컴퓨터에서 학습
  - 축소판 DS2를 내 목소리로 파인튜닝

## seq2seq

- **[How seq2seq Works](https://github.com/dev-jonghoonpark/how-seq2seq-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-seq2seq-works/)
  - seq2seq — 인코더·디코더와 고정 길이 병목
- **[How Pointer Network Works](https://github.com/dev-jonghoonpark/how-pointer-network-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-pointer-network-works/)
  - Pointer Networks — 어텐션 분포를 그대로 출력으로
- **[How Order Matters Works](https://github.com/dev-jonghoonpark/how-order-matters-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-order-matters-works/)
  - Order Matters — 순서를 바꾸면 성능이 달라지는 이유

## 메모리 증강 신경망

- **[How Neural Turing Machines Work](https://github.com/dev-jonghoonpark/how-ntm-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-ntm-works/)
  - Neural Turing Machine — 미분 가능한 외부 메모리

## Transformer

- **[How Attention Works](https://github.com/dev-jonghoonpark/how-attention-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-attention-works/)
  - Attention — Q·K·V, 마스크, 멀티헤드
- **[그림으로 보는 Transformer](https://github.com/dev-jonghoonpark/illustrated-transformer-ko)** · [🔗 데모](https://dev-jonghoonpark.github.io/illustrated-transformer-ko/)
  - The Illustrated Transformer를 따라 그림 속 숫자를 직접 계산
- **[How Transformer Works](https://github.com/dev-jonghoonpark/how-transformer-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-transformer-works/)
  - Transformer 블록과 모델 전체 — 잔차와 LayerNorm의 순서
- **[How Positional Encoding Works](https://github.com/dev-jonghoonpark/how-positional-encoding-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-positional-encoding-works/)
  - 위치 인코딩이 sin과 cos를 함께 쓰는 이유
- **[How BERT Works](https://github.com/dev-jonghoonpark/how-bert-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-bert-works/)
  - BERT — GPT와의 차이는 어텐션 마스크 한 장
- **[How GPT Works](https://github.com/dev-jonghoonpark/how-gpt-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gpt-works/)
  - GPT가 다음 단어를 고르는 과정 (3Blue1Brown DL5~7)
- **[How Universal Transformer Works](https://github.com/dev-jonghoonpark/how-universal-transformer-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-universal-transformer-works/)
  - Universal Transformer — 같은 층을 T번 반복
- **[Annotated Transformer Modern](https://github.com/dev-jonghoonpark/annotated-transformer-modern)** · 💻 내 컴퓨터에서 학습
  - The Annotated Transformer를 최신 라이브러리로
- **[Annotated Transformer Step by Step](https://github.com/dev-jonghoonpark/annotated-transformer-step-by-step)** · [🔗 데모](https://dev-jonghoonpark.github.io/annotated-transformer-step-by-step/)
  - 빈 파일에서 18단계로 Annotated Transformer 완성

## 강화학습과 탐색 (AlphaGo)

- **[How AlphaGo Works](https://github.com/dev-jonghoonpark/how-alphago-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-alphago-works/)
  - AlphaGo — 정책망·가치망과 MCTS

## 스케일링과 병렬화

- **[How Scaling Laws Work](https://github.com/dev-jonghoonpark/how-scaling-laws-work)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-scaling-laws-work/)
  - Scaling Laws — loss는 규모의 멱법칙
- **[How GPipe Works](https://github.com/dev-jonghoonpark/how-gpipe-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-gpipe-works/)
  - GPipe — 층으로 자르고 마이크로배치로 흘리기
- **[How FSDP Works](https://github.com/dev-jonghoonpark/how-fsdp-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-fsdp-works/)
  - FSDP — 저장은 나누고, 쓸 때만 모은다
- **[How Mesh-TensorFlow Works](https://github.com/dev-jonghoonpark/how-mesh-tensorflow-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mesh-tensorflow-works/)
  - Mesh-TensorFlow — 차원에 이름을 붙여 메시에 나누기
- **[How Parallelism Works](https://github.com/dev-jonghoonpark/how-parallelism-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-parallelism-works/)
  - 데이터·텐서·파이프라인·컨텍스트·전문가 병렬과 Llama 3의 4D 병렬화

## 표현과 관계 추론

- **[How VLAE Works](https://github.com/dev-jonghoonpark/how-vlae-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-vlae-works/)
  - Variational Lossy Autoencoder — 잠재 코드에 무엇이 담기나
- **[How Relation Network Works](https://github.com/dev-jonghoonpark/how-relation-network-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-relation-network-works/)
  - Relation Network — 모든 객체 쌍에 같은 함수
- **[How Relational RNN Works](https://github.com/dev-jonghoonpark/how-relational-rnn-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-relational-rnn-works/)
  - Relational RNN — 메모리 갱신을 셀프 어텐션으로

## 복잡도와 압축

- **[How Kolmogorov Complexity Works](https://github.com/dev-jonghoonpark/how-kolmogorov-complexity-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-kolmogorov-complexity-works/)
  - 콜모고로프 복잡도 — 규칙성 = 짧게 적을 수 있음
- **[How Complexodynamics Works](https://github.com/dev-jonghoonpark/how-complexodynamics-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-complexodynamics-works/)
  - Complexodynamics — 엔트로피와 흥미로운 복잡도의 차이
- **[How MDL Works](https://github.com/dev-jonghoonpark/how-mdl-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-mdl-works/)
  - MDL — 일반화는 압축이다 (Hinton & van Camp 1993)

## 지능의 정의와 안전

- **[How Universal Intelligence Works](https://github.com/dev-jonghoonpark/how-universal-intelligence-works)** · [🔗 데모](https://dev-jonghoonpark.github.io/how-universal-intelligence-works/)
  - 보편 지능 — 단순한 환경일수록 크게 쳐 준 성적의 합

## LLM 레퍼런스 노트

- **[Alisa의 LLM 노트 (한국어 번역)](https://github.com/dev-jonghoonpark/book-of-llms-ko)** · [🔗 읽기](https://dev-jonghoonpark.github.io/book-of-llms-ko/)
  - Alisa Liu의 LLM 학습 노트 번역 — 수식 레퍼런스
