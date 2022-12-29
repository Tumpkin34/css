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

# 캐스케이딩(Cascading)
	하나의 요소는 하나 이상의 CSS선언에 영향을 받을 수 있다.
	이 때 충돌을 피하기 위해서 CSS 적용 우선순위가 필요하다.
	
# 1. 중요도 : CSS가 어디에 선언되었는 지에 따라서 우선순위가 달라진다.
	(1) 인라인 스타일(HTML 요소 내부에 style 속성으로 사용)
	(2) 내부 스타일 시트(HTML 문서의style태그 안에 위치)
	(3) 외부 스타일 시트(CSS 파일을 외부에 따로 만들어서 불러오는 방법)
	(4) 웹 브라우저 기본 스타일
		
	우선 순위는 (1) > (2) > (3) > (4) 순이다.
	인라인 스타일의 우선순위가 가장 높다.

# 2. 명시도 : 명혹하게 특정할수록 우선순위가 높아진다.
	!important > 인라인 스타일 > 아디 선택자 > 클래스 선택자  > 태그 선택자 > 전체 선택자 > 상속받은 속성
		
	!important를 이길 수 있는 스타일은 없다. 하지만 중요도에 따라서 같은 important일 지라도 우선순위가 달라질 수 있다.

# 3. 선언순서 : 나중에 선언된 스타일이 우선 적용된다.
  	여러개의 클래스 명을 사용하는 경우에도 나중에(아래에) 선언된 스타일이 우선 적용된다.
	 
# 시맨틱 태그
	시맨틱 : "의미가 있는"
	HTML5에 도입된 시맨틱 태그는 개발자와 브라우저에게 의미있는 태그를 제공한다.

# ▶ 태그의 종류
	<div> : non-semantic태그, 안에 들어갈 의미를 크게 유추하기 힘들다.
	<header>, <footer> : semantic태그, 특정 형태의 글이 포함될 것이라는 유추가 가능하다.

	-header : 상단, 헤더를 의미
	-nav : 메뉴, 내비게이션을 의미
	-main : 내용의 중심을 의미
	-aside : 사이드에 위치하는 공간을 의미
	-section : 여러 중심 내용을 감싸는 공간을 의미
	-article : 글자가 많이 들어간 부분을 의미
	-footer : 하단, 푸터를 의

# ▷ <header> 태그
	1. 머리말 지정
	2. 사이트 전체의 헤더는 주로 페이지 맨 위쪽이나 왼쪽에 삽입하며, 헤더의 내용으로는 주로 <form>태그를 사용해 검색 창을 넣거나 
	<nav> 태그를 연동하여 사이트 메뉴를 넣는다.

# ▷ <nav> 태그
	1. 문서를 연결하는 내비게이션 링크
	2. 내비게이션 역할을 하는 <nav>태그는 동일한 사이트 안의 문서나 다른 사이트의 문서로 연결하는 링크 모음을 나타낸다.
	3. <nav> 태그는 내비게이션 메뉴 뿐 아니라 <header>, <footer> 태그 안에 있는 링크 부분에도 많이 사용된다.

# ▷ <section> 태그
	1. 주제별 컨텐츠 영역 나타내기
	2. <section> 태그는 문맥 흐름 중에서 컨텐츠를 주제로 묶을 때 사용하며 그 안에는 섹션 제목을 나타내는 <h1> ~ <h6> 제목 태그가 함께 사용된다.


# ▷ <aside> 태그
	1. 본문 이외의 내용 표시
	2. 블로그에서 왼쪽이나 오른족 하단에 사이드 바가 표시된 형태이다.
	3. 필수 요소가 아니므로 광고나 링크 모음 등 문서의 메인 내용에 영향을 미치지 않는 내용을 넣을 때 사용한다.

# ▷ <footer> 태그
	1. 제작 정보와 저작권 정보 표시
	2. 웹 문서 끝자락에 들어가는 태그
	3. <footer> 태그 안에는 <section>, <article> 등 다른 레이아웃 태그들을 모두 사용할 수 있으며, 이런 태그를 이용해서 <footer> 안에 다양한 정보를 넣는다.

# ★ 검색 엔진과 시맨틱 태그와의 관련성
	검색 엔진 최적화에서 시맨틱 태그는 매우 중요한 요소이다.
	그렇기 때문에 검색결과에 많은 노출을 시키고 싶다면 시맨틱 태그를 필수로 사용하는 것이 좋다.



















