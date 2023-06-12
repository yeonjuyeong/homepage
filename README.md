# homepage
### 메인
![image](https://github.com/yeonjuyeong/homepage/assets/123055714/6b07128c-a762-42f2-a908-123100474f7b)

css, js 연결
```html
<!DOCTYPE html>
<html>
<head>
<meta charset='utf-8'>
<link rel="stylesheet" href="css/style.css?=abc" type="text/css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js" defer="defer"></script>
<script src="js/script.js?=dfg" defer="defer" ></script>
</head>
```




메인 보이는 부분
```html
<body>

<div id='page'>
	<header>
		<div id='logo'>
			<img src='img/한국민속촌.svg'>//로고
			
			
			
		</div>//메뉴
		<div id='top'>
			  <ul class="main-menu">
                <li>
                    <a href="#" >민속촌 이용안내</a>
                    <ul class="sub"> 
                        <li><a href="#">민속촌위치</a></li>
                        <li><a href="#">촬영안내</a></li>
                        <li><a href="#">운영시간</a></li>
                        <li><a href="#">자주 묻는 질문</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#" >요금/예약</a>
                    <ul class="sub">
                        <li><a href="#">예약</a></li>
                        <li><a href="#">단체예약</a></li>
                        <li><a href="#">요금할인</a></li>
                        <li><a href="#">요금안내</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#" >할 수 있는 체험</a>
                    <ul class="sub">
                        <li><a href="#">한복대여</a></li>
                        <li><a href="#">공연안내</a></li>
                        <li><a href="#">체험</a></li>
                        <li><a href="#">체험Q&A</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#" >회원</a>
                    <ul class="sub">
                        <li onclick="winOpen1()"><a href="#">로그인</a></li>
                        <li onclick="winOpen2()"><a href="#">회원가입 클릭</a></li>
                    </ul>
                </li>
             </ul>
		</div>//메뉴
	</header>

	
	
	
	
<div class='clear'></div>  <!--	float 속성 해제 -->	
	
	<section>//연속적인 이미지
             <div class="imgs" >
                 <img src='img/민속촌1.jfif'>
                 <img src='img/민속촌2.jfif'>
                 <img src='img/민속촌3.jfif'>
                 <img src='img/민속촌4.jfif'>
                 <div class="welcome">
                     <h2><span>민속촌에 오신 것을 환영합니다.</span></h2>
                 </div>
             </div>
	</section>//연속적인 이미지
	
	
	
	
	
	<div class='clear'></div>  <!--	float 속성 해제 -->
    
    <div>//게시물
            <div class = "notice">
                    <h2>공지사항</h2>
                    <table class = "table">
                            <tr>
                                    <th>내용</th>
                                    <th>날짜</th>
                            </tr>
                            <tr>
                                    <td><a href = "#">민속촌의 사진 모음</a></td>
                                    <td>2022-06-01</td>
                            </tr>
                            <tr>
                                    <td><a href = "#">여름방학할인이 시작됩니다.</a></td>
                                    <td>2022-08-01</td>
                            </tr>
                            <tr>
                                    <td><a href = "#">단풍사진이벤트!</a></td>
                                    <td>2022-10-01</td>
                            </tr>
                            <tr>
                                    <td><a href = "#">공사 안내</a></td>
                                    <td>2022-11-01</td>
                            </tr>
                            <tr>
                                    <td><a href = "#">눈송이 이벤트!</a></td>
                                    <td>2022-12-20</td>
                            </tr>
                    </table>
            </div>//게시물
	    
	    
	    
	    
        <div class=clear></div>
        <footer>//위치
        <div id=address align="center">
        	<img src="img/민속촌 위치.png">
        </div>
        
        </footer>//위치
    </div>
</div>
</body>
</html>
```







로그인 버튼을 누구면 로그인 화면이 뜨고
![image](https://github.com/yeonjuyeong/homepage/assets/123055714/18cef82c-ecdd-40b1-a78e-3a8fe8f4c100)

회원 가입 버튼을 누르면 회원관리 화면이 뜬다
![image](https://github.com/yeonjuyeong/homepage/assets/123055714/0a19ed0e-b624-45d7-bd50-dfc48e35b813)


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>

        body {
            font-size: 14px;
            font-family: 돋움;
        }

        table {
            width: 800px;
            margin: 0 auto;
        }

        table, tr, th, td {
            border: 1px solid #333;
            border-spacing: 0;
        }

        strong { color: red; }

        caption {
            text-align: right;
        }

        th, td {
            padding: 10px 15px;
        }

        span { color: red;}

        th {text-align: right;}

        #btn {float:right;}

    </style>
</head>

<body>
    <form action="join.jsp" method="post" name="form">
        <table>
            <caption>(*)표시는 <strong>필수입력</strong> 사항입니다.</caption>
            <tr>
                <th><span>*</span>회원유형</th>
                <td>학생</td>
            </tr>
            <tr>
                <th><span>*</span>이름(실명)</th>
                <td>홍길동</td>
            </tr>
            <tr>
                <th><span>*</span>아이디</th>
                <td><p><input type="text" size="20" maxlength="15"></p>
                    <p>6~15자의 영문소문자, 숫자만 가능합니다.</p>
                </td>
            </tr>
            <tr>
                <th><span>*</span>비밀번호</th>
                <td><p><input type="password" size="20"></p>
                    <p>비밀번호는 <strong>영대문자, 영소문자, 숫자, 특수문자의 조합</strong>으로 이루어져야합니다.<br>
                        - 조합이 2종류 이상인 경우 10자리 이상,<br>
                        - 조합이 3종류 이상인 경우 8자리 이상 가능합니다.
                    </p>
                </td>
            </tr>
            <tr>
                <th><span>*</span>비밀번호 확인</th>
                <td><p><input type="password" size="20"></p></td>
            </tr>    
            <tr>
                <td colspan="2"><p>학교 홈페이지에 가입하시겠습니까?
<span id="btn"><input type="submit" value="확인"> <input type="reset" value="취소"></span></p>
                </td>
            </tr>
        </table>
    </form>
</body>
</html>
```
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>로그인페이지</title>
</head>
<body>
    <form> 
        <p>ID : <input type = "text" size="20"> </p>
        <p> Password : <input type = "password" size="30"></p>
        <p> <input type="submit" value="확인"> <input type="reset" value="취소"></p>
    </form>
    
</body>
</html>
```
