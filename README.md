# 코딩 컨벤션
### (최종 아님)

---
## 구분
캐멀 케이스 (또는 캐멀)
- 띄어쓰기를 각 단어의 첫 글자를 대문자로 만들어 구분하는 형식
- ex) camelCase

파스칼 케이스 (또는 파스칼):
-  캐멀과 동일한, 맨 앞글자가 대문자인 형식
- ex) PascalCase


---

## 규칙
#### 몇가지 예외를 제외하고, 모든 변수명은 캐멀, 그 외 모든 함수/클래스/열거형/구조/네임스페이스 등은 파스칼 케이스로 작성합니다
> public과 private을 구분짓는 요소는, 말 그대로 `public`과 `private` attribute여야 합니다.  
> 이를 대소문자로 구분하는 것은 위험할 뿐 아니라,  
> 부모-자식 관계의 `protected`와, 어셈블리간의 `internal` attribute를 표현하는 방식에서 모호성이 존재합니다.  
>		internal 붙었다고 클래스를 캐멀로 적을 수는 없잖아요 :)
	
	같은 맥락으로 
	따라서 모든 변수명은 캐멀, 그 외 "특별한" 것들은 파스칼로 통일합니다.
	예외로 const 변수는 전체를 대문자로 표시하며, 띄어쓰기는 언더바( _ )로 구분합니다.

3. 
