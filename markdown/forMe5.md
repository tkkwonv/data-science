5.블럭과 테이블
===========
5-1.블럭
------------------
블럭은 이 문법 설명서를 쭉 보면서 가장 많이 본 부분이기도 합니다. 제가 코드를 보여드릴 때 회색 상자에 코드를 넣었던 것을 기억하실 겁니다. 만약 그 회색 상자가 아니라 그냥 깃헙 기스트에 작성했다면 알아서 변환되어 보이기 때문에 코드를 그대로 보여줄 수 없었을 겁니다. 이걸 해결하기 위한 문법이 바로 코드블럭입니다. 코드블럭을 만드는 방법은 여러가지가 있는데 가장 쉬운 방법부터 올라가 보도록 하겠습니다.

먼저 가장 쉬운 방법은 스페이스바를 4번 누르는 방법입니다.
```
    for(i=0; i<10; i++) {
    	cout << “게임하고싶다” << endl;
    }
```
이 코드는 c++코드입니다. 이 파일의 확장자가 마크다운 파일이기 때문에 코드가 변환되지는 않겠지만 코드라는 의미를 살리기 위해 넣었습니다. 스페이스바를 4번 써서 조금 띄어져 있는 게 보이시나요? 안보이시더라도 이해하시면 됩니다. 다음 방법은 임의로 상자를 구분하는 방식입니다.
~~~
```
for(i=0; i<10; i++) {
	cout << “게임하고싶다” << endl;
}
```
~~~
```
~~~
for(i=0; i<10; i++) {
	cout << “게임하고싶다” << endl;
}
~~~
```
이 방법은 보시는 바와 같이 두 가지 방법이 있습니다. 하나는 \```처럼 ‘ \` ’문자를 3번 쓰는 방법, 다른 하나는 \~~~처럼 ‘ ~ ’를 3번 쓰는 방법입니다. 사실 공식적으로 깃헙에서는 \```를 사용하라고 하는 것 같습니다. 하지만 \~~~도 되기는 됩니다. 또 하지만 사실\~~~는 \```를 쉬프트키를 누르고 친 것과 같기때문에 \```가 더 편합니다. 판단은 여러분에게 맡깁니다.

위에서 사용한 3가지 방법은 모두
```
for(i=0; i<10; i++) {
	cout << “게임하고싶다” << endl;
}
```
처럼 보이게 됩니다. 결국 방법만 다르지 보여지는 방식은 같다는 얘기이니 편한것을 골라서 쓰시면 됩니다. 참고로 저는 \```을 가장 많이 사용합니다.

코드블럭은 이것 말고도 작게 쓰는 방법이 존재합니다. 사실 한줄정도의 코드를 쓰기 위해 커다락 코드블럭을 만드는 건 조금 이상하죠. 그 방식은 바로 이렇습니다.
```
`printf(“스팀 여름세일”);`
```
아주 쉽습니다. 방법은 위에서 설명했던 ‘ \` ’기호를 따옴표처럼 코드 양 끝에 열고 닫아주면 됩니다. 그러면 결과는 `이렇게`나오게 됩니다.

코드블럭을 보여주는 기본적인 방식은 저게 끝이지만 깃헙의 추가적인 기능이 하나 더 있습니다. 바로 언어에 따른 코드표현입니다. 설명을 따로 드리겠지만 코드를 먼저 보여드리겠습니다.
~~~
```javascript
if (gameIsFun) {
return true;
}
```
~~~
이런 방식입니다. 아마 그냥 딱 봐도 이해하시겠지만 위에서 설명한 ```방식에 언어를 명시적으로 추가해서 코드를 작성했습니다. 저도 모든 언어를 시도해 보지는 않았지만 대부분 가능합니다. 그리고 저렇게 작성하면 코드는
```javascript
if (gameIsFun) {
return true;
}
```
처럼 보이게 됩니다. 조금 더 컬러풀해졌죠? 우리가 흔히 사용하는 코드 편집기들이 코드에는 색이 있다보니 아무래도 개발자들은 코드에 색이 있는 편이 눈에 더 잘 들어옵니다. 가능하다면 이 기능을 사용하는걸 추천하겠습니다. 블럭의 설명은 여기까지이고 테이블로 들어가겠습니다.

******************************************

5-2.테이블
--------------------
테이블은 html같은 언어 뿐만 아니라 한글파일이나 다른 워드에서도 많이 사용하는 기능입니다. 가로 몇칸 세로 몇칸을 지정해서 만드는 것이 가능하죠. 방법은 아주 간단합니다. 
```
머리1 | 머리2 | 머리3 | 뚝배기
---- | ---- | ---- | ----
다리 | 다리1 | 다리2 | 뚝배기깹니다
금 | 의 | 환 | 향
```
와 같은 방식입니다. ‘ | ’이 문자는 백슬레시 혹은 원화모양 버튼을 쉬프트 버튼을 누르고 누르면 됩니다. 제가 위에서 만든 코드는 가로4칸 세로3칸인 테이블로 머리부분에서 칸수를 정하고 밑에 ‘ - ’문자를 써서 구분을 해준 후 칸에 맞게 밑으로 늘려가면 됩니다. 
이 코드는 실제로

머리1 | 머리2 | 머리3 | 뚝배기
---- | ---- | ---- | ----
다리 | 다리1 | 다리2 | 뚝배기깹니다
금 | 의 | 환 | 향

처럼 보이게 됩니다.

보시면 아시겠지만 테이블 각 칸의 크기는 세로칸에서 가장 긴 칸에 맞춰서 조절됩니다. 그리고 자동으로 좌측정렬로 글자가 조정됩니다. 크기와 글자 쏠림을 설정하는 것은 html처럼 직접 설정하면 가능하지만 저는 마크다운에서 그렇게 까지 할 필요성을 못 느껴서 적지 않겠습니다. 애초에 마크다운이라는 언어 자체가 편의성과 빠른 작성 그리고 이해하기 편한 것을 목적으로 했기 때문에 html같이 작성해 버리면 큰 의미가 없어진다고 생각합니다.  

참고로 중간에 빈칸을 넣고싶으면 간단하게 그냥 칸을 비우면 됩니다.
```
머리1 | 머리2 | 머리3 | 뚝배기
---- | ---- | ---- | ----
다리 | | | 뚝배기깹니다
금 | 의 | 환 | 향
```
이렇게 말입니다. 그러면 실제로는

머리1 | 머리2 | 머리3 | 뚝배기
---- | ---- | ---- | ----
다리 | | | 뚝배기깹니다
금 | 의 | 환 | 향

이와 같이 칸이 비어서 나오게 됩니다.  
여기까지가 블럭과 테이블에대한 내용이었습니다.