# 코딩 컨벤션
##### (최종 아님)
---

### 구분
##### 캐멀 케이스 (또는 캐멀)
- 띄어쓰기를 각 단어의 첫 글자를 대문자로 만들어 구분하는 형식
- ex) camelCase

##### 파스칼 케이스 (또는 파스칼):
-  캐멀과 동일하지만, 맨 앞글자가 대문자인 형식
- ex) PascalCase


---

## 규칙
### 몇가지 예외를 제외하고, 모든 변수명은 캐멀, 그 외 모든 함수/클래스/열거형/구조/네임스페이스 등은 파스칼 케이스로 작성합니다
> 접근성인 `public`과 `private`을 구분짓는 요소는, 말 그대로 `public`과 `private` 키워드여야 합니다.  
> 이를 대소문자로 구분하는 것은 위험할 뿐 아니라,  
> 부모-자식 관계의 `protected`와, 어셈블리간의 `internal`\`extern` 키워드를 사용할 때 모호성이 존재합니다.  
>     *internal 붙었다고 클래스를 캐멀로 적을 수는 없잖아요* :)
	
> 따라서 모든 변수명은 캐멀, 그 외 "특별한" 것들은 파스칼로 통일하고, 같은 맥락으로 private 변수 앞에 언더바 ( _ ) 또한 사용하지 않습니다.
> 예외로 const 변수는 전체를 대문자로 표시하며, 띄어쓰기는 언더바로 구분합니다.  
> 이는 특별한 상황에서 배열을 const식으로 사용하고 싶은 경우에도 유효합니다.

![image](https://github.com/user-attachments/assets/a7e1f1f0-efe5-4eef-961a-4cf5a031893f "예시")

---
### 가독성을 위해 불필요한 키워드의 사용은 지양합니다.
> 선언문 앞에 별도의 키워드를 지정하지 않은 경우 대부분 private으로 지정됩니다. (클래스의 경우 조금 다른데, 어쨌든 역할은 비슷해 굳이 다루지 않습니다.)  
> 이를 활용하여, 불필요한 키워드의 사용을 줄이고, 유니티 기본 제공 함수들과 통일성을 두며, 변수들이 여럿 나열되어 있을 경우에도 가독성을 유지합니다.
![image](https://github.com/user-attachments/assets/9192888e-2672-4e06-99e6-47f836e78c6a "생략 X")
![image](https://github.com/user-attachments/assets/3ec8435a-ff95-4ffd-8633-9eb5a4938185 "생략 O")





  	
```
namespace NAME {
	enum ENUM {
	}

	class CLASS {
	}
}

##### 변수는 종류별로 선언하지 않고, 지엽적으로 묶어 선언합니다
###### region을 사용하고 모든 변수가 오직 그 안에서만 사용된다는 제한 하에서, 변수를 region 내에 선언하는 것을 허용합니다. 
