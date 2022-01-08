# 0108 map() 메서드 및 JSON 사용(+react.key)

### map() 메서드

##### - map() 메서드란?

배열 내 모든 요소 각각에 주어진 함수를 호출 후 순환한 결과를 모아 새로운 배열을 반환

##### - map() 특징

- 기존 배열을 호출해 새로운 배열을 반환하는 것이므로 기존 배열을 변형시키지는 않음
- return 값 필수

##### - map() 사용법

1. let(or const or var) <신규 변수명> = <배열 타입으로 선언된 변수>.map((<배열 타입 변수의 요소(element)>, <배열 타입 변수 요소의 인덱스(index)(선택)>) => {

   return < map 함수를 사용함으로써 새로운 배열로 나타내고 싶은 callback  함수 형식 >

   });

2. <신규 함수명>() {

   ​	return <배열 타입으로 선언된 변수>.map((<배열 타입 변수의 요소(element)>, <배열 타입 변수 요소의 인덱스(index)(선택)>) => {

   ​		return (

   ​		< map 함수를 사용함으로써 새로운 배열로 나타내고 싶은 callback  함수 형식 >

   ​		);

   ​	});

   }


##### - map() 사용처

반복되는 태그 형식을 갖줬지만 요소마다 속성이 다를 때

(ex)배너, GNB, LNB, 반복되는 list 틀 등)



------



### JSON 사용

##### - JSON 이란?

key, value 값으로 이루어진 자바스크립트 객체 문법으로 경량 데이터 교환 형식

##### - JSON 특징

- 원하는 값(value)을 특정 key에 속성 부여하여 사용
- 다양한 value 타입 지정 가능(number, array, string, object, boolean, null)
- string(문자열) value 지정 시에는 쌍따옴표 필수
- 속성을 부여한 줄에는 마지막 줄을 포함하여 쉼표로 줄 바꿈
- 여러 개의 JSON을 중첩 시켜서 하나의 객체로 지정 가능
- 텍스트 형식으로 작성

##### - JSON 사용법

1. { key: value }

2. {

   ​	key1: value1,

   ​	key2: value2,

   ​	key3: value3,

   }

3. const <신규 변수명> = {

   ​	arrayJsonKey1: [

   ​		{

   ​			key1: value1,

   ​			key2: value2,

   ​		}

   ​		{

   ​			key1: value3,

   ​			key2: value4,

   ​		}

   ​		{

   ​			key2: value5,

   ​			key3: value6,

   ​		}

   ​	],

   ​	JsonKey2: jsonValue2,

   ​	JsonKey3: jsonValue3,

   }

##### - JSON 사용처

임시 데이터 저장, 복잡한 데이터 모델 단순화 등

(ex)배너 묶음 배열 표현, 메뉴 묶음 배열 표현 등)



------



### React.key

##### - React.key 란?

컴포넌트 배열을 렌더링했을 때 어떤 원소에 변동이 있었는지 알아내려고 사용하는 고유값

= 배열 내부의 요소(ID, element, index 등)로 배열 원소의 고유성을 판별할 떄 사용

##### - React.key 특징

- map() 메서드와 같이 사용 추천
- 추출을 대상으로 하는 element에 key를 부여(사용법 참조)

##### - React.key 사용법

1. <신규 함수명>() {

   ​	return <배열 타입으로 선언된 변수>.map((<배열 타입 변수의 요소(element)>, <배열 타입 변수 요소의 인덱스(index)(선택)>) => {

   ​		return (

   ​			<태그명 key={index}>

   ​				<태그명>{element.key1}</태그명>
   ​          	  <태그명>{element..key2}</태그명>

   ​			</태그명>

   ​		);

   ​	});

   }

2. const <신규 변수명> = <배열 타입으로 선언된 변수>.map((<배열 타입 변수의 요소(element)>, <배열 타입 변수 요소의 인덱스(index)(선택)>) => {

   ​	return (

   ​			<태그명 key={index}>

   ​				{element}

   ​			</태그명>

   ​	);

   });

##### - React.key 사용처

list 형식의 배열에서 각각의 요소에 속성이 부여되어 있을 때