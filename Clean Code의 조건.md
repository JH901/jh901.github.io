# Clean Code의 조건
-------------------------------------------------------------------------
### Clean code란?
> 잘 동작하는 코드 + 부가 설명이 필요 없는 코드 



### 1.  검색 가능한 변수명 사용.
> 부적절한 예
~~~java
	setInterval(countSecond, 86400);
~~~

> 적절한 예
~~~java
	const SECONDS_IN_A_DAY = 86400;
	setInterval(countSecond, SECONDS_IN_A_DAY);
~~~



### 2. 함수명은 반드시 동사로.
> 부적절한 예
~~~java
	function userData(){
		//..
	}
	
	const data = userData();
~~~

> 적절한 예
~~~java
	function loadUserData(){
		//..
	}
	
	const userData = loadUserData();
~~~
> 함수명을 동사 형태로 작성하게되면 해당 함수의 역활을 보다 명확하게 이해할 수 있다.
> 함수가 여러가지 역할을 수행한다면 해당 함수를 분할해야할 가능성을 염두해 두어야 한다.
> **즉, 함수는 단 한가지 액션만 수행해야 한다.**



### 3.  함수의 인수는 3개 이하가 적당

** 3개 이상의 인수가 필요할 경우 Object를 사용하여 param사용! **
> 부적절한 예
~~~java 
	function makePayment(int price, String productId, int size, int quantity, String userId){
		//..
	}
	
	makePayment(35, "product5", 7, 2, "user1");
~~~

> 적절한 예
~~~java
	function makePayment({int price, String productId, int size, int quantity, String userId}){
		//..
	}
	
	makePayment({
        price : 35,
        productId : "product5",
        size : 7,
        quantity : 2,
        userId : "user1"
	});
~~~

> 함수 인자의 수를 제한하는것이 함수를 이해하기 쉽고, 필요한 인자수를 정확하게 알수있게 한다.



### 4.  Boolean 값을 param으로 함수에 보내지 않는것을 추천 .
> 부적절한 예
~~~java
	function sendMessage(String message, boolean isPrivate){
		if(isPrivate){
		//..
		}else {
		//..
		}
	}
	
	sendMessage("this is a public message", false);
	sendMessage("this is a secret message", true);
~~~

> 적절한 예
~~~java
	function sendPublicMessage(String message){
	//..
	}
	function sendPrivateMessage(String message){
	//..
	}
	
	sendPublicMessage("this is a public message");
	sendPrivateMessage("this is a secret message");
~~~
> 대부분의 경우 Boolean값이 인자로 보내진다는 것은 함수안에 if-else가 존재함을 의미
> 함수안에 2가지 이상의 액션을 구현하기보다 함수를 2개로 구분하는것을 추천



### 5. 너무 축약된 변수명 사용 금지
> 부적절한 예
~~~java
	userList.forEach((u, i) => {
		sendEmail(u);
		addToCount(i);
	});
~~~

> 적절한 예
~~~java
	userList.forEach((user, currentNumber) => {
		sendEmail(user);
		addToCount(currentNumber);
	});
~~~

> 변수명을 이해하기 위해 시간투자 할 필요없이 바로 이해할 수 있도록 정확하게 기입!!





[출처-노마드 코더 Nomad Coders] (https://www.youtube.com/watch?v=Jz8Sx1XYb04)



