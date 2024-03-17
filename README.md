# COVID19-Classification

- 진행날짜 : 2020.06.20 ~ 2020.07.06


- 그동안 Vision관련 논문 읽은 것을 바탕으로 실제 데이터에 적용해보고, 코드로 구현해봤다!
- 옛날 노트북인 core i3로 플젝을 진행했는데 계속 Memory Error가 떴다.
- 코랩으로 갈아탔다. Colab 처음 경험해봤는데 GPU는 신세계였다.
- 이미지 데이터라서 그런지 몰라도 Neaural Net은 컴퓨터 성능이 가장 중요한 것 같다.

</br>
</br>



 # 느낀 점
 > 우선 논문마다, 사이트 마다 용어가 달랐다. 내가 읽은 mobile net과 effecient net 같은 경우, filter라고 되어있는 부분이 어떤 사이트에서는 window라고도 하고, 어떤 곳에서는 kernel이라고 표현했다. 그 용어가 똑같은 개념이라는 것을 인식하기 까지 굉장히 헷갈렸다.
 
 # 덧,
- Efficient Net
  - Overfitting 발생 (Train data와 Validation data 차이 심각 -> Test data가기 전부터 과적합됨)
  - 아마도 확진자 데이터가 적어서 Auto-Augmentation 을 진행했는데, 이것이 원인이 된 것 같다.

- VGG, DenseNet, WideResNet 에서는 EffNet만큼의 오버피팅 발생하지 않음.
  - 하이퍼 파라미터들의 관계를 미리 정해놓아서 오버피팅이 발생한것이 아닌가... 하는 생각도 드는데 정확한 건 아니니 좀 더 생각해봐야한다!

- 오 생각해보니까 폐 CT임 -> 좌우 대칭 -> 그럼 좌우 반전 agumentation 해도 데이터 증폭 아니라 그냥 같은 데이터를 2배 한 꼴이 된것 같음.
- 그래서 당연히 오버피팅 일어난 듯 싶음.
- 앞으로는 생각하면서 진행하기 -> 그냥 무작정 step을 따라서 하지 않을 것.
