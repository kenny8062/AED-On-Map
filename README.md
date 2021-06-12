# AED-On-Map
위급상황 발생시 쉽고 빠르게 버튼을 누르면서 다음과 같은 기능들을 해준다.
기능 1.자동으로 현재위치를 gps로 잡으며 현재위치에 위급환자가 있다고 119에 자동으로 문자가 간다.
기능 2.이 어플을 다운받고 있는 근처의 다른사람들에게 현재위치로 AED를 갖고와달라는 알림이 간다.
기능 3.AED의 근처위치를 알려주며 AED사용법을 알려준다.

나는 FCM을 이용한 gps로 근처에 있는 사람들을 판별하여 client -> client 알림을 보내는 기능을 하였다.
이때 사용자들의 위치는 firebase db를 Query문을 통하여 근처에있는 사용자들만 가져왔다.

issue -> Query문을 사용할 때 Firebase DB는 이중Query가 불가능하여 Query를 각각 실행하여 배열에 저장을 시킨 뒤 IF문으로 이중Query와 같은 필터링 방법을 사용하였다.