# 🚀 Vue.js 시작하기
## Vue.js 란?
 > *자바스크립트 프레임워크로 다른 프레임워크에 비해 유연하고 가벼우며 라우터(router)를 활용해 단일페이지 애플리케이션 아키텍쳐구성에 효과적이다.*

### 개발 환경설정
 - Node.js
 - npm : Node Package Manager
 - Chrome Vue.js devtools : Chrome 브라우저 기반에서 작동하는 Vue.js전용 디버깅, 개발도구
   - <a href="https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=ko">Vue.js devtools 설치</a>
 - Vue-CLI : 앱 작성의 기본틀 제공
  
## ✅ Vue.js의 `LifeCycle`
<!-- > <img src="https://kr.vuejs.org/images/lifecycle.png"> -->
> <img src="https://gblobscdn.gitbook.com/assets%2F-M26jG1xuJ_y_q6GUJdp%2F-M26n5U2kzzz42LMgqau%2F-M26n8a_2P3mYmOeE2im%2FScreen-Shot-2019-01-14-at-12.44.09-AM.png?alt=media">
<br>

### Vue Template
> *Vue.js는 렌더링 된 DOM을 기본 Vue인스턴스의 데이터에 선언적으로 바인딩할 수 있는 HTML기반 템플릿 구문을 사용한다.<br>각 페이지마다 HTML코드와 Component가 들어가는 위치이다.*

### Component
> *컴포넌트는 Vue에서 가장 중요한 기능으로 HTML 엘리먼트를 확장하여 재사용 가능한 코드를 ***캡슐화*** 하는 기능으로 HTML Tag와 같은 형태를 갖고있어 혼동할 수 있다.<br>사용할 Component를 import해준다면 로컬의 어느곳에서든 사용 가능하다.<br>ex) Home.vue - `<LoadingDiv></LoadingDiv>`*
### vue-router
> *애플리케이션에서 사용자가 요청한 URI 경로에 따라 각각 다른 화면이 렌더링되고 `SPA(Single Page Application)`를 손쉽게 만들 수 있도록 함.*
 - 중첩된 경로, 뷰를 매핑할 수 있다.
 - 컴포넌트 기반의 라우팅을 구현할 수 있다.
 - Vue.js의 전환효과를 적용할 수 있다.
 - History Mode와 Hash Mode를 모두 사용할 수 있다.
 - queryString, Parameter, WildCard를 사용하여 라우팅을 구형할 수 있다.
  
import구문을 이용해 vue-router를 참조하고 컴포넌트를 매핑한 라우터 객체를 인스턴스 만들때 지정.
템플릿에서 `<router-link></router-link>`로 하이퍼링크 생성 후 URI경로에 따라 router 객체에서 매핑한 컴포넌트가 `<router-view></router-view>`에 나타나게 됨.
 - **Base-Vue에서는 Header의 Navigation기능에서 사용하고 있다. <br>/router/index.js를 보면 2Depth 기능을 사용하기 위하여 route 선언해줄 때 children을 사용함.**
> *⚠️ `vue-router`를 사용하기 위해서는 `main.js`에서 import구문을 이용해 참조하고 router를 사용할수 있도록 선언 해줘야한다.*

### .vue파일에서 script작성
> `<template></template>`하단에 `<script></script>`를 만들어준다.
> ```javascript
> <script>
> export default {
>   data() {
> 
>   }
> }
> </script>
> ```
> 스크립트를 작성 할 때 `methods: {}`에 함수 만들어주고 `LifeCycle`에 맞게 함수 호출구문 만들어주면 사용가능하다.

### axios
> *HTTP 요청을 위한 클라이언트로 API요청할 때 중간 역할을 한다.*
> axios Package를 터미널을 통해 설치하고 `main.js`에서 import구문을 통해 사용할 수 있도록 해준다.<br>base-vue에서는 `/api/index.js`에서 각각 원하는 API데이터를 사용하기 위해 함수화 해줌. 

### Vuex Store(상태관리)
> *앞서 `axios`를 통해 API 데이터를 호출 했다면 호출한 데이터를 저장할 공간이 필요하다.<br>필요할때 마다 호출할 수 있지만 페이지 로딩시간이 길어지고 과부하가 일어날 수 있기떄문에 저장하고 가져오는 방식 중 `Vuex Store`방식을 택하게 됨.*

***Web Storage 종류***
 - <p style="color:red">Vuex Store : Application에 대한 상태관리 패턴</p>

    > 1. 해당 application의 모든 컴포넌트에대한 중앙 집중식 저장소 역할을 함.
    > 2. 저장소에서 직접 상태를 변경하지 않고 반드시 변이(mutation)를 통해서만 변경.
 - Local Storage / Session Storage
    > 1. key와 value형태로 이루어짐.
    > 2. 객체 정보를 저장 할 수 있다.
    > 3. 영구적으로 데이터를 저장 할 수 있다.
    > 4. Session Storage는 세션 종료시 클라이언트에 대한 정보를 삭제한다.
 - Cookie
    > 1. 매번 서버로 전송 된다.(서버에 부담이 된다)
    > 2. 만료일자를 지정해서 원하는 기간만큼 데이터를 저장할 수 있다.
    > 3. 암호화가 존재하지 않아 보안성이 취약하다.


#### Vuex store로 API data를 저장하고 필요할 때 저장된 데이터 사용 가능
<img src="https://blog.martinwork.co.kr/images/vue/vuex-state-one-way-data-flow.png">

 > *사용자(Component)가 `Action`을 취했을 때  `Actions`는 외부 API를 호출하고 `Mutations`(변이)을 통해 `State`를 변경한다. `State`의 값이 변경되면 해당 컴포넌트가 다시 로딩.*
 - `state` : 상태(데이터가 들어가는 곳)
 - `mutation` : 변이(데이터가 실제로 변경되는 곳_규약)
 - `action` : 함수가 들어가는 곳(비동기적 처리)
  
***사용 할 때는 해당 페이지에서 `dispatch`해야 사용 가능함***

## 📲 Base-Vue의 기본 화면 구성
 > ### ***Component -> Template -> Page(Layout)***

### Home.vue
 >
## 📝 Clone Project
 ### 1️⃣ Node.js Version 확인
  - #### `cmd`창에서 `$ node --version`
  - #### ***설치된 Node.js Version이 14.17.0이 아니라면..***
    - `$ nvm list` : 현재 설치된 Node.js Version 확인
    - `$ nvm install 14.17.0` : Ver.14.17.0 설치
    - `$ nvm list` : 다시 PC에 설치된 Node.js 확인(Ver.14.17.0이 설치된것을 확인할 수 있다)
    - `$ nvm use 14.17.0` : 14.17.0 Version으로 Node.js 변경
    - `$ node --version` : 현재 사용중인 Version을 확인하여 제대로 변경 되었는지 Check
    - *참고) <a id="node-version-change" nameid="node-version-change" href="https://node-js.tistory.com/entry/Nodejs-nvm%EC%9C%BC%EB%A1%9C-%EC%89%BD%EA%B2%8C-Node-%EB%B2%84%EC%A0%84%EB%B3%80%EA%B2%BD%ED%95%98%EA%B8%B0">Node Version 변경하기</a>*
 ### 2️⃣ GitLab에서 Project Clone 하기
 <!-- - #### `$ git clone https://gitlab.com/bstones-feteam/base-vue.git` -->
  - #### *VSCode로 바로 열었을 경우나 git으로 Clone했을 경우*
    - VSCode에서 터미널창 진입 or `cmd` 진입하여 해당 프로젝트 폴더로 이동
  #### `$ npm install`
  - #### *`npm install`시 Project에서 사용된 Module(Package)이 자동으로 설치*
   > *여러 사람과 함께 작업을 진행할 때는 `pull`받고 나서 `npm install`를 해야 추가로 Package가 사용 되었을 때 정상적으로 실행 할 수 있다.<br>⚠️ `npm update`는 Package를 최신 Version으로 설치해주는 명령어 이므로 Version을 지정해서 설치한 Package가 있을 수 있으니 `npm install`을 해주는 것이 좋다.*

 ### 3️⃣ `base-vue` Project 실행 방법
  - #### `npm update` 가 완료된 후  `npm run serve` 입력
  - #### http://localhost:8080/ 접속
<br>

## 📝 Vue.js Project 만들기
### 1️⃣ `vue-cli` 설치
 - #### `cmd`창에서 `$ npm install @vue/cli -g`
### 2️⃣ 프로젝트 생성
- #### `$ vue create 프로젝트명`
  ⚠️ ***create 할 때 순서대로 선택***
  - Manually select features
  - Choose Vue Version , Babel , Router , Vuex , CSS Pre-processors , Linter/Formatter
    - `space bar`눌러서 선택
  - 2.x
  - Yes
  - Sass/SCSS (with node-sass)
  - ESLint with error prevention only
  - Lint on save
  - In dedicated config files
  - No

*위 방식으로 프로젝트를 만들었다면 기본으로 `core-js`, `vue`, `vue-router`, `vuex`  Package 설치되어 있음*
<br>

### 3️⃣ 프로젝트에 필요한 패키지 설치 
#### - **🎁 Base-Vue에서 필요한 패키지**
```
  npm i bootstrap popper.js/core jquery vue-frag axios swiper vue-awesome-swiper vuejs-paginate query-string vue-meta vue2-editor quill material-icons fullcalendar date-fns jquery-ui-dist aos vue-masonry vue-masonry-css
```

| Package Name | Meaning |
|:---:|---|
| **⭐️ `bootstrap`** | bootstrap의 css를 사용하기 위해 사용 |
| **⭐️ `popper.js/core`** | Bootstrap관련해서 ToolTip을 보여주는 Package |
| **⭐️ `jquery`** | jquery를 사용하기 위한 package <br>*( vue.config.js 파일을 따로 만들어서 jquery를 전역에서 사용할 수 있도록 해줘야한다. )* |
| **⭐️ `vue-frag`** | `<template>`안에 div로 감싸야 했는데 `vue-frag` package사용 | 후 `<div v-frag></div>`로 감싸주면 실제 html에서는 안보이게 만들어짐. |
| **⭐️ `axios`** | data를 요청할 때 중간역할을 한다. |
| **`swiper`** | swiper기능 사용시 필요 css |
| **`vue-awesome-swiper`** | `component`로 만들어주는 역할(`swiper`와 세트) |
| **⭐️ `vuejs-paginate`** | Pagination을 위한 Package로 CSS로 스타일 지정이 가능 |
| **`query-string`** | URL 쿼리 문자열 구문 분석 및 문자열 화 |
| **`vue-meta`** | meta Tag사용을 위한 Package |
| **`vue2-editor`** | 게시판에 에디터를 사용하기 위한 Text Editor Package |
| **`quill`** | Editor CSS 변경을 위한 Package |
| **`material-icons`** | material icon을 사용하기 위한 Package |
| **`fullcalendar`** | Calendar 관련 Package |
| **`date-fns`** | date format 변경을 위한 Package |
| **`jquery-ui-dist`** | jquery ui 에서 이벤트 등록시 날짜 Form사용하기 위한 Package |
| **`aos`** | Animation On Scroll 스크롤 애니메이션 Package(https://michalsnik.github.io/aos/) |
| **`vue-masonry`** | masonry layout(핀터레스트 타입) 자동 줄맞춤 해주는 Package |
| **`vue-masonry-css`** | 위 `vue-masonry`를 사용할때는 구역을 미리 정해 놓기 때문에 Pagination을 사용할때는 간격조절 하기가 쉽지 않다. 이를 보완하기 위해 사용하는 Package |

- #### 🔊 jquery사용
  ***jquery사용을 위해 프로젝트 로컬 경로에 `vue.config.js`파일 생성***

   ```javascript
   const webpack = require('webpack')
   
   module.exports = {
     configureWebpack: {
       plugins: [
         new webpack.ProvidePlugin({
           $: 'jquery',
           jquery: 'jquery',
           'window.jQuery': 'jquery',
           jQuery: 'jquery'
         })
       ]
     }
   }
   ```
  ***추가 해준뒤 프로젝트 로컬에 생성되어있는 `.eslintrc.js`파일에 아래 코드 추가***
   ```javascript
   module.exports = {
    root: true,
    env: {
      // 추가해준다
      node: true,
      jquery: true
    },
    ```
<br>

### 4️⃣ `main.js` 활용 하기
  - ***`main.js`에서는 Package나 script, css 등 전역으로 사용할 항목들을 선언 해준다.***
    ***예를 들어 아래 함수처럼 자주 사용할 함수를 등록해주면 plugin화 해서 app전체에서 `$scrollToTop`을 사용할 수 있다.***
    ```javascript
    // plugin
    const plugins = {
      install() {
        Vue.prototype.$scrollToTop = () => window.scrollTo(0, 0);
      }
    }
    ```

 -  ***🔊 main.js에서 전역에서 사용가능한 plugin을 만들 수 있다.(utill, api, axios 등) 필요할때마다 `.vue`파일에서 선언해주는게 아니라 main.js에 선언되어 있는것을 가져다 쓴다.***
<br>

`Home.vue`에서 Api를 사용할때 `<script>`내의 `method: {}`에서 Api 호출함수 사용.
 > ```javascript
 > methods: {
 >    callGetAlbum() {
 >      this.$api                 //$api는 main.js에서 만든 Plugin
 >        .getAlbum()             //api > index.js에서 만든 함수
 >        .then((response) => {   //getAlbum()을 호출하고 난 뒤에 실행
 >          this.dataDummy = response.data; 
 >       // getAlbum()의 리턴값을 (LocalStorage의 dataDummy값) response.data에 저장
 >          this.$utils.setLocalStore("dataDummy", response.data);  
 >       // main.js에서 만들어진 $utill에서 setLocalStore()함수의 
 >       // key값과 value값에 각각 "dataDummy"와 response.data를 넣어준다.
 >        })
 >        .then(() => {
 >          this.loading = false;
 >        })
 >        .catch((error) => {
 >          console.log(error);
 >        });
 >    },
 >  },
 >  created() {
 >    this.callGetAlbum();
 >  },
 > ```

#### 🔊 *`router > index.js`에서 2-Depth 메뉴를 만들 때 `children`을 사용하여 만든다.<br>1-Depth는 2-Depth의 첫번째 항목을 가져와야 한다면 `redirect`를 사용하여 2-Depth의 첫번째 항목의 path값을 가져오도록 한다.*
>  ```javascript
>  path: "/hello",
> // path를 "/hello"로 지정했지만 redirect 했기 때문에 
> // 1-Depth인 "헬로우" 클릭 시 "/hello/violin" 으로 이동하게 됨.
>   redirect: '/hello/violin',
>   name: "hello",
>   component: Hello,
>  ```

#### ✅ ***`v-bind:class=" "` `v-bind:key=" "` 는 반복적으로 사용하는 부분이 있기에 편의성을 위해 `:class=" "` `:key=" "`와 같은 형식으로 사용하는게 좋을 듯함.***

#### ✅ `script` 를 작성하고 싶을 땐 `methods` 안에 함수를 만들고 *[Life Cycle](#vue-lifecycle)* 에 맞게 함수를 호출한다.
<br>



### 📝 컴포넌트의 인스턴스 및 요소에 접근
 - #### `ref`속성 사용하여 자식 요소에 레퍼런스 ID를 할당할 수 있다.
    ex) base-vue/template/TempBoardView.vue
    ```js
    <template>
    ...
    <TempBoardDelete ref="tempDelete" :deleteId="$route.params.id">
    </TempBoardDelete>
    ...
    methods: {
      handleDelete() {
        this.$refs.tempDelete.BoardDelete();
      },
    }
    ```
 - 위와 같이 사용하면 `<TempBoardDelete>`의 인스턴스 요소에 접근 가능함.
> *`$refs` 는 컴포넌트가 렌더링 된 후에 접근할 수 있으며, 반응형이 아님. <br>즉, 직접적인 자식 요소 제어에만 유효함.<br> `$refs`를 <a style="color:red">template </a>나 <a style="color:red">computed 속성</a> 안에 포함시키지 않는 것이 좋다.*

 - #### `props`속성은 컴포넌트간에 데이터를 전달할 수 있는 통신 방법
   - 상위 컴포넌트에서 하위 컴포넌트로 내보내려는 데이터 속성


## base-vue page Description
> base-vue는 사실 로컬경로에 있는 App.vue를 보고 있는 것.<br>App.vue안에 내용을 보면 `Accessibility`와 `Container`라는 Component를 import시켜 사용하고 있는 모습이다.<br>`Container.vue`를 확인해보면 기본적인 HTML-layout인 Header-Main-Footer로 나눠져 있는걸 확인 할 수 있고 마찬가지로 Component로 사용한다.

*Vue.js는 컴포넌트들을 조합해 전체 애플리케이션을 작성한다. 컴포넌트들은 부보-자식 관계로 형성되며 속성(props)을 통해 자식 컴포넌트로 정보를 전달할 수 있다.*
- <a href="http://selphy1.cafe24.com/basevue/">Home : </a>형식의 모듈별 최신글 및 공지사항과 리스트 형식의 좋아요순, 조회수순(인기글) 확인
  - 페이지 설명
- 헬로우
  - <a href="http://selphy1.cafe24.com/basevue/hello/static">스태틱 : </a>정적인 컨텐츠를 여러 방식(swiper, video, history)으로 활용
  - <a href="http://selphy1.cafe24.com/basevue/hello/handling">핸들링 : </a>자주 사용하는 간단한 핸들링 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/hello/slider">슬라이더 : </a>다양한 Swiper 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/hello/animation">애니메이션 : </a>AOS(Animation On Scroll) Lib를 활용한 스크롤 애니메이션 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/hello/location">로케이션 : </a>kakaomap API를 활용한 지도 기능 구현
- 모듈1
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1table">테이블 : </a>API data(동적인 데이터)를 테이블 형태로 출력 및 C.R.U.D 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1sort">정렬 : </a>테이블 형태의 리스트를 여러 방식으로 정렬
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1perpage">퍼페이지 : </a>테이블 형태의 리스트의 갯수를 조절하는 기능
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1search">검색 : </a>테이블 형태의 컨텐츠의 검색 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1category">카테고리 : </a>테이블 형태의 리스트를 카테고리별 분류
- 모듈2
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2card">카드 : </a>API data(동적인 데이터)를 카드 형태로 출력 및 C.R.U.D 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2card">정렬 : </a>카드 형태의 리스트를 여러 방식으로 정렬
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2perpage">퍼페이지 : </a>카드 형태의 리스트의 갯수를 조절하는 기능
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2search">검색 : </a>카드 형태의 컨텐츠의 검색 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2category">카테고리 : </a>카드 형태의 리스트를 카테고리별 분류
- 모듈3
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3more">더보기 : </a>동적인 컨텐츠를 더보기 버튼을 통해 5개씩 추가
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3infinite">무한스크롤 : </a>카드형식의 동적인 데이터를 스크롤을 내리면 자동으로 컨텐츠 추가
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3masonry">Masonry : </a>동적인 데이터를 핀터레스트 방식에서 Masonry 패키지를 사용하여 자동으로 높이 조절하는 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3type">타입 : </a>동적인 데이터를 여러 타입으로 볼 수 있는 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3accord">아코디언 : </a>동적인 데이터를 아코디언 방식으로 출력
- 모듈4
  - <a href="http://selphy1.cafe24.com/basevue/module4/m4event">이벤트 : </a>이벤트 형태의 동적인 데이터 출력 및 이벤트 C.R.U.D 기능 구현
  - <a href="http://selphy1.cafe24.com/basevue/module4/m4calendar">캘린더 : </a>등록된 이벤트 날짜를 calendar에 출력
  - <a href="http://selphy1.cafe24.com/basevue/module4/m4map">지도 : </a>등록된 이벤트 장소를 kakaomap API를 이용해 지도에 출력
- 모듈5
  - <a href="http://selphy1.cafe24.com/basevue/module5/m5share">공유 : </a>게시판 contents SNS 공유기능 구현(facebook, twitter, naver, kakao, email, URL copy)
  - <a href="http://selphy1.cafe24.com/basevue/module5/m5comment">댓글 : </a>게시판 댓글 기능 구현(댓글 수, 댓글등록, 수정, 삭제)
- 회원
  - <a href="http://selphy1.cafe24.com/basevue/member/mypage">마이페이지 : </a>로그인을 하지 않았을땐 /login으로 이동하게 되고 로그인시 카카오계정으로 로그인 가능하며 로그인을 하고난 뒤에는 계정 정보가 나온다.
  - <a href="http://selphy1.cafe24.com/basevue/member/login">로그인 : </a>카카오계정으로 로그인할 수 있도록 로그인 창이 나옴.
  - <a href="http://selphy1.cafe24.com/basevue/member/logout">로그아웃 : </a>로그인을 하고나면 로그인 탭이 로그아웃으로 변경 되고 로그아웃후 Home으로 이동됨.


***Base-Vue 프로젝트 구조***
 ```bash
Base-vue
    ├── vue.config.js
    ├── README.md
    ├── package.json
    ├── package-lock.json
    ├── jsconfig.json
    ├── deploy.js
    ├── babel.config.js
    ├── .gitignore
    ├── .eslintrc.js
    ├── .browserslistrc
    └── src
       ├── main.js
       ├── App.vue
       ├── utils                 필터 등의 유틸리티 함수
       │  └── index.js
       ├── templates             템플릿
       │  └── TempCardLink.vue
       ├── store                 상태 관리
       │  └── index.js
       ├── settings              도메인, 사이트 정보
       │  └── index.js
       ├── router                라우터
       │  └── index.js
       ├── pages                 페이지
       │  ├── Hello
       │  │  ├── Animation.vue
       │  │  ├── Handling.vue
       │  │  ├── Hello.vue
       │  │  ├── Location.vue
       │  │  ├── Parallax.vue
       │  │  ├── Slider.vue
       │  │  └── Static.vue
       │  ├── Member
       │  │  ├── Auth.vue
       │  │  ├── Login.vue
       │  │  ├── Logout.vue
       │  │  ├── Member.vue
       │  │  └── Mypage.vue
       │  ├── Module1
       │  │  ├── M1Add.vue
       │  │  ├── M1Category.vue
       │  │  ├── M1Edit.vue
       │  │  ├── M1Perpages.vue
       │  │  ├── M1Search.vue
       │  │  ├── M1Sort.vue
       │  │  ├── M1Table.vue
       │  │  ├── M1View.vue
       │  │  └── Module1.vue
       │  ├── Module2
       │  │  ├── M2Add.vue
       │  │  ├── M2Card.vue
       │  │  ├── M2Category.vue
       │  │  ├── M2Edit.vue
       │  │  ├── M2Perpages.vue
       │  │  ├── M2Search.vue
       │  │  ├── M2Sort.vue
       │  │  ├── M2View.vue
       │  │  └── Module2.vue
       │  ├── Module3
       │  │  ├── M3Accord.vue
       │  │  ├── M3Infinite.vue
       │  │  ├── M3InfiniteView.vue
       │  │  ├── M3Masonry.vue
       │  │  ├── M3MasonryView.vue
       │  │  ├── M3More.vue
       │  │  ├── M3MoreView.vue
       │  │  ├── M3Type.vue
       │  │  ├── M3TypeView.vue
       │  │  └── Module3.vue
       │  ├── Module4
       │  │  ├── M4Add.vue
       │  │  ├── M4Calendar.vue
       │  │  ├── M4Edit.vue
       │  │  ├── M4Event.vue
       │  │  ├── M4Map.vue
       │  │  ├── M4View.vue
       │  │  └── Module4.vue
       │  ├── Module5
       │  │  ├── M5Comment.vue
       │  │  ├── M5CommentView.vue
       │  │  ├── M5Share.vue
       │  │  ├── M5ShareView.vue
       │  │  └── Module5.vue
       │  ├── Search
       │  │  └── Search.vue
       │  ├── Home.vue
       │  └── NotFound.vue
       ├── layouts               페이지 레이아웃
       │  ├── Accessibility.vue
       │  ├── Container.vue
       │  ├── Footer.vue
       │  ├── Header.vue
       │  ├── Main.vue
       │  ├── MainBottom.vue
       │  ├── MainBreadcrumb.vue
       │  ├── MainTop.vue
       │  └── Navigation.vue
       ├── components            컴포넌트
       │  ├── Button
       │  │  ├── ButtonAnchor.vue
       │  │  ├── ButtonBasic.vue
       │  │  ├── ButtonInput.vue
       │  │  ├── ButtonLink.vue
       │  │  ├── ButtonSubmit.vue
       │  │  └── ButtonWrap.vue
       │  ├── Card
       │  │  ├── CardBody.vue
       │  │  ├── CardFigure.vue
       │  │  ├── CardFooter.vue
       │  │  ├── CardGroup.vue
       │  │  ├── CardLink.vue
       │  │  └── CardNone.vue
       │  ├── Grid
       │  │  ├── GridCol.vue
       │  │  └── GridRow.vue
       │  ├── List
       │  │  ├── ListGroup.vue
       │  │  ├── ListItem.vue
       │  │  ├── ListLink.vue
       │  │  └── ListNone.vue
       │  ├── Loading
       │  │  ├── LoadingDiv.vue
       │  │  ├── LoadingFloat.vue
       │  │  ├── LoadingLi.vue
       │  │  └── LoadingTr.vue
       │  ├── Search
       │  │  └── SearchBar.vue
       │  ├── Share
       │  │  ├── ShareEmail.vue
       │  │  ├── ShareFacebook.vue
       │  │  ├── ShareKakao.vue
       │  │  ├── ShareNaver.vue
       │  │  ├── ShareTwiter.vue
       │  │  └── ShareUrl.vue
       │  ├── Swiper
       │  │  ├── SwiperAuto.vue
       │  │  ├── SwiperCentered.vue
       │  │  ├── SwiperCenteredauto.vue
       │  │  ├── SwiperCustom.vue
       │  │  ├── SwiperDefault.vue
       │  │  ├── SwiperDynamic.vue
       │  │  ├── SwiperFraction.vue
       │  │  ├── SwiperFreemode.vue
       │  │  ├── SwiperMultiple.vue
       │  │  ├── SwiperNavigation.vue
       │  │  ├── SwiperPagination.vue
       │  │  ├── SwiperProgress.vue
       │  │  ├── SwiperScrollbar.vue
       │  │  ├── SwiperSpace.vue
       │  │  └── SwiperVertical.vue
       │  └── Table
       │     ├── TableNone.vue
       │     ├── TableTbody.vue
       │     ├── TableTD.vue
       │     ├── TableTH.vue
       │     ├── TableThead.vue
       │     ├── TableTR.vue
       │     └── TableWrap.vue
       ├── assets                기타 지원
       │  ├── images
       │  ├── scss
       │  └── videos
       └── api                   api 함수
          └── index.js
 ```