#자바 스크립트 공부하기 첫걸음#

-------로컬 스토리지란?---------
<h2>데이터를 사용자 로컬에 보존하는 방식<h2>
<h2>자바 스크립트로 조작</h2>
<p>웹 스토리지의 한 부분으로 </br>세션 스토리지와 구분되는 점은 영구적으로 이용가능함, </br>필요할 때 언제든지 이용가능함 </p>

------로컬 스토리지 활용 ---------

<p>localStorage.setItem("이름", 저장할 값);  // 스토리지에 데이터 쓰기</p>


<p>localStorage.getItem("이름");  // 스토리지로 부터 데이터 읽기</p>


<p>localStorage.removeItem("이름");  // 스토리지의 데이터 삭제</p>


<p>localStorage.clear();  // 모든 스토리지의 데이터 삭제</p>


<p>localStorage.length;  // 저장된 키/값 쌍의 개수</p>

<h4>객체배열 저장</h4>
<p> objArr = [{num:1, title:'name', contents:'abcde'}, ...] </p>


-------------스토리지 이해했는지 테스트 ---------------------
<!DOCTYPE html>
<html>
    <head>
        <title>Test</title>
</head>
<body>
    <div id = "first">
        <input id = "id" type="text" placeholder="id">
    </div>
    <div id = "second">
        <input id = "password" type="text" placeholder="Password">
    </div>

    <form class= "inbutton">
        <input type = "submit" value = "로그인">
    </form>
    <script src="js-login.js"></script>

</body>
</html>
---------------- js-login.js -----------------------------

<p>const input = document.querySelector ("#first");  //id의 input 영역 </p>
<p>const input_One = input.querySelector("input");</p>
<p>const password1 = document.querySelector("#second");</p>
<p>const password_One = password1.querySelector("input"); //password의 input 영역</p>
<p>const form = document.querySelector(".inbutton"); // 버튼 영역</p> 
<p>console.log(input_One);</p>

<p>function handlesubmitId(event){  //함수로 묶음 </p> 
    <p>console.log("Start-HandleSubmitId");</p>
    <p>let currentId = input_One.value;  // currentdld, currentPassword 라는 변수에 각각 input_One(id의 입력값), </p>
   <p> let currentPassword = password_One.value; // Password_One(pw의 입력값)의 입력값을 넣음</p>
   <p> localStorage.setItem(currentId,currentPassword);</p>
}


<p>function init(){ //버튼이 눌릴때 함수 작동하기</p>
    <p>form.addEventListener("click",handlesubmitId);</p>
    <p>console.log("1");</p>
}

init();

//결과 : 스토리지 저장 완료!///
<p>------------------------ 응용해서 로그인 및 회원가입 간단하게 구현해보기  -----------</p>
<!DOCTYPE html>
<html>
<head>
<title>Real Test</title>
</head>

<body>
    <div class ="texts">
        <div class = "login">
            <h2>로그인</h2>
            <div id = "login1">
                <input id = "loginId" type ="text" placeholder="id">
            </div>
            <div id = "login2">
                <input id= "loginPassword" type = "text" placeholder = "Password">
            </div>

            <form class = "loginbutton loginbtn">
                <input id = "loginbtn" type = "submit" value = "로그인">
            </form>
        
        </div>
        <div class = "join">
                <h2>회원가입 연습</h2>
                <div id = "first">
                    <input id = "id" type = "text" placeholder="id">
                </div>
                <div id = "second">
                    <input id = "password" type = "text" placeholder="Password">  
                </div>    
            </div>
             
            <form class = "joinbutton inbtn">
                <input id = "inbtn" type = "join" value = "회원가입">
             </form>
        </div>
    </div>
    <script src ="js-join.js"></script>
    <script src ="js-login.js"></script>
</body>
</html>
--------------------- js-join.js ----------------------------

<p>const check_1 = document.querySelector("#login1");  //querySelector로부터 로그인 입력칸 & 로그인 버튼을 가져옴</p>
<p>const check_id = check_1.querySelector("input");</p>
<p>const check_2 = document.querySelector("#login2");</p>
<p>const check_password = check_2.querySelector("input");</p>
<p>const loginBtn = document.querySelector(".loginbutton");</p>

<p>function CheckValue(){ //하나의 함수로 묶음</p>
    <p>const ID = check_id.value; // ID에 입력칸 값 저장</p>
   <p>const PASSWORD = check_password.value; // PW에 입력한 값 저장</p>
    <p>if(localStorage.getItem(ID) == PASSWORD) {</p>
        <p>alert("로그인 되었습니다.");            //회원가입한 아이디와 비밀번호가 입력되었으면 출력</p>
   <p> }else{</p>
        <p>alert("등록되지 않거나 아이디,비밀번호 오류입니다!"); //회원가입한 아이디나 비밀번호가 둘중하나라도 오류이면 출력</p>
   <p> }</p>
<p>}</p>

<p>function init(){</p>
    <p>loginBtn.addEventListener("click",CheckValue);</p>
<p>}


init();

// 결과 회원가입 O 로그인 O





<h2>자바스크립트의 다양한 식 나타내기</h2>



    <p>inch * 2.54</p> // 연산식은 식입니다.
    <p>"안녕하세요?"; // 문자열도 식입니다.
    <p>5</p> // 숫자도 식입니다.





<h2>알림 창 만들기</h2>



<p>alert("안녕하세요?")</p>





<h3>확인 창 만들기</h3>



<p> var reply = confirm("정말 배경 이미지를 바꾸시겠습니까?");





<h4>프롬포트 창의 기본값 지정하기</h4>



<p>var name = prompt("이름을 입력하세요."아무개");</p>





<h4>이름 받아서 화면에 표시하기</h4>



 <script>
     var name = prompt("이름을 입력하세요.");
     document.write("<b><big>"+"name"+"</big></b>님, 환영합니다.");
 </script>



<h3>배열 나열하기</h3>

<p>var spring = "봄";</p>
<p>var summer = "여름";</p>
<p>var fall = "가을";</p>
<p>var winter = "겨울"</p>



<p>var season = ["봄","여름","가을","겨울"];</p>





<h2>블록 변수 선언하기</h2>



function calcSum(n) {

​	let sum = 0;

​	for(let i = 1; i < n + 1; i++ ){

​	sum += i;

​	}

​	console.log(sum);

}



<h2>매개변수를 사용한 함수 선언하고 호출하기</h2>

function addNumber(num1,num2) {

​	var sum =  num1+num2; 

​	return sum;

}

var result = addNumber(2,3);

document.write("두 수를 더한 값: "+ result);



<h3>버튼을 클릭하면 배경 색 바꾸기</h3>

<body>

	<ul>
	    <li><a href="#"onclick = " changeBg('green')">Green</a></li>
	    <li><a href="#"onclick = " changeBg('orange')">Green</a></li>
	    <li><a href="#"onclick = "changeBg('purple')"</li>
	</ul>
	<div id = 'result'></div>
	
	<script>
	fucntion changrBg(color) {
		var result = document.querySelector('#result');
		result.style.backgroundColor = color;
	}
	</script>
	</body>
	
<h3>도대체 DOM이란 무엇인가?</h3>

<p>Document Object Model의 약자, 문서객체모델,,</p>
<p>문서 객체란? <html>이나 <body> 같은 html문서의 태그들을 JavaScript가 이용할 수 있는 객체(object)로 만들면 그것을 문서 객체라고 한다. </p>
<p>(그럼 html문서의 태그들이 객체에 담긴 상태를 의미하는 것일까?) </p>
<p>여기에 Model을 붙였는데 Model이라는 영어 단어에는 모형, 주형이라는 의미도 있고 모듈이라는 의미도 있다고 한다. </p>
<p>비슷하게 여기서는 문서 객체를 '인식하는 방식'이라고 해석할 수 있다.</p>
	<p>DOM은 넓은 의미로 웹 브라우저가 HTML 페이지를 인식하는 방식을 의미한다.</p>
	<p>조금 좁은 의미로 본다면 document 객체와 관련된 객체의 집합을 의미할 수도 있다. </p>
 	<p>DOM의 구조는 자료구조중 트리에 해당</P>
	
<h3>다양한 방법으로 DOM 요소에 접근하기</h3>
	<p>document.getElementById("heading")  //id값이 heading인 요소에 접근</p>
	<p>document.getElementByClassName("클래스 명") // class 선택자 이름이 들어있는 DOM요소에 접근</p>
	
	querySelector("#heading") //id="heading"인 요소
	querySelector(".bright") //class = "bright"인 요소
	
	



