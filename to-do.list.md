메인 메뉴

---  미 로그인시 게시판 이동불가 //   로그인 후 이용하세요 alert 출력 OO

- 로그인 누르면 로그인 폼   O

- 회원가입 누르면 회원가입 폼   O
   -> 완료시 메인 화면으로 롤백

- 여기서 로그인 누르고 로그인시  O 
  --> 000님 환영합니다 문구 띄우기    /// 세션 다지워지는  오류  막기  해결 O

------------------------------------------------------------------------------
게시판 쪽

글 작성시 로그인한 guest ID , 작성자 명에 출력  OO

게시글 리스트에 글 작성자 명에 출력 △  <<맨위 리스트 1개에만 이름이 나오는 오류 >>

게시글 누르면 등록한 글에도 ID 출력 / 해결 OO

last, 글 수정시 글을 작성한 사람만 수정 가능 

--->

※※※※수정 버튼에 함수를 넣자※※※※

  if (작성자 != UserName) {
    alert ('수정 권한이 없습니다') 
  }else (modify.html)

but how????





-------------------------------------------------------

/*css*/

1. 글 쓰기 폼 적용    O 
2. 게시글 리스트 폼 적용 O
3. 메인페이지 적용 O
4. 게시글 확인 페이지 적용  O
5. 로그인 폼 적용 O
6. 회원가입 폼 적용  O
