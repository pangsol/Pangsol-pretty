# Pangsol-pretty
<!DOCTYPE HTML>
<html lang="ko">
<머리>
<meta charset=>UTF-8" />
<title>말랑노트 익명게시판+채팅+투표</title>
<스타일>
 본문 {폰트 패밀리}: Arial, 산세리프; 최대 너비: 600px; 여백: 20px auto; }
 h2 { 테두리 하단: 2 px 솔리드 #f49ac2; 패딩 하단: 5 px; 색상: #d65a8d; }
 텍스트 영역 {폭: 100%; 높이: 60 px; }
 입력[type=text] {폭: 80%; }
 버튼 { 여백 상단: 8 px; 패딩: 6 px 12 px; 배경: #f49ac2; 테두리: none; 색상: #ffff; 커서: pointer; }}
 버튼: hover {background:#d65a8d; }
 .post, .chammsg {경계 하단: 1 px 솔리드 #cc; 패딩: 6 px 0; }
 #채팅로그 {경계: 1px 솔리드 #ccc; 높이: 150px; 오버플로우-y: 자동; 패딩: 8px; 여백 하단: 10px; }
 #결과 ul {패딩-왼쪽: 20 px; }
 레이블 { 커서:pointer;}
 섹션 { 여백 하단: 30 px; }
</스타일>
</머리>
<바디>

<섹션>
 <h2>익명게시판</h2>
 <textarea id="content" 자리 표시자="여기에 글을 써주세요"></textarea><br />
 <버튼 클릭="addPost()">글 올리기</버튼>
 <div id="posts"></div>
</섹션>

<섹션>
 <h2>간단 채팅방</h2>
 <div id="chatLog"></div>
 <입력 유형="text" id="chatInput" 플레이스홀더="메시지를 입력하세요" />
 <버튼 클릭="메시지 보내기()">전송</버튼>
</섹션>

<섹션>
 <h2>간단 투표</h2>
 <p>좋아하는 과일을 골라주세요:</p>
 <label><입력 유형="라디오" 이름="과일" 값="사과" /> 사과</label><br />
 <label><입력 유형="라디오" 이름="과일" 값="바나나" /> 바나나</label><br />
 <label><입력 유형="라디오" 이름="과일" 값="포도" /> 포도</label><br />
 <버튼 클릭="vote()">투표하기</버튼>
 <div id="result"></div>
</섹션>

<스크립트>
 // 익명게시판
 const postsDiv = document.getElementById('posts');
 함수 addPost()
