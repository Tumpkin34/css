# CSS란?
	CSS는 Cascading Style Sheets의 약자이다.
	CSS는 HTML요소들이 각종 미디어에서 어떻게 보이는 가를 정의하는 데 사용한다.
	스타일을 HTML문서로부터 분리하는 것이 가능해진다.

# CSS를 사용하는 이유
	HTML만으로 웹 페이지를 제작할 경우, HTML 요소의 세부 스타일을
	일일이 따로 지정해주어야 하기 때문에 많은 시간이 걸리며, 완성한 후에도
	스타일의 변경 및 유지보수가 매우 힘들어진다.
	이 문제점을 해소하기 위해서 W3C에서 만든 스타일 시트 언어가 바로 CSS이다.
	웹 페이지의 스타일을 별도의 파일로 저장할 수 있게 해줌으로써 사이트의 전체 스타일을
	손쉽게 제어할 수 있게 된다. 또한 웹 사이트의 스타일을 일관성 있게 유지할 수 있도록 해주며,
	그에 따른 유지보수 또한 쉬워진다.

# CSS 문법
	  p {   text-align: center; color: blue; }
	---    ----------- -------- ------ ------
	[선택자]   속성명       속성값  속성명  속성값
	-------------------------------------
	[선언부]

   1. CSS의 문법은 선택자와 선언부로 구성된다.
   2. 선택자는 CSS를 적용하고자 하는 HTML 요소를 가리키고
       선언부는 중괄호({})를 사용하여 전체를 둘러싼다.
   3. 각 선언은 CSS 속성명과 속성 값을 콜론(:)으로 연결한다.
   4. CSS 선언은 언제나 마지막에 세미콜론(;)으로 끝마친다.

# CSS 주석
	주석을 표시할 때에는 /* */사이에 내용을 입력한다.
	예) p {color: blue;} /*p태그의 글자 색상은 파란색입니다.*/

# CSS 선택자
	# 1. 전체 선택자
		스타일을 모든 요소에 적용할 때 사용한다.
		주로 모든 하위 요소에 한꺼번에 스타일을 적용할 때 사용하고
		전체 선택자는 asterisk(*) 기호를 사용한다.

	# 2. HTML 요소 선택자(태그 선택자)
		특정 태그가 쓰인 모든 요소에 스타일을 적용한다.
		선택자 위치에 태그명을 작성하면 사용된 모든 해당 태그에 동일한 스타일이 적용된다.

	# 3. 클래스 선택자(class 속성에 부여된 값)
		클래스 선택자는 특정 집단의 여러 요소를 한번에 선택할 때 사용한다.
		같은 클래스 이름을 가지는 요소들을 모두 선택해주고 스타일 적용 시
		선택자에 ".클래스명"을 작성해준다.

	# 4. 아이디 선택자(id 속성에 부여된 값)
		아이디 선택자는 특정 요소를 선택할 때 사용한다.
		스타일을 지정할 때 사용한다. 선택자 부분에 "#아이디명"을 작성한다.

	※ 아이디와 클래스 선택자의 차이점
		class속성 값에 여러 개의 이름을 작성할 수 있고 각 이름은 공백으로 구분한다.
		id 속성 값에는 단 한 개의 이름만 작성한다.
		class는 여러 태그에서 동일한 이름으로 묶어주는 목적이 있고, 
		id는 한 개의 태그를 특정시킬 때 즉, 중복없이 사용하는 목적이 있다.
		하지만 id도 중복으로 사용되었을 때 CSS스타일은 똑같이 적용되긴 한다.
		만약 id와 class 선택자를 동시에 적용하면, id 선택자의 스타일이 적용된다.
	
	# 5. 그룹 선택자
		여러 선택자에 같은 스타일을 적용할 경우 쉼표로 구분해서 여러 선택자를 나열한 후
		스타일은 한 번만 정의한다.

