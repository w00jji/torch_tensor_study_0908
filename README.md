# torch_tensor_sudy_0908

study process
### 1. 파이토치 모듈 이해

※ 텐서 구조가 익숙해야 이미지,시계열에 대해서 잘 조작 할 수 있다.
ex) 시계열 4차원
이미지 (묶음사이즈 , 크기 , 세로 )
시계열 (묶음사이즈 , 시간길이, 크기 , 세로 )

- 텐서 조작 (참고 : 위키 독스)

![image](https://github.com/user-attachments/assets/f4d351c5-71d2-4cb0-8a48-aea9779f1558)


1) 파이토치에서는 텐서 타입만 가능 -> 텐서 shape 알아야함

tensor study process
- 텐서 조작
  1) 넘파이로 텐서 만들기
  2) 파이토치로 텐서 만들기
  3) 브로드캐스팅
  4) 곱셈 (행렬곱)
  5) 평균
  6) 덧셈
 
 2차원 , 3차원 dim 인덱스 순서
 - 2D : 세로 dim = 0 , 가로 dim = 1
 - 3D: 0 z 방향, 1 세로, 2 가로

   7) Max와 ArgMax => 중요!! classification에 사용 argmax란 텐서에서 가장 큰 값의 인덱스를 반환하는 것이다.
   8) 뷰(view)
   9) 스퀴지(Squeeze) - 1인 차원을 제거한다.
   10) 언스퀴지(Unsqueeze) - ★특정 위치★에 1인 차원을 추가한다.
       - 차원추가① - Unsqueeze로 차원 추가
       - view로도 Unsqueeze가 가능하다.
       - 차원추가③ - 차원을 특정 위치에 추가
   11) 텐서타입은 뭐가 있나요?

       ![image](https://github.com/user-attachments/assets/d25296bf-a45c-43b6-af86-192bd96a7c96)
   12) 연결하기 : cat => 차원을 먼저 늘린 후에, 쌓아야 함
   13) 쌓기 또는 스택킹(Stacking) => 알아서 차원이 늘어남
   14) ones_like와 zeros_like - 0으로 채워진 텐서와 1로 채워진 텐서
   15) 15) 덮어쓰기 연산 : 중요!!!  , _를 붙이면 계산과 동시에 기존의 값을 덮어쓰기 한다.
