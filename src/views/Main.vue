<template>
  <div class="ms">
    <header class="mw1440">
      <div class="logo-box">
        <a href="">
          <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE1Mu3b?ver=5c31" alt="" style="height: 100%;">
        </a>
      </div>
      <nav class="fs12">
        <ul style="display: flex;">
          <li><a href="">Office</a></li>
          <li><a href="">Windows</a></li>
          <li><a href="">Surface</a></li>
          <li><a href="">Xbox</a></li>
          <li><a href="">지원</a></li>
        </ul>
      </nav>
      <button class="xi-bars mobile-nav-btn" @click="openMobileNav()"></button>
      <div class="side-box fs12">
        <button id="msAll" @click="showMsDropdownMenu">
          <p>Microsoft 전체</p>
          <span class="xi-angle-down"></span>
        </button>
        <button class="search" @click="showSearchForm"> 
          <p class="search-text mobile-hide">검색</p>
          <span class="xi-search"></span>
        </button>  
        <a href="" class="cart">
          <p class="mobile-hide">카트</p>
          <span class="xi-cart-o"></span>
        </a>
        <a href="" class="login">
          <span class="mobile-hide">로그인</span>
          <i class="xi-profile-o"></i>
        </a>
      </div>
      <div class="fs12" id="msAll-dropdown-menu" style="max-height: 0;">
        <div class="dropdown-top">
          <ul>
            <li style="font-weight: bold;">소프트웨어</li>
            <li><a href="">Windows용 앱</a></li>
            <li><a href="">OneDrive</a></li>
            <li><a href="">Outlook</a></li>
            <li><a href="">Skype</a></li>
            <li><a href="">OneNote</a></li>
          </ul>
          <ul>
            <li style="font-weight: bold;">PC 및 장치</li>
            <li><a href="">PCs &amp; tablets</a></li>
            <li><a href="">주변 기기</a></li>
          </ul>
          <ul>
            <li style="font-weight: bold;">엔터테인먼트</li>
            <li><a href="">Xbox 및 게임</a></li>
            <li><a href="">게임</a></li>
            <li><a href="">Windows 게임</a></li>
          </ul>
          <ul>
            <li style="font-weight: bold;">기업 고객용</li>
            <li><a href="">Microsoft Azure</a></li>
            <li><a href="">Microsoft Dynamics 365</a></li>
            <li><a href="">Microsoft 365</a></li>
            <li><a href="">Microsoft Industry</a></li>
            <li><a href="">데이터 플랫폼</a></li>
            <li><a href="">불륨 라이선싱</a></li>
          </ul>
          <ul>
            <li style="font-weight: bold;">Developer &amp; IT</li>
            <li><a href="">.NET</a></li>
            <li><a href="">Visual Studio</a></li>
            <li><a href="">Windows Server</a></li>
            <li><a href="">Windows 앱 개발</a></li>
            <li><a href="">문서</a></li>
          </ul>
          <ul>
            <li style="font-weight: bold;">기타</li>
            <li><a href="">Microsoft Store</a></li>
            <li><a href="">무료 다운로드 및 보안</a></li>
            <li><a href="">교육</a></li>
          </ul>
        </div>

        <div class="dropdown-bottom">
          <a href="">
            <span>사이트맵 보기</span>
            <i class="xi-angle-right"></i>
          </a>
        </div>
      </div>
      <form action="" id="search-form">
        <button class="xi-arrow-left back" @click="closeSearchForm"></button>
        <div class="input-box">
          <input type="search" placeholder="Microsoft.com 검색">
          <button class="xi-search" type="button"></button>
        </div>
        <button class="cancel fs12" type="button" @click="closeSearchForm">취소</button>
      </form>

      <div id="mobile-nav-container" class="fs14">
        <button class="xi-close close-btn" @click="closeMobileNav()"></button>
        <a href="">Microsoft 365</a>
        <a href="">Office</a>
        <a href="">Windows</a>
        <a href="">Surface</a>
        <a href="">Xbox</a>
        <a href="">지원</a>
        <div class="btn-box">
          <button href="" @click="openMobileSw()">
            <p>소프트웨어</p>
            <p class="xi-angle-down" id="swI"></p>
          </button>
          <div class="dropdown-box" id="swDdBox">
            <a href="">Windows 앱</a>
            <a href="">OneDrive</a>
            <a href="">Outlook</a>
            <a href="">Skype</a>
            <a href="">OneNote</a>
            <a href="">Microsoft Teams</a>
          </div>
        </div>

        <div class="btn-box">
          <button @click="openMobilePcDevice()">
            <p>PC 및 장치</p>
            <p class="xi-angle-down" id="pdI"></p>
          </button>
          <div class="dropdown-box" id="pdDdBox">
            <a href="">XBox 쇼핑</a>
            <a href="">PCs &amp; tablets</a>
            <a href="">주변 기기</a>
          </div>
        </div>

        <div class="btn-box">
          <button @click="openMobileEt()">
            <p>엔터테인먼트</p>
            <p class="xi-angle-down" id="etI"></p>
          </button>
          <div class="dropdown-box" id="etDdBox">
            <a href="">Xbox Game Pass Ultimate</a>
            <a href="">Xbox Live GOld</a>
            <a href="">Xbox 및 게임</a>
            <a href="">PC 게임</a>
            <a href="">Windows 게임</a>
          </div>
        </div>

        <div class="btn-box">
          <button @click="openMobileEc()">
            <p>기업 고객용</p>
            <p class="xi-angle-down" id="ecI"></p>
          </button>
          <div class="dropdown-box" id="ecDdBox">
            <a href="">Microsoft Azure</a>
            <a href="">Microsoft Dynamics 365</a>
            <a href="">Microsoft 365</a>
            <a href="">Microsoft Industry</a>
            <a href="">데이터 플랫폼</a>
            <a href="">볼륨 라이선싱</a>
            <a href="">비즈니스 쇼핑</a>
          </div>
        </div>

        <div class="btn-box">
          <button @click="openMobileDi()">
            <p>Developer &amp; IT</p>
            <p class="xi-angle-down" id="diI"></p>
          </button>
          <div class="dropdown-box" id="diDdBox">
            <a href="">.NET</a>
            <a href="">Visual Studio</a>
            <a href="">Windows Server</a>
            <a href="">Windows 앱 개발</a>
            <a href="">문서</a>
          </div>
        </div>

        <div class="btn-box" @click="openMobileOther()">
          <button>
            <p>기타</p>
            <p class="xi-angle-down" id="otherI"></p>
          </button>
          <div class="dropdown-box" id="otherDdBox">
            <a href="">무료 다운로드 및 보안</a>
            <a href="">교육</a>
          </div>
        </div>
        <a href="">사이트맵 보기</a>
      </div>
    </header>

    <main>
      <div class="introduce mw1440">
        <div class="intro intro1">
          <a href="">
            <div class="img-bg img-bg1"></div>
            <div class="img-text-box">
              <h1 class="head" style="color: #fff;">새로운 Surface Laptop 3</h1>
              <p class="fs16" style="color: #fff;">완벽한 일상용 노트북이 이제 더욱 빨라졌습니다.</p>
              <a href="" class="aBtn-white">
                <span class="detail">자세히 보기</span>
                <span class="xi-angle-right"></span>
              </a>
            </div>
          </a>
        </div>

        <div class="intro intro2">
          <a href="">
            <div class="img-bg img-bg2"></div>
            <div class="img-text-box">
              <h1 class="head">새로운 Surface Pro 7</h1>
              <p class="fs16">초경량의 다재다능함</p>
              <a href="" class="aBtn-black">
                <span class="detail">자세히 보기</span>
                <span class="xi-angle-right"></span>
              </a>
            </div>
          </a>
        </div>

        <button class="xi-angle-left prev" @click="plusSlides(-1)"></button>
        <button class="xi-angle-right next" @click="plusSlides(1)"></button>

        <!-- <div class="control-box"></div> -->
      </div>

      <div class="card-text mw1440">
        <a href="" class="box">
          <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RWfbJT?ver=8259&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;aim=true" alt="">
          <p class="title">Surface Book 2</p>
          <p class="text">최상의 노트북에서 경험하는 최고의 성능.</p>
          <a href="">
            <span>지금 쇼핑하기</span>
            <i class="xi-angle-right"></i>
          </a>
        </a>
        <a href="" class="box">
          <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE37GsN?ver=07d4&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;aim=true" alt="">
          <p class="title">여러분을 위한 365</p>
          <p class="text">날마다 Office 365로 할 수 있는 일들을 찾아보세요.</p>
          <div class="a-box">
            <a href="">
              <span>최대 6명 사용 가능</span>
              <i class="xi-angle-right"></i>
            </a>
            <a href="">
              <span>1명 사용 가능</span>
              <i class="xi-angle-right"></i>
            </a>
          </div>
        </a>
        <a href="" class="box">
          <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE37bh1?ver=33cd&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;aim=true" alt="">
          <p class="title">Xbox Game Pass Ultimate</p>
          <p class="text">Xbox Live Gold와 100개 이상의 고품질 콘솔 및 PC 게임. 친구들과 함께 플레이하고 다음에 즐길 게임을 찾아보세요.</p>
          <a href="">
            <span>지금 구입</span>
            <i class="xi-angle-right"></i>
          </a>
        </a>
        <a href="" class="box">
          <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE1uWfh?ver=0868&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;aim=true" alt="">
          <p class="title">SXbox One S</p>
          <p class="text">최고의 게임 시스템이자 4K 엔터테인먼트 시스템.</p>
          <a href="">
            <span>자세히 보기</span>
            <i class="xi-angle-right"></i>
          </a>
        </a>
      </div>

      <div class="store mw1440">
        <a href="">
          <div class="img-bg"></div>
          <div class="img-text-box">
            <h1 class="head">Microsoft 스토어</h1>
            <p class="fs16">집과 학교, 직장 및 여가 생활에 필요한 제품을 확인하세요.</p>
            <a href="" class="aBtn-white">
              <span class="detail">구매하기</span>
              <span class="xi-angle-right"></span>
            </a>
          </div>
        </a>
      </div>

      <div class="work-card-text mw1440">
        <h1>기업 사용자</h1>
        <div class="group">
          <a href="" class="box">
            <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE1CmIw?ver=e555&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;aim=true" alt="">
            <p class="title">Surface Book 2</p>
            <p class="text">최상의 노트북에서 경험하는 최고의 성능.</p>
            <a href="">
              <span>지금 쇼핑하기</span>
              <i class="xi-angle-right"></i>
            </a>
          </a>
          <a href="" class="box">
            <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE2mheW?ver=527a&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;x=444&amp;y=171&amp;aim=true" alt="">
            <p class="title">여러분을 위한 365</p>
            <p class="text">날마다 Office 365로 할 수 있는 일들을 찾아보세요.</p>
            <a href="">
              <span>1명 사용 가능</span>
              <i class="xi-angle-right"></i>
            </a>
          </a>
          <a href="" class="box">
            <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE4561D?ver=b6fc&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;aim=true" alt="">
            <p class="title">Xbox Game Pass Ultimate</p>
            <p class="text">Xbox Live Gold와 100개 이상의 고품질 콘솔 및 PC 게임. 친구들과 함께 플레이하고 다음에 즐길 게임을 찾아보세요.</p>
            <a href="">
              <span>지금 구입</span>
              <i class="xi-angle-right"></i>
            </a>
          </a>
          <a href="" class="box">
            <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE2OfW4?ver=3149&amp;q=90&amp;m=6&amp;h=201&amp;w=358&amp;b=%23FFFFFFFF&amp;l=f&amp;o=t&amp;aim=true" alt="">
            <p class="title">SXbox One S</p>
            <p class="text">최고의 게임 시스템이자 4K 엔터테인먼트 시스템.</p>
            <a href="">
              <span>자세히 보기</span>
              <i class="xi-angle-right"></i>
            </a>
          </a>
        </div>
      </div>

      <div class="follow mw1440">
        <p>Microsoft 팔로우</p>
        <a href="">
          <img src="//www.microsoft.com/onerfstatics/marketingsites-eus-prod/_h/85288795/coreui.statics/images/social/facebook.png" alt="Facebook">
        </a>
        <a href="">
          <img src="//www.microsoft.com/onerfstatics/marketingsites-eus-prod/_h/93690392/coreui.statics/images/social/twitter.png" alt="Twitter">
        </a>
      </div>
    </main>

    <footer>
      <div class="f-container mw1440">
        <div class="footer-top">
          <div class="footer-menu-box">
            <p class="text">새로운 기능</p>
            <ul>
              <li><a href="">Surface Pro X</a></li>
              <li><a href="">Surface Pro 7</a></li>
              <li><a href="">Surface Laptop 3</a></li>
              <li><a href="">Surface Go</a></li>
              <li><a href="">Windows 10 앱(238K)</a></li>
              <li><a href="">Office 앱</a></li>
            </ul>
          </div>
          <div class="footer-menu-box">
            <p class="text">Microsoft Store</p>
            <ul>
              <li><a href="">계정 프로필</a></li>
              <li><a href="">다운로드 센터</a></li>
              <li><a href="">Microsoft Store 지원</a></li>
              <li><a href="">반품/환불</a></li>
              <li><a href="">주문 추적</a></li>
            </ul>
          </div>
          <div class="footer-menu-box">
            <p class="text">교육</p>
            <ul>
              <li><a href="">교육 분야의 Microsoft</a></li>
              <li><a href="">학생용 Office</a></li>
              <li><a href="">학교용 Office 365</a></li>
              <li><a href="">학생 및 학부모용 특가 혜택</a></li>
              <li><a href="">교육 분야의 Microsoft Azure</a></li>
            </ul>
          </div>
          <div class="footer-menu-box">
            <p class="text">대기업</p>
            <ul>
              <li><a href="">Azure</a></li>
              <li><a href="">AppSource</a></li>
              <li><a href="">자동차</a></li>
              <li><a href="">정부 기관</a></li>
              <li><a href="">의료 서비스</a></li>
              <li><a href="">제조업</a></li>
              <li><a href="">금융 서비스</a></li>
              <li><a href="">소매</a></li>
            </ul>
          </div>
          <div class="footer-menu-box">
            <p class="text">개발자</p>
            <ul>
              <li><a href="">Microsoft Visual Studio</a></li>
              <li><a href="">Windows 개발자 센터</a></li>
              <li><a href="">개발자 네트워트</a></li>
              <li><a href="">TechNet</a></li>
              <li><a href="">Microsoft 개발자 프로그램</a></li>
              <li><a href="">채널 9</a></li>
            </ul>
          </div>
          <div class="footer-menu-box">
            <p class="text">회사</p>
            <ul>
              <li><a href="">채용 정보</a></li>
              <li><a href="">Microsoft 정보</a></li>
              <li><a href="">회사 뉴스</a></li>
              <li><a href="">Microsoft 개인 정보 보호</a></li>
              <li><a href="">투자자</a></li>
              <li><a href="">보안</a></li>
            </ul>
          </div>
        </div>
        <div class="footer-bottom">
          <div class="language">
            <a href="">
              <img src="../assets/earth.png" alt="">
              <span>한국어(대한민국)</span>
            </a>
          </div>
          <div class="footer-bottom-nav">
            <a href="">Microsoft에 문의</a>
            <a href="">개인정보처리방침</a>
            <a href="">사용약관</a>
            <a href="">상표</a>
            <a href="">광고정보</a>
            <span>© Microsoft 2019</span>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data: () => ({
    slideIndex: 1,
    timer: null
  }),
  created(){
  },
  mounted() {
    this.showSlides();
    this.timer = setInterval(this.executeTimer, 6000);
  },
  methods: {
    showSlides() {
      var slides = document.getElementsByClassName("intro");
      for (var i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      if (this.slideIndex > slides.length) {this.slideIndex = 1 }
      if (this.slideIndex < 1) {this.slideIndex = slides.length}
      slides[this.slideIndex-1].style.display = "block";
    },
    executeTimer() {
      this.slideIndex++;
      this.showSlides()
    },
    plusSlides() {
      clearInterval(this.timer);
      this.timer = setInterval(this.executeTimer, 6000);
      this.slideIndex++;
      this.showSlides()
    },
    showMsDropdownMenu() {
      var msAll = document.getElementById("msAll")
      var dd = document.getElementById("msAll-dropdown-menu")
      if (dd.style.maxHeight == "0px") {
        dd.style.maxHeight = "400px";
        msAll.classList.add('clicked')
      } else {
        dd.style.maxHeight = "0"
        msAll.classList.remove('clicked')
      }
      window.addEventListener('resize', function() {
        if(window.innerWidth < 861){
          dd.style.maxHeight = "0"
        } else{
          dd.style.maxHeight = "400px";
        }
      }, true);
    },
    showSearchForm() {
      document.getElementById("search-form").style.display = "block";
    },
    closeSearchForm() {
      document.getElementById("search-form").style.display = "none";
    },
    openMobileNav() {
      document.getElementById("mobile-nav-container").style.display = "block"
    },
    closeMobileNav() {
      document.getElementById("mobile-nav-container").style.display = "none"
    },

    openMobileSw() {
      if(document.getElementById("swDdBox").style.display == "block") {
        document.getElementById("swDdBox").style.display = "none"
        document.getElementById("swI").style.transform = "rotate(0)"
      } else {
        document.getElementById("swDdBox").style.display = "block"
        document.getElementById("swI").style.transform = "rotate(180deg)"
      }
    },
    openMobilePcDevice() {
      if(document.getElementById("pdDdBox").style.display == "block") {
        document.getElementById("pdDdBox").style.display = "none"
        document.getElementById("pdI").style.transform = "rotate(0)"
      } else {
        document.getElementById("pdDdBox").style.display = "block"
        document.getElementById("pdI").style.transform = "rotate(180deg)"
      }
    },
    openMobileEt() {
      if(document.getElementById("etDdBox").style.display == "block") {
        document.getElementById("etDdBox").style.display = "none"
        document.getElementById("etI").style.transform = "rotate(0)"
      } else {
        document.getElementById("etDdBox").style.display = "block"
        document.getElementById("etI").style.transform = "rotate(180deg)"
      }
    },
    openMobileEc() {
      if(document.getElementById("ecDdBox").style.display == "block") {
        document.getElementById("ecDdBox").style.display = "none"
        document.getElementById("ecI").style.transform = "rotate(0)"
      } else {
        document.getElementById("ecDdBox").style.display = "block"
        document.getElementById("ecI").style.transform = "rotate(180deg)"
      }
    },
    openMobileDi() {
      if(document.getElementById("diDdBox").style.display == "block") {
        document.getElementById("diDdBox").style.display = "none"
        document.getElementById("diI").style.transform = "rotate(0)"
      } else {
        document.getElementById("diDdBox").style.display = "block"
        document.getElementById("diI").style.transform = "rotate(180deg)"
      }
    },
    openMobileOther() {
      if(document.getElementById("otherDdBox").style.display == "block") {
        document.getElementById("otherDdBox").style.display = "none"
        document.getElementById("otherI").style.transform = "rotate(0)"
      } else {
        document.getElementById("otherDdBox").style.display = "block"
        document.getElementById("otherI").style.transform = "rotate(180deg)"
      }
    }
  }
}
</script>


<style scoped>
/* header */
  header{ height: 60px; position: relative; }
  header .logo-box{ height: 100%; float: left; margin-right: 10px; }
  header .logo-box a{
    height: 100%;
    padding: 16px 10px;
  }

  header nav{ height: 100%; float: left; }
  header nav a{ height: 60px; line-height: 60px; padding: 0 10px; position: relative; }
  header nav a:before{
    content: "";
    background: #000;
    height: 2.5px;
    position: absolute;
    top: 40px;
    left: 50%;
    width: 0;
    transform: translate(-50%, 0%);
    transition: .2s;
  }
  header nav a:hover:before{ width: calc(100% - 20px); }

  header .mobile-nav-btn{ float: left; display: none; font-size: 28px; height: 60px; padding: 0 10px; }

  header .side-box{ height: 100%; float: right; display: flex; }
  header #msAll{ padding: 0 10px; display: flex; align-items: center; z-index: 3; }
  header #msAll.clicked{ background-color: #eee; border: 1px solid #d6d6d6; border-bottom: none; }
  header #msAll.clicked:hover p:before{ width: 0; }

  header .search, header .cart
  { padding: 0 10px; display: flex; align-items: center; }
  header #msAll span{ margin-left: 5px; }
  header .search span, header .cart span
  { font-size: 22px; margin-left: 5px; }
  header .login{ padding: 0 10px; display: flex; align-items: center; }
  header .login i{ font-size: 36px; margin-left: 5px; }
  header .side-box p{ position: relative; }
  header .side-box p:before{
    content: "";
    background: #000;
    height: 2.5px;
    position: absolute;
    bottom: -5px;
    left: 50%;
    width: 0;
    transform: translate(-50%, 0%);
    transition: .2s;
  }
  header .side-box button:hover p:before,
  header .side-box a:hover p:before{ width: 100%; }


  #mobile-nav-container{
    background-color: #f2f2f2;
    width: 100%;
    border-bottom: 2px solid #000;
    position: absolute;
    top: 60px;
    left: 0;
    z-index: 1;
    display: none;
  }
  #mobile-nav-container .close-btn{
    background-color: #fff;
    width: 48px;
    font-size: 24px;
    margin-left: 20px;
    border: none;
    padding: 0 10px;
    display: inline-block;
    position: absolute;
    top: -55px;
  }
  #mobile-nav-container a, #mobile-nav-container button{
    width: 100%;
    height: 50px;
    line-height: 50px;
    border-bottom: 1px solid #e6e6e6;
    padding: 0 30px;
  }
  #mobile-nav-container button{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  #mobile-nav-container .dropdown-box{
    width: calc(100% - 30px);
    margin-left: auto;
    display: none;
  }


  #msAll-dropdown-menu{ background-color: #eee; color: #323232; width: calc(100% - 80px); position: absolute; top: 59px; left: 40px; z-index: 2; overflow: hidden; transition: .3s; }
  .dropdown-top{ display: flex; padding: 10px 0; border: 1px solid #d6d6d6; }
  .dropdown-top ul{ width: 16.66667%; }
  .dropdown-top ul li:first-child{ padding: 16px 20px; }
  .dropdown-top ul li a{ width: 100%; padding: 16px 20px; }
  .dropdown-top ul li:hover a{ text-decoration: underline; }
  .dropdown-bottom{ background-color: #d6d6d6; text-align: center; border-bottom: 2px solid #000; }
  .dropdown-bottom a{ padding: 10px 60px; }
  .dropdown-bottom a:hover span{ text-decoration: underline; }


  header form{ background-color: #fff; width: calc(100% - 230px); height: 100%; padding: 10px 0; position: absolute; top: 0; left: 190px; display: none; z-index: 4; }
  header form .back{
    width: 40px;
    height: 40px;
    font-size: 20px;
    display: none;
  }
  .input-box{ width: calc(100% - 80px); height: 100%; float: left; position: relative; }
  header form input{  width: 100%; border: 2px solid #000; padding: 10px 10px; display: block; float: left; }
  header form input:focus{ outline:  none; }
  header form .xi-search{ font-size: 20px; padding: 10px; position: absolute; top: 0; right: 0; }
  header form .cancel{ height: 40px; padding: 0 20px; margin-left: 10px; }


/* main */
  .box{ width: 24%; margin-bottom: 30px; }
  .box:hover img{ opacity: .8; }
  .box img{ width: 100%; margin-bottom: 30px; }
  .box a{ font-size: 14px; font-weight: bold; color: #0067b8; padding: 5px 0; }
  .box a span{ position: relative; transition: .2s; }
  .box a span:before{
    content: '';
    width: 0;
    height: 2px;
    background-color: #0067b8;
    position: absolute;
    bottom: -2px;
    transition: .2s;
  }
  .box a:hover span{ margin-right: 5px; }
  .box a:hover span:before{ width: 100%; }


/* introduce */
  .introduce{ position: relative; }
  .introduce:hover button{
    display: block;
  }
  .introduce .intro{ position: relative; animation-name: fade; animation-duration: 1s; display: none; }
  @keyframes fade { from {opacity: .5} to {opacity: 1} }
  .introduce .intro > a{
    width: 100%;
  }
  .introduce .img-bg{
    width: 100%;
    height: 70vh;
    background-size: cover;
    background-position: center;
  }
  .introduce .img-bg1{
    background-image: url(https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE3NJb7?ver=a8b5&amp;q=90&amp;m=8&amp;h=600&amp;w=1600&amp;b=%23FFFFFFFF&amp;l=f&amp;x=0&amp;y=166&amp;s=2120&amp;d=795&amp;aim=true);
  }
  .introduce .img-bg2{
    background-image: url(https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE3NR20?ver=7bd2&amp;q=90&amp;m=8&amp;h=600&amp;w=1600&amp;b=%23FFFFFFFF&amp;l=f&amp;x=0&amp;y=213&amp;s=2103&amp;d=789&amp;aim=true);
  }

  .introduce button{
    background-color: rgba(46, 46, 46, .5);
    width: 40px;
    height: 40px;
    border-radius: 50%;
    font-size: 20px;
    color: #eee;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    transition: all .4s;
    display: none;
  }
  .introduce .prev{ left: 40px; }
  .introduce .next{ right: 40px; }

  .img-text-box{
    width: 100%;
    padding: 0 5%;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
  }
  .img-text-box p{ margin: 20px 0 24px; }
  .img-text-box a{ width: 145px; font-size: 15px; font-weight: 600; padding: 10px 0; text-align: center; }
  .aBtn-white{ background-color: #fff; color: #000; }
  .aBtn-black{ background-color: #000; color: #fff; }
  .detail{ position: relative; transition: .2s; }
  .aBtn-white .detail:before{
    content: "";
    background: #000;
    width: 0;
    height: 2px;
    position: absolute;
    bottom: -3px;
    left: 0;
    transition: .2s;
  }
  .aBtn-black .detail:before{
    content: "";
    background: #fff;
    width: 0;
    height: 2px;
    position: absolute;
    bottom: -3px;
    left: 0;
    transition: .2s;
  }
  .img-text-box a:hover .detail:before{ width: 100%; }
  .img-text-box a:hover .detail{ margin-right: 10px; }


/* card-text */
  .card-text{ padding-top: 60px; padding-bottom: 30px; display: flex; flex-wrap: wrap; justify-content: space-between; }
  .a-box{ display: flex; flex-wrap: wrap; }
  .a-box a:first-child{ margin-right: 20px; }

/* store */
  .store{ position: relative; color: #fff;}
  .store > a{
    width: 100%
  }
  .store .img-bg{
    width: 100%;
    height: 70vh;
    background-size: cover;
    background-position: center;
    background-image: url(https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RW5kpU?ver=a008&amp;q=90&amp;m=8&amp;h=600&amp;w=1600&amp;b=%23FFFFFFFF&amp;l=f&amp;x=0&amp;y=212&amp;s=2063&amp;d=774&amp;aim=true);
  }


/* work-card-text */
  .work-card-text{ padding-top: 60px; padding-bottom: 30px; }
  .work-card-text h1{ margin-bottom: 20px; }
  .work-card-text .group{ display: flex; justify-content: space-between; flex-wrap: wrap;  }


/* follow */
  .follow{ display: flex; align-items: center; padding-top: 30px; padding-bottom: 60px; }
  .follow p{ font-size: 14px; color: #666; margin-right: 20px; }
  .follow a{ margin-right: 20px; }
  .follow a img{ width: 30px; height: 30px; }
  .follow a:active img{ border: 2px solid #666; }


/* footer */
  footer{ background-color: #eee; font-size: 11px; color: #666; padding: 40px 0 20px; }
  .footer-top{ display: flex; flex-wrap: wrap; justify-content: space-between; } 
  .footer-menu-box{ width: 16%; margin-bottom: 30px; }
  .footer-menu-box .text{ font-weight: 600; }
  .footer-menu-box li{ margin-bottom: 15px; }
  .footer-menu-box a:hover{ text-decoration: underline; }

  .footer-bottom{ display: flex; justify-content: space-between; align-items: center; }
  .footer-bottom a{ padding: 5px; }
  .language a{ display: flex; align-items: center; }
  .language a:hover span{text-decoration: underline; }
  .language img{ width: 20px; height: 20px; margin-right: 10px; }
  .footer-bottom-nav a{ margin-right: 10px; }


/* 반응형 */

@media (max-width: 1080px) {
  header{ padding: 0 30px; }
  .side-box .mobile-hide{ display: none; }
  header #msAll{ margin-right: 0; }
  header .search, header .cart{ margin-right: 0; }
  header .search span, header .cart span{ margin-left: 0; }

  header form{ width: calc(100% - 220px); left: 180px; }
  #msAll-dropdown-menu{
    width: 100%;
    left: 0;
  }
  .box{ width: 49%; }
  .introduce, .store{ padding: 0; 
  }
  .introduce button{
    width: 36px;
    height: 36px;
    font-size: 16px;
  }
  .introduce .prev{ left: 0px; }
  .introduce .next{ right: 0px; }

  .footer-menu-box{ width: 32%; }
}

@media (max-width: 860px) {
  header{ padding: 0 20px; }
  header .logo-box{ position: absolute; left: 50%; transform: translateX(-50%); }
  header nav{ display: none; }
  header .mobile-nav-btn{ display: block; }
  header #msAll{ display: none; }
  header .search{ height: 60px; position: absolute; top: 0; left: 72px; }
  header .login i{ margin: 0; }

  header form{ width: calc(100% - 40px); left: 20px; }
  header form .back{ display: inline-block; }
  .input-box{
    width: calc(100% - 40px);
    float: right;
  }
  header form .cancel{ display: none; }
  .img-text-box{ padding: 0 7%; }

  .introduce button{
    display: block;
  }
}

@media (max-width: 767px) {
  .introduce .img-bg, .store .img-bg{ height: 50vh; }
  .img-text-box{
    height: 280px;
    position: relative;
    text-align: center;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    top: -1px;
    transform: translateY(0);
  }
  .intro1 .img-text-box{ background-color: #707072; }
  .intro2 .img-text-box{ background-color: #e6e6e6; }
  
  .store .img-text-box{
    background-color: #e6e6e6;
    color: #000;
  }
}

@media (max-width: 500px) {
  header{ padding: 0; }
  header .logo-box{
    margin: 0;
  }
  header .logo-box a{
    padding: 18px 10px;
  }
  header .search{
    left: 48px;
  }
  header form{
    width: calc(100% - 10px);
    left: 0;
  }

  #mobile-nav-container .close-btn{
    margin-left: 0px;
  }

  .box{ width: 100%; }
  .box img{ margin-bottom: 10px; }
  .introduce .img-bg, .store .img-bg{ height: 40vh; }
  .footer-menu-box{ width: 100%; }
  .footer-bottom{ display: block; }
  .language{ margin-bottom: 10px; }
  .footer-bottom-nav a{ margin-bottom: 5px; }
}

</style>
