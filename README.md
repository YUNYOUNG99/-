<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>온라인 전시</title>
    <style>
        body {
            font-family: 'Malgun Gothic', sans-serif;
            background-color: black;
            color: white;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            flex-direction: column; /* 세로 중앙 정렬을 위해 */
        }
        main {
            display: flex;
            flex-direction: column;
            align-items: center;
            max-width: 600px; /* 메인 화면 최대 너비 */
            margin: auto;
            padding: 20px;
        }
        .artwork-container {
            width: 100%; /* 작품 이미지 너비 */
            max-width: 400px; /* 작품 이미지 최대 너비 */
            margin-bottom: 30px; /* 작품 사이 간격 */
            position: relative;
        }
        .artwork-img {
            width: 100%;
            height: auto;
            cursor: pointer;
            transition: transform 0.5s ease;
        }
        .artwork-back {
            position: absolute;
            top: 0;
            left: 0;
            display: none;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 20px;
            box-sizing: border-box;
            text-align: left; /* 왼쪽 정렬 */
            z-index: 1; /* 이미지 위에 띄우기 */
            opacity: 0; /* 초기에는 숨김 */
            transition: opacity 0.3s ease;
        }
        .artwork-container.active .artwork-back {
            display: block;
            opacity: 1; /* 활성화되면 투명도 적용 */
        }
        .close-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            color: white;
            cursor: pointer;
            font-size: 1.2em;
        }
        .artwork-back img {
            max-width: 100%;
            height: auto;
            margin-bottom: 10px;
        }
        .header-content, .footer-content {
            text-align: center;
            margin-bottom: 20px;
        }
        .signature-img {
            max-width: 10mm;
            max-height: 10mm;
            cursor: pointer;
        }
        .social-buttons {
            margin-top: 20px;
            text-align: center;
        }
        .social-buttons a {
            display: block;
            margin-bottom: 10px;
            text-decoration: none;
            color: white;
            background-color: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 20px;
            transition: background-color 0.3s ease;
        }
        .social-buttons a:hover {
            background-color: rgba(255, 255, 255, 0.3);
        }
        .author-info {
            display: none;
            max-width: 100%;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            margin-top: 20px;
            box-sizing: border-box;
            text-align: left; /* 왼쪽 정렬 */
        }
        .show-author-info {
            display: block;
        }
    </style>
</head>
<body>

<main>
    <div class="header-content">
      <div class="header-content">
        <p>Lee, Yun young</p>
          <button onclick="toggleAuthorInfo()">작가소개</button>
<p>
        <div class="author-info" id="authorInfo">
     "많"은 "취"향을 가진 사람, 많취입니다.
<p>
산업디자인과를 졸업해 놓곤, 어쩌다 수제화를 배워 창업했다가, 유난히 좋아하는 외계인 캐릭터로 디지털 드로잉 작가 활동도 하고, 수제 작업물도 판매하고, 취미 미술학원 선생님을 하기도 했어요. 대학 입학부터 2024년인 지금까지 햇수로는 6년 안에 일어난 일입니다.
<p>
좋아하는 것이 너무 많아서 제대로 갈피를 못 잡고 꾸준히 다양한 예술 분야에 눈독을 들였습니다. <p>그 덕분일까요? <p>사람들은 제게 " 알록달록 오팔 같은 매력이 있다"라며 입을 모아 말합니다.
<p>
저의 모습을 닮아 알록달록하고, 넘실거리는 자연을 그린 첫 번째 공개 작품. 산수화 시리즈로 세상에 문을 두드립니다.
<p>
그림들은 결코 혼자 그려내지 않습니다. <p> 자연이 준 바람 소리와 아이들이 뛰노는 모습, 16년 친구 반려견의 눈빛과 사랑하는 사람들의 지지가 있었습니다. 이것들을 잊지 않고 보답하기 위해, 나로 인해 다른 사람도 행복해지길 바라는 마음으로 그림을 그려요.<p>
<p>
      <p>dbsdudgustjd@naver.com    이윤영<p><p>

        </div>

    </div>
<p>
<p>
<p>
<p>

    <div class="artwork-container" onclick="toggleArtworkDetail(this)">
        <img src="front1.jpg" alt="Artwork 1" class="artwork-img">
        <div class="artwork-back">
            <img src="back1.jpg" alt="Artwork 1 Back">
            <p style="text-align: left;">작품명 | 오월 야옹이의 이상향 <br> </p>(Meow's Utopia in May)<br></p>

         2024년<br> 캔버스에 유채 (Oil on canvas)<br>24*40cm<br></p>

            작품설명 | <br> </p>

이곳은 고양이들의 낙원. 너무나도 달콤해 보이는… <br>
인간 눈에는 달다 못해 이가 썩어버릴 것 같지만, 고양이들은 이곳이 적당히 아늑하니 좋다고 한다. 따뜻한 햇볕에 눈을 꼭 감고 있고, 너무 더우면 그늘 밑에서 시원함을 즐긴다. 조금만 걸어가면 흐르는 강물이 있지만, 귀찮아서 자주 가지 않는다.
<br><p>
언제나 여름일 것 같은 이곳엔 애묘가들이 올 것 같다. 사담을 덧붙이자면 정작 이걸 그린 사람은 고양이 알레르기가 있어 오래 있지 못한다는 점이다. 이곳은 밤에 달이 선명하게 뜬다. 목욕을 싫어하는 고양이들을 위해 비도 자주 오지 않는다</p>

            <span class="close-btn" onclick="toggleArtworkDetail(this.parentNode)">X</span>
        </div>
    </div>

    <div class="artwork-container" onclick="toggleArtworkDetail(this)">
        <img src="front2.jpg" alt="Artwork 2" class="artwork-img">
        <div class="artwork-back">
            <img src="back2.jpg" alt="Artwork 2 Back">
            <p style="text-align: left;">작품명 | 푸른달 가령폭포의 불청객<br> </p> (An uninvited guest of the Flower Moon, in alyeong Falls)<br></p>

 	2024년<br> 캔버스에 유채 (Oil on canvas)<br> 24*40cm
<br></p>
            작품설명 |<br> </p>

이 산수 풍경화는 동양화의 평면 기법을 곳곳에 적용하였지만, 서양 재료인 유화의 특성을 최대한 활용하여 그려졌다. 붓을 이용한 부드러운 블렌딩, OHP 필름 모서리를 활용한 날카롭고 시원한 외곽선 표현 등 이론은 적용 되지만 공식은 적용되지 않은 그림이다.
<br><p>


시원한 폭포 소리가 가득한 이곳에는 사람의 발길이 닿는 딱 여기까지만 새 소리를 들을 수 없다. 이 장소의 주인인 자연은 인간을 허락하지 않는 듯하다. 주인들은 어디에 숨은 건지 시선을 둘 데가 없이 꽉 막혀있고, 또 다른 출입문인 폭포의 시작점엔 오직 산새만이 들락날락한다.</p>

            <span class="close-btn" onclick="toggleArtworkDetail(this.parentNode)">X</span>
        </div>
    </div>

    <div class="artwork-container" onclick="toggleArtworkDetail(this)">
        <img src="front3.jpg" alt="Artwork 3" class="artwork-img">
        <div class="artwork-back">
            <img src="back3.jpg" alt="Artwork 3 Back">
 <p style="text-align: left;">작품명 | 무릉도원<br></p>(복숭아꽃이 피는 아름다운 계곡)<br></p>p style="text-align: left;">작품명 | 무릉도원<br></p>(복숭아꽃이 피는 아름다운 계곡)<br></p>


 2024 년<br> 캔버스에 유채(캔버스 위의 오일)<br> 22*22cm<br></p>

 작품설명 |<br> </p>
 배경 색상은 계산 없이 무작위로 선택하고 고민 없이 블랜딩했다. 우연이 만들어낸 패턴 위에 날씨와 장소를 적절히 조합하여 무릉도원을 그려냈다.
</p>

맨 처음 거침없이 붓질하는 과정에서 물아일체가 되며, 그림을 그리고 있는 바로 그곳이 지상낙원으로 느껴졌다. "낙원"의 정의가 한 점의 작은 그림으로 시작되어, 이렇게 한 줄 쓰인다.
</p>

"그림을 그리는 행위가 나에겐 낙원이었다." </p>


 <span class="close-btn" on click="toggleArtwork Detail(this.parentNode)">X</span>
 </div>
 </div>

 <!-- 추가된 작품 -->
 <div class="artwork-container" 클릭="toggleArtwork Detail(이것)">
 <img src="front4.jpg" alt="아트워크 4" class="artwork-img">
 <div class="artwork-back">
 <img src="back4.jpg" alt="아트워크 4 백">
 <p style="text-align: left;">작품명 | 구비구비 설원<br></p>(롤링 스노우 씬)<br></p>


 2024 년<br> 캔버스에 유채, 아크릴(오일, 화폭에 아크릴)<br>33*53cm<br></p>

 작품설명 |<br> </p>
 이번 산수화 시리즈에서 유일하게 색이 거의 없는 상당히 추상적인 그림이다.
</p>
이렇게 바라보니, 저 멀리 지나온 길은 가늘어지다 보이지 않는다.
</p>
순탄하기만 한 인생이 어디 있겠냐마는, 물길을 건너고, 산을 굽이굽이 여기까지 걸어왔다. 길이 복잡해서 이리저리 들쑤신 건지 이미 지나왔던 길을 다시 돌아가는 중 인지 우리는 알 수 없다. 그러나 한 가지 확실한 건, 획은 계속해서 그어지리라는 것.
</p>
아득히 먼 옛날을 지나 선명한 현재를 만끽하고, 알 수 없는 미래를 향해 나아간다.
</p>

     <span class="close-btn" on click="toggleArtwork Detail(this.parentNode)">X</span>
     </div>
    </div>

    <div class="footer-content">
     <img src="signature.png" alt="Signature" class="signature-img">
     <div class="social-buttons">
     <a href="https://www.instagram.com/manchwi_alien/ " target="_blank">@manch wi_ailen</a>
     <a href="https://blog.naver.com/dbsdudgustjd " target="_blank">많취의 블로그</a>
     </div>
    </div>
</메인>

<대본>
 기능 토글 아트워크 상세 (아트워크 컨테이너) {
 artworkContainer.classList.toggle('active');
 }

 기능 토글작성자 정보() {
 var authorInfo = document.getElementById('author)정보';
 authorInfo.classList.toggle('show-author-info');
 }
</스크립트>

</신체>
</html>
