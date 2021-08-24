<template>
<q-layout view="lHh lpr lFf">
  <div v-bind:class="{'main': $q.platform.is.desktop,
  'mobile_main': $q.platform.is.ipad || $q.platform.is.mobile}"
  class="full-height" style="background-color:rgba(0, 0, 0, 1);">

    <q-header class="elevated" style="background-color:rgba(0, 0, 0, 0);;">
      <!-- <q-toolbar class="text-h4"> -->
        <q-space></q-space>
        <q-tabs v-model="selected_tab" shrink>
          <q-tab :style="[selected_tab == 't_0' ? {backgroundColor: 'white',color:'black'} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_hello')" style="width:120px;min-height:auto;!important;color: white;" label="Top" />
          <q-tab :style="[selected_tab == 't_1' ? {backgroundColor: 'white', color:'black'} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_about_me')" style="width:120px;min-height:auto !important;color: white;" label="about Me" />
          <q-tab :style="[selected_tab == 't_2' ? {backgroundColor: 'white', color:'black'} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_projects')" style="width:120px;min-height:auto !important;color: white" label="Projects" />
          <q-tab :style="[selected_tab == 't_3' ? {backgroundColor: 'white', color:'black'} : {}]" class="q-mr-sm q-py-xs custom_tab" @click="scrollToElement('id_contact_me')" style="width:120px;min-height:auto !important;color: white" label="Contact Me" />
        </q-tabs>
      <!-- </q-toolbar> -->
    </q-header>

    <section>
      <div class="full-height full-width flex flex-center text-center"
      style="background-color: rgba(0, 0, 0, 0.5)
      !important;z-index:0;height: 100vh !important;" id="id_hello">

      <q-img src="/statics/images/nameTag1_1.png"
      spinner-color="white"
      style="max-width: 500px; margin-right:10px"
    />
    <q-img src="/statics/images/nameTag2_1.png"
      spinner-color="white"
      style="max-width: 500px;"
    />
      </div>
    </section>
  </div>

  <div style="background-color:#f0f0f1; margin:30px" id="id_about_me"> 
    <div class="row">
    
      <div class="q-px-lg q-pb-md" style=" display:inline-block; margin:auto;">
      <q-timeline color="secondary">
        <q-timeline-entry heading>
          <span class="material-icons">school</span> GRADUATION
        </q-timeline-entry>

        <q-timeline-entry color="orange"
          icon="done_all">
          <template v-slot:title>
            2021
          </template>
          <template v-slot:subtitle>
            March 03, 2021
          </template>

          <div>
            한국폴리텍대학 서울강서캠퍼스 하이테크과정 스마트금융과 입학</br>
            - 2021.12 하이테크과정 졸업 예정
          </div>
        </q-timeline-entry>

        <q-timeline-entry>
          <template v-slot:title>
            2019
          </template>
          <template v-slot:subtitle>
            February 21, 2019
          </template>

          <div>
            명지대학교 인문캠퍼스 사회과학대학 디지털미디어학과 졸업</br>
          </div>
        </q-timeline-entry>



        <q-timeline-entry>
          <template v-slot:title>
            2013
          </template>
          <template v-slot:subtitle>
            February 22, 2013
          </template>

          <div>
            이화여자대학교병설 미디어고등학교 졸업
          </div>
        </q-timeline-entry>

        <q-timeline>
        </q-timeline>
      </q-timeline>
  </div>
    </div>
  </div>

<!-- language Skill -->

    <div class="q-pa-md">
    <div class="q-gutter-y-md column">
      <q-toolbar class="bg-grey-3 shadow-2 rounded-borders">
        <q-space />
          <q-btn stretch flat style="font-size:20px;" label="LANGUAGE SKILL" />
        <q-space />
      </q-toolbar>
    </div>
  </div>
  <div class="q-pa-md flex flex-center" style="text-align:center;">
      <q-circular-progress
      show-value
      font-size="12px"
      :value="75"
      size="200px"
      :thickness="0.22"
      color="teal"
      track-color="grey-3"
      class="q-ma-md"
    >
      <h5>JAVA</br>75%</h5>
    </q-circular-progress>

        <q-circular-progress
      show-value
      font-size="12px"
      :value="50"
      size="200px"
      :thickness="0.22"
      color="teal"
      track-color="grey-3"
      class="q-ma-md"
    >
      <h5>PYTHON</br>50%</h5>
    </q-circular-progress>

        <q-circular-progress
      show-value
      font-size="12px"
      :value="60"
      size="200px"
      :thickness="0.22"
      color="teal"
      track-color="grey-3"
      class="q-ma-md"
    >
      <h5>JAVASCRIPT</br>60%</h5>
    </q-circular-progress>
  
  </div>
    



  <!-- my works -->
  <div style="background-color:#afb3b0" id="id_projects">
      <div class="row q-px-xl">
        <div class="text-h2 text-center text-white q-py-sm q-my-md full-width">
          <div class="q-pa-md q-gutter-sm">
            <q-btn color="white" outline style="color: goldenrod;" label="My Project" />
          </div>
        </div>
      </div>

        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section horizontal>
            <q-card-section>
              <div class="text-overline text-black">JAVA PROJECT</div>
                  <div class="text-h4 q-mt-sm q-mb-xs">
                    <a class="project_link" style="text-decoration: none;color: #111111;" href="https://github.com/kimscode0116/final_project_GamewebPage" target="_blank">
                    'Oaiagame' Project</a>
                  </div>
                  <div class="text-caption text-grey-9">
                    Java와 Python을 활용한 게임과 웹페이지 개발

                    <ul>
                      <li>Java Spring Framework</li>
                      <li>python 3.8, Java 1.8</li>
                      <li>Oracle DB, Oracle cloud</li>
                      <li>Pygame Library</li>
                    </ul>
                    
                    - Java Spring Frame work(Spring MVC)를 활용하여 실제 서비스 가능한 웹페이지를 구현 </br>
                    - Oracle DB 연동을 통한 효율적 데이터 관리 </br>
                    - AWS 서버와 Oracle Cloud를 이용하여 완성된 프로젝트 배포
                    - 게임 웹사이트들에 있는 로그인, 랭킹, 커뮤니티 등의 기능을 모두 구현한 완성도 있는 웹을 구현
                  </div>
                  <div class="text-h4 q-mt-sm q-mb-xs">
                    <q-btn align="around" class="btn-fixed-width" color="brown-5" href="https://github.com/kimscode0116" label="More Datails Here" icon="fab fa-github" />
                  </div>
            </q-card-section>
              <div class="col-6">
                <q-card-section class="col-3">
                  <q-img src="/statics/images/project_oaiagame.png"  />
                </q-card-section>
              </div>
            </q-card-section>
          </q-card>
        </div>
    

      <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section horizontal>
            <q-card-section>
              <div class="text-overline text-black">Python PROJECT</div>
                  <div class="text-h4 q-mt-sm q-mb-xs">
                    <a class="project_link" style="text-decoration: none;color: #111111;" href="https://github.com/kimscode0116/kopoStockModel/tree/master/student/4th/%EA%B9%80%EC%9D%80%ED%98%9C" target="_blank">
                    파이썬을 활용한 주가예측</a>
                  </div>
                  <div class="text-caption text-grey-9">
                    크롤링과 Python을 활용한 주가예측 모델

                    <ul>
                      <li>install Selenium</li>
                      <li>pip bs4, FinanceDataReader, matplotlib</li>
                      <li>python 3.8</li>
                    </ul>
                    
                    - selenium을 통해 유저가 입력하는 주식 종목의 종목 코드 및 주가 정보를 크롤링 <br />
                    - 분기별 부채 비율의 변동률이 100이상인 경우, 기업의 유보율을 500% 기준으로 위험도를 경고 <br /> 
                    - 전년 대비 연간 매출액 및 영업이익, 당기 순이익 등의 증감의 폭에 따라 성장도를 판단 <br />
                    - 수집된 데이트를 통해 실제 주식의 가치(주당 순이익)를 합산하여 최종으로 해당 주식의 구매 추천
                  </div>
                  <div class="text-h4 q-mt-sm q-mb-xs">
                    <q-btn align="around" class="btn-fixed-width" color="brown-5" href="https://github.com/kimscode0116/kopoStockModel/tree/master/student/4th/%EA%B9%80%EC%9D%80%ED%98%9C" label="More Datails Here" icon="fab fa-github" />
                  </div>
            </q-card-section>
              <div class="col-6">
                <q-card-section class="col-3">
                  <q-img src="/statics/images/predict1.png" />
                  <q-img src="/statics/images/predict2.png" />
                </q-card-section>
              </div>
            </q-card-section>
          </q-card>
        </div>

          <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section horizontal>
            <q-card-section>
              <div class="text-overline text-black">VUE PROJECT</div>
                  <div class="text-h4 q-mt-sm q-mb-xs">
                    <a class="project_link" style="text-decoration: none;color: #111111;" href="https://github.com/kimscode0116/final_project_GamewebPage" target="_blank">
                    'TODO_LIST' Project</a>
                  </div>
                  <div class="text-caption text-grey-9">
                    Vue.js로 만드는 mobile/web TODO_LIST

                    <ul>
                      <li># install dependencies : npm install</li>
                      <li># serve with hot reload at localhost:8080 : npm run dev</li>
                      <li># build for production with minification : npm run build</li>
                      <li> - vue.js 및 web DB를 베이스로 웹 CRUD 구현</li>
                      <li> - PC / MOBILE 환경에서의 화면 크기를 모두 고려한 UI 구성</li>
                    </ul>
                        <q-card-section class="col-6">
                  <q-img src="/statics/images/vueTodo1.png" />
                </q-card-section>
                    </div>
                  <div class="text-h4 q-mt-sm q-mb-xs">
                    <q-btn align="around" class="btn-fixed-width" color="brown-5" href="https://github.com/kimscode0116" label="More Datails Here" icon="fab fa-github" />
                  </div>
            </q-card-section>
              <div class="col-6">
                <q-card-section class="col-6">
                  <q-img src="/statics/images/vueTodo2.png" />
                </q-card-section>
              </div>
            </q-card-section>          
          </q-card>
        </div>
        </br>
  </div>

  
  <!-- Mail -->
  <div id="contact_us" >
    <div class="col-md-8 col-lg-8 col-xs-12 col-sm-12 q-px-md q-pt-sm">
          <div class="text-h2 text-center text-black q-py-xs q-my-xs">
               If you have Any question,
          </div>
    </div>
    <!-- <div style="background-color: red !important;"> -->
      <form action="https://formspree.io/f/xeqvpdnq" method="POST">
        <div class="q-pa-md" style="text-align: center;">

          <!-- name / email -->
          <div class="q-gutter-md">
            <div style="display:inline-block; width: 500px;">  
            <q-input rounded outlined v-model="name" name="name" bg-color="white" label="이름을 입력하세요">
              <template v-slot:append>
                <q-icon name="list" style="color:gray" />
              </template>
            </q-input>
            </div>
            <q-separator dark />

            <div style="  display:inline-block; width: 500px">  
            <q-input type="email" rounded outlined v-model="email" name="_replyto" bg-color="white" label="이메일을 입력하세요">
              <template v-slot:append>
                <q-icon name="email" style="color:gray" />
              </template>
            </q-input>
            </div>
            <q-separator dark />

          </div>

          <!-- textarea -->
          <div class="q-gutter-md">
            <div class="q-pa-md" style="display:inline-block; width: 500px;">
            <q-input required v-model="message" name="message" class="" filled type="textarea" bg-color="lightgray"outlined label="내용을 입력하세요">
            </q-input>
          </div>
          
        </div>

        <!-- btn sendmail -->
        <div class="row flex flex-center text-center q-pb-xl q-mt-md">
          <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12">
            <q-btn outline rounded color="primary" type="submit" size="lg" style="background:green;color: white" label="send Mail" />
          </div>
        </div>

        </div>
      </form>
    <!-- </div> -->
  </div>
  <q-separator black />


  

  <!-- 하단 footer (SNS) -->
  
  <q-toolbar class="flex flex-center text-white" id="id_contact_me">
    <div class="q-pa-sm q-gutter-sm">
      <q-btn target="_blank" round color="grey" type="a" href="https://github.com/kimscode0116" icon="fab fa-github" />
      <q-btn round color="grey" type="a" href="mailto:eunhye3576@gamil.com" icon="email" />
      <q-btn target="_blank" round color="grey" type="a" href="https://www.instagram.com/kkeehhh/" icon="fab fa-instagram" />
    </div>
  </q-toolbar>
</q-layout>
</template>

<script>
import {
  scroll
} from 'quasar'

const {
  getScrollTarget,
  setScrollPosition
} = scroll

export default {
  name: 'PageIndex',
  data() {
    return {
      name: "",
      email: "",
      message: "",
      selected_tab: 't_0'
    }
  },
  
  methods: {
    scrollToElement(id) {
      let el = document.getElementById(id)
      const target = getScrollTarget(el)
      const offset = el.offsetTop - 65
      const duration = 800
      setScrollPosition(target, offset, duration)
    }
  }
}

</script>

<style>
.main {
  background: url("https://media.giphy.com/media/YpMYUdwJvFkkd5lL1q/giphy.gif?cid=ecf05e478s9yp2kykgi39kysc02w3jwkux6hkuur1prfrqit&rid=giphy.gif&ct=g") no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  height: 100vh !important;
}

.mobile_main {
  background: url("https://media.giphy.com/media/fSRQtBAzrPokPCItuu/giphy.gif") no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  height: 100vh !important;
}

.my-card {
  width: 100%;
  max-width: 800px;
  border: none;
  border-radius: 0px;
}

.sponsor-card {
  width: 100%;
  max-width: 240px;
  border: none;
  border-radius: 6px;
}

.project_link:hover {
  text-decoration: underline !important;
}


#contact_us {
  /* background: url(/statics/images/contact_us.jpg); */
  background-size: cover;
  background-position: 50%;
  background-attachment: fixed;
  background-repeat: no-repeat;
}

.custom_tab {
  width: 130px;
}

body {
  overflow-x: hidden;
}

section {
  position: relative;
}

section>* {
  z-index: 9;
  position: relative;
  top: 0;
}
</style>
