//정수입력받아 여러가지로 출력하기
<!DOCTYPE html>

<html>
<head>
	<meta charset="utf-8">
	<title></title>
</head>
<body>
	<h3>정수 5개 입력받아 출력하기</h3>
	<hr>
	<script type="text/javascript">
	
	var plots = [prompt("첫번째 정수 입력"),prompt("두번쨰 정수 입력"),prompt("세번쨰 정수 입력"),prompt("네번째 정수입력"),prompt("5번쨰 정수입력")]
	var re_plots=new Array();
	for (var i=0; i<plots.length; i++) {
		re_plots[i]=plots[plots.length-1-i]
	}
	var ma=plots[0]
	ma=parseInt(ma) 
	var mi=plots[0]
	mi=parseInt(mi)
	document.write("정수 5개 입력받은 순으로 출력<br>"+plots+"<hr>")
	document.write("정수 5개 입력받아 역순으로 출력<br>"+re_plots+"<hr>")
	for (var i=0;i<25;i++){
		for (j=0;j<5;j++){
			if (ma<parseInt(plots[j])) {
				ma=parseInt(plots[j])
			}
		}
	}
	for (var i=0;i<25;i++){
		for (j=0;j<5;j++){
			if (mi>parseInt(plots[j])) {
				mi=parseInt(plots[j])
			}
		}
	}
	document.write("정수 5개 입력받아 가장 높은 수 출력<br>"+ma+"<hr>")
	document.write("정수 5개 입력받아 가장 낮은 수 출력<br>"+mi+"<hr>")
	
</script>
</body>
</html>
//마우스올리면 추가 설명 출력하기
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	
	<script type="text/javascript">
		function vis(idval){
			var div1=document.getElementById=idval
			div1.style.visibility="visible"
			div1.style.top=event.clientY + "px"
			div1.style.left=event.clientX + "px"

		}
		function hid(idval){
			var div2=document.getElementById=idval
			div2.style.visibility="hidden"
		}
	</script>
	<style type="text/css">
		div {
			visibility: hidden;
			position: absolute;
			border-color: green;
			background: skyblue;
		}
	</style>
</head>
<body>
	<h3 id=h>아이템에 마우스를 올리면 설명 출력</h3>
	<hr>
	방학 도중 하고 싶은 것들
	<br>
	<ul>
		<li id=i1 onmouseover="vis(d1)" onmouseout="hid(d1)">자전거로 대한민국 일주</li>
		<li id=i2 onmouseover="vis(d2)" onmouseout="hid(d2)">책 100권 읽기</li>
		<li id=i3 onmouseover="vis(d3)" onmouseout="hid(d3)">철인 3종 경기 준비</li>
		<li id=i4 onmouseover="vis(d4)" onmouseout="hid(d4)">자바스크립트 정복</li>
	</ul>
	<div id=d1>픽시를 타고 의정부에서 한강을 지나 땅끝 마을로 간다음 다시 목포, 인천을 거쳐 달린다.</div>
	<div id=d2>소설, 만화 등 문학을 제외한 책을 하루 2권씩 읽는다.</div>
	<div id=d3>기초 체력을 먼저 단련한 후, 종목을 연습한다.</div>
	<div id=d4>교재를 복습하고, 인강을 듣는다.</div>

</body>
</html>
