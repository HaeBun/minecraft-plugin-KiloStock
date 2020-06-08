객체지향을 다루고자 나만의 방식으로 DB를 관리하는 방법을 찾아나가는 플러그인
제대로 된 DB를 배우지 않아 폴더 생성,
txt파일 생성, BufferedReader, BufferedWriter를 이용해서 내용을 불러오고 저장하는 방식으로 플러그인을 개발

-command-

/복권

/복권 즉석
/복권 즉석 구메
/복권 즉석 기록

/복권 추첨
/복권 추첨 구매
/복권 추첨 기록




- Todo -
유저가 직접 reward값을 조절할 수 있게 만들어야함.
펄미션 권한에 따라 조작 방법이 다르게 개발해야함. ( OverPower / default )
코드 최적화 매우 필요( 기능 구현을 빠르게 하기 위해 가장 큰 실수인 복사 붙여넣기를 막 갈궈넣음 )



- Algorithm -
유저가 복권을 구매하는 것부터 시작함
구매를 하면 가장 먼저 유저의 소지금액을 확인 후 복권 가격만큼 돈이 있는지 판별 ( 이상 -> 계속 진행, 미만 -> return false )
구매 기록을 저장하는 알고리즘으로 이동 - History


[ History ]
기본적으로 존재여부확인, 읽기, 쓰기, 기록 수 세기, 기록 업데이트 기능이 필요하겠다 생각하고 개발 진행

구매기록을 저장하기 전, 이 유저가 오늘 처음 구매하는 경우를 확인해야함 (기록 파일이 없으면 쓰기를 못하니)
확인해서 없으면 만들고, 있으면 넘어감
