# ๐ Vue.js ์์ํ๊ธฐ
## Vue.js ๋?
 > *์๋ฐ์คํฌ๋ฆฝํธ ํ๋ ์์ํฌ๋ก ๋ค๋ฅธ ํ๋ ์์ํฌ์ ๋นํด ์ ์ฐํ๊ณ  ๊ฐ๋ฒผ์ฐ๋ฉฐ ๋ผ์ฐํฐ(router)๋ฅผ ํ์ฉํด ๋จ์ผํ์ด์ง ์ ํ๋ฆฌ์ผ์ด์ ์ํคํ์ณ๊ตฌ์ฑ์ ํจ๊ณผ์ ์ด๋ค.*

### ๊ฐ๋ฐ ํ๊ฒฝ์ค์ 
 - Node.js
 - npm : Node Package Manager
 - Chrome Vue.js devtools : Chrome ๋ธ๋ผ์ฐ์  ๊ธฐ๋ฐ์์ ์๋ํ๋ Vue.js์ ์ฉ ๋๋ฒ๊น, ๊ฐ๋ฐ๋๊ตฌ
   - <a href="https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=ko">Vue.js devtools ์ค์น</a>
 - Vue-CLI : ์ฑ ์์ฑ์ ๊ธฐ๋ณธํ ์ ๊ณต
  
## โ Vue.js์ `LifeCycle`
<!-- > <img src="https://kr.vuejs.org/images/lifecycle.png"> -->
> <img src="https://gblobscdn.gitbook.com/assets%2F-M26jG1xuJ_y_q6GUJdp%2F-M26n5U2kzzz42LMgqau%2F-M26n8a_2P3mYmOeE2im%2FScreen-Shot-2019-01-14-at-12.44.09-AM.png?alt=media">
<br>

### Vue Template
> *Vue.js๋ ๋ ๋๋ง ๋ DOM์ ๊ธฐ๋ณธ Vue์ธ์คํด์ค์ ๋ฐ์ดํฐ์ ์ ์ธ์ ์ผ๋ก ๋ฐ์ธ๋ฉํ  ์ ์๋ HTML๊ธฐ๋ฐ ํํ๋ฆฟ ๊ตฌ๋ฌธ์ ์ฌ์ฉํ๋ค.<br>๊ฐ ํ์ด์ง๋ง๋ค HTML์ฝ๋์ Component๊ฐ ๋ค์ด๊ฐ๋ ์์น์ด๋ค.*

### Component
> *์ปดํฌ๋ํธ๋ Vue์์ ๊ฐ์ฅ ์ค์ํ ๊ธฐ๋ฅ์ผ๋ก HTML ์๋ฆฌ๋จผํธ๋ฅผ ํ์ฅํ์ฌ ์ฌ์ฌ์ฉ ๊ฐ๋ฅํ ์ฝ๋๋ฅผ ***์บก์ํ*** ํ๋ ๊ธฐ๋ฅ์ผ๋ก HTML Tag์ ๊ฐ์ ํํ๋ฅผ ๊ฐ๊ณ ์์ด ํผ๋ํ  ์ ์๋ค.<br>์ฌ์ฉํ  Component๋ฅผ importํด์ค๋ค๋ฉด ๋ก์ปฌ์ ์ด๋๊ณณ์์๋  ์ฌ์ฉ ๊ฐ๋ฅํ๋ค.<br>ex) Home.vue - `<LoadingDiv></LoadingDiv>`*
### vue-router
> *์ ํ๋ฆฌ์ผ์ด์์์ ์ฌ์ฉ์๊ฐ ์์ฒญํ URI ๊ฒฝ๋ก์ ๋ฐ๋ผ ๊ฐ๊ฐ ๋ค๋ฅธ ํ๋ฉด์ด ๋ ๋๋ง๋๊ณ  `SPA(Single Page Application)`๋ฅผ ์์ฝ๊ฒ ๋ง๋ค ์ ์๋๋ก ํจ.*
 - ์ค์ฒฉ๋ ๊ฒฝ๋ก, ๋ทฐ๋ฅผ ๋งคํํ  ์ ์๋ค.
 - ์ปดํฌ๋ํธ ๊ธฐ๋ฐ์ ๋ผ์ฐํ์ ๊ตฌํํ  ์ ์๋ค.
 - Vue.js์ ์ ํํจ๊ณผ๋ฅผ ์ ์ฉํ  ์ ์๋ค.
 - History Mode์ Hash Mode๋ฅผ ๋ชจ๋ ์ฌ์ฉํ  ์ ์๋ค.
 - queryString, Parameter, WildCard๋ฅผ ์ฌ์ฉํ์ฌ ๋ผ์ฐํ์ ๊ตฌํํ  ์ ์๋ค.
  
import๊ตฌ๋ฌธ์ ์ด์ฉํด vue-router๋ฅผ ์ฐธ์กฐํ๊ณ  ์ปดํฌ๋ํธ๋ฅผ ๋งคํํ ๋ผ์ฐํฐ ๊ฐ์ฒด๋ฅผ ์ธ์คํด์ค ๋ง๋ค๋ ์ง์ .
ํํ๋ฆฟ์์ `<router-link></router-link>`๋ก ํ์ดํผ๋งํฌ ์์ฑ ํ URI๊ฒฝ๋ก์ ๋ฐ๋ผ router ๊ฐ์ฒด์์ ๋งคํํ ์ปดํฌ๋ํธ๊ฐ `<router-view></router-view>`์ ๋ํ๋๊ฒ ๋จ.
 - **Base-Vue์์๋ Header์ Navigation๊ธฐ๋ฅ์์ ์ฌ์ฉํ๊ณ  ์๋ค. <br>/router/index.js๋ฅผ ๋ณด๋ฉด 2Depth ๊ธฐ๋ฅ์ ์ฌ์ฉํ๊ธฐ ์ํ์ฌ route ์ ์ธํด์ค ๋ children์ ์ฌ์ฉํจ.**
> *โ ๏ธ `vue-router`๋ฅผ ์ฌ์ฉํ๊ธฐ ์ํด์๋ `main.js`์์ import๊ตฌ๋ฌธ์ ์ด์ฉํด ์ฐธ์กฐํ๊ณ  router๋ฅผ ์ฌ์ฉํ ์ ์๋๋ก ์ ์ธ ํด์ค์ผํ๋ค.*

### .vueํ์ผ์์ script์์ฑ
> `<template></template>`ํ๋จ์ `<script></script>`๋ฅผ ๋ง๋ค์ด์ค๋ค.
> ```javascript
> <script>
> export default {
>   data() {
> 
>   }
> }
> </script>
> ```
> ์คํฌ๋ฆฝํธ๋ฅผ ์์ฑ ํ  ๋ `methods: {}`์ ํจ์ ๋ง๋ค์ด์ฃผ๊ณ  `LifeCycle`์ ๋ง๊ฒ ํจ์ ํธ์ถ๊ตฌ๋ฌธ ๋ง๋ค์ด์ฃผ๋ฉด ์ฌ์ฉ๊ฐ๋ฅํ๋ค.

### axios
> *HTTP ์์ฒญ์ ์ํ ํด๋ผ์ด์ธํธ๋ก API์์ฒญํ  ๋ ์ค๊ฐ ์ญํ ์ ํ๋ค.*
> axios Package๋ฅผ ํฐ๋ฏธ๋์ ํตํด ์ค์นํ๊ณ  `main.js`์์ import๊ตฌ๋ฌธ์ ํตํด ์ฌ์ฉํ  ์ ์๋๋ก ํด์ค๋ค.<br>base-vue์์๋ `/api/index.js`์์ ๊ฐ๊ฐ ์ํ๋ API๋ฐ์ดํฐ๋ฅผ ์ฌ์ฉํ๊ธฐ ์ํด ํจ์ํ ํด์ค. 

### Vuex Store(์ํ๊ด๋ฆฌ)
> *์์ `axios`๋ฅผ ํตํด API ๋ฐ์ดํฐ๋ฅผ ํธ์ถ ํ๋ค๋ฉด ํธ์ถํ ๋ฐ์ดํฐ๋ฅผ ์ ์ฅํ  ๊ณต๊ฐ์ด ํ์ํ๋ค.<br>ํ์ํ ๋ ๋ง๋ค ํธ์ถํ  ์ ์์ง๋ง ํ์ด์ง ๋ก๋ฉ์๊ฐ์ด ๊ธธ์ด์ง๊ณ  ๊ณผ๋ถํ๊ฐ ์ผ์ด๋  ์ ์๊ธฐ๋๋ฌธ์ ์ ์ฅํ๊ณ  ๊ฐ์ ธ์ค๋ ๋ฐฉ์ ์ค `Vuex Store`๋ฐฉ์์ ํํ๊ฒ ๋จ.*

***Web Storage ์ข๋ฅ***
 - <p style="color:red">Vuex Store : Application์ ๋ํ ์ํ๊ด๋ฆฌ ํจํด</p>

    > 1. ํด๋น application์ ๋ชจ๋  ์ปดํฌ๋ํธ์๋ํ ์ค์ ์ง์ค์ ์ ์ฅ์ ์ญํ ์ ํจ.
    > 2. ์ ์ฅ์์์ ์ง์  ์ํ๋ฅผ ๋ณ๊ฒฝํ์ง ์๊ณ  ๋ฐ๋์ ๋ณ์ด(mutation)๋ฅผ ํตํด์๋ง ๋ณ๊ฒฝ.
 - Local Storage / Session Storage
    > 1. key์ valueํํ๋ก ์ด๋ฃจ์ด์ง.
    > 2. ๊ฐ์ฒด ์ ๋ณด๋ฅผ ์ ์ฅ ํ  ์ ์๋ค.
    > 3. ์๊ตฌ์ ์ผ๋ก ๋ฐ์ดํฐ๋ฅผ ์ ์ฅ ํ  ์ ์๋ค.
    > 4. Session Storage๋ ์ธ์ ์ข๋ฃ์ ํด๋ผ์ด์ธํธ์ ๋ํ ์ ๋ณด๋ฅผ ์ญ์ ํ๋ค.
 - Cookie
    > 1. ๋งค๋ฒ ์๋ฒ๋ก ์ ์ก ๋๋ค.(์๋ฒ์ ๋ถ๋ด์ด ๋๋ค)
    > 2. ๋ง๋ฃ์ผ์๋ฅผ ์ง์ ํด์ ์ํ๋ ๊ธฐ๊ฐ๋งํผ ๋ฐ์ดํฐ๋ฅผ ์ ์ฅํ  ์ ์๋ค.
    > 3. ์ํธํ๊ฐ ์กด์ฌํ์ง ์์ ๋ณด์์ฑ์ด ์ทจ์ฝํ๋ค.


#### Vuex store๋ก API data๋ฅผ ์ ์ฅํ๊ณ  ํ์ํ  ๋ ์ ์ฅ๋ ๋ฐ์ดํฐ ์ฌ์ฉ ๊ฐ๋ฅ
<img src="https://blog.martinwork.co.kr/images/vue/vuex-state-one-way-data-flow.png">

 > *์ฌ์ฉ์(Component)๊ฐ `Action`์ ์ทจํ์ ๋  `Actions`๋ ์ธ๋ถ API๋ฅผ ํธ์ถํ๊ณ  `Mutations`(๋ณ์ด)์ ํตํด `State`๋ฅผ ๋ณ๊ฒฝํ๋ค. `State`์ ๊ฐ์ด ๋ณ๊ฒฝ๋๋ฉด ํด๋น ์ปดํฌ๋ํธ๊ฐ ๋ค์ ๋ก๋ฉ.*
 - `state` : ์ํ(๋ฐ์ดํฐ๊ฐ ๋ค์ด๊ฐ๋ ๊ณณ)
 - `mutation` : ๋ณ์ด(๋ฐ์ดํฐ๊ฐ ์ค์ ๋ก ๋ณ๊ฒฝ๋๋ ๊ณณ_๊ท์ฝ)
 - `action` : ํจ์๊ฐ ๋ค์ด๊ฐ๋ ๊ณณ(๋น๋๊ธฐ์  ์ฒ๋ฆฌ)
  
***์ฌ์ฉ ํ  ๋๋ ํด๋น ํ์ด์ง์์ `dispatch`ํด์ผ ์ฌ์ฉ ๊ฐ๋ฅํจ***

## ๐ฒ Base-Vue์ ๊ธฐ๋ณธ ํ๋ฉด ๊ตฌ์ฑ
 > ### ***Component -> Template -> Page(Layout)***

### Home.vue
 >
## ๐ Clone Project
 ### 1๏ธโฃ Node.js Version ํ์ธ
  - #### `cmd`์ฐฝ์์ `$ node --version`
  - #### ***์ค์น๋ Node.js Version์ด 14.17.0์ด ์๋๋ผ๋ฉด..***
    - `$ nvm list` : ํ์ฌ ์ค์น๋ Node.js Version ํ์ธ
    - `$ nvm install 14.17.0` : Ver.14.17.0 ์ค์น
    - `$ nvm list` : ๋ค์ PC์ ์ค์น๋ Node.js ํ์ธ(Ver.14.17.0์ด ์ค์น๋๊ฒ์ ํ์ธํ  ์ ์๋ค)
    - `$ nvm use 14.17.0` : 14.17.0 Version์ผ๋ก Node.js ๋ณ๊ฒฝ
    - `$ node --version` : ํ์ฌ ์ฌ์ฉ์ค์ธ Version์ ํ์ธํ์ฌ ์ ๋๋ก ๋ณ๊ฒฝ ๋์๋์ง Check
    - *์ฐธ๊ณ ) <a id="node-version-change" nameid="node-version-change" href="https://node-js.tistory.com/entry/Nodejs-nvm%EC%9C%BC%EB%A1%9C-%EC%89%BD%EA%B2%8C-Node-%EB%B2%84%EC%A0%84%EB%B3%80%EA%B2%BD%ED%95%98%EA%B8%B0">Node Version ๋ณ๊ฒฝํ๊ธฐ</a>*
 ### 2๏ธโฃ GitLab์์ Project Clone ํ๊ธฐ
 <!-- - #### `$ git clone https://gitlab.com/bstones-feteam/base-vue.git` -->
  - #### *VSCode๋ก ๋ฐ๋ก ์ด์์ ๊ฒฝ์ฐ๋ git์ผ๋ก Cloneํ์ ๊ฒฝ์ฐ*
    - VSCode์์ ํฐ๋ฏธ๋์ฐฝ ์ง์ or `cmd` ์ง์ํ์ฌ ํด๋น ํ๋ก์ ํธ ํด๋๋ก ์ด๋
  #### `$ npm install`
  - #### *`npm install`์ Project์์ ์ฌ์ฉ๋ Module(Package)์ด ์๋์ผ๋ก ์ค์น*
   > *์ฌ๋ฌ ์ฌ๋๊ณผ ํจ๊ป ์์์ ์งํํ  ๋๋ `pull`๋ฐ๊ณ  ๋์ `npm install`๋ฅผ ํด์ผ ์ถ๊ฐ๋ก Package๊ฐ ์ฌ์ฉ ๋์์ ๋ ์ ์์ ์ผ๋ก ์คํ ํ  ์ ์๋ค.<br>โ ๏ธ `npm update`๋ Package๋ฅผ ์ต์  Version์ผ๋ก ์ค์นํด์ฃผ๋ ๋ช๋ น์ด ์ด๋ฏ๋ก Version์ ์ง์ ํด์ ์ค์นํ Package๊ฐ ์์ ์ ์์ผ๋ `npm install`์ ํด์ฃผ๋ ๊ฒ์ด ์ข๋ค.*

 ### 3๏ธโฃ `base-vue` Project ์คํ ๋ฐฉ๋ฒ
  - #### `npm update` ๊ฐ ์๋ฃ๋ ํ  `npm run serve` ์๋ ฅ
  - #### http://localhost:8080/ ์ ์
<br>

## ๐ Vue.js Project ๋ง๋ค๊ธฐ
### 1๏ธโฃ `vue-cli` ์ค์น
 - #### `cmd`์ฐฝ์์ `$ npm install @vue/cli -g`
### 2๏ธโฃ ํ๋ก์ ํธ ์์ฑ
- #### `$ vue create ํ๋ก์ ํธ๋ช`
  โ ๏ธ ***create ํ  ๋ ์์๋๋ก ์ ํ***
  - Manually select features
  - Choose Vue Version , Babel , Router , Vuex , CSS Pre-processors , Linter/Formatter
    - `space bar`๋๋ฌ์ ์ ํ
  - 2.x
  - Yes
  - Sass/SCSS (with node-sass)
  - ESLint with error prevention only
  - Lint on save
  - In dedicated config files
  - No

*์ ๋ฐฉ์์ผ๋ก ํ๋ก์ ํธ๋ฅผ ๋ง๋ค์๋ค๋ฉด ๊ธฐ๋ณธ์ผ๋ก `core-js`, `vue`, `vue-router`, `vuex`  Package ์ค์น๋์ด ์์*
<br>

### 3๏ธโฃ ํ๋ก์ ํธ์ ํ์ํ ํจํค์ง ์ค์น 
#### - **๐ Base-Vue์์ ํ์ํ ํจํค์ง**
```
  npm i bootstrap popper.js/core jquery vue-frag axios swiper vue-awesome-swiper vuejs-paginate query-string vue-meta vue2-editor quill material-icons fullcalendar date-fns jquery-ui-dist aos vue-masonry vue-masonry-css
```

| Package Name | Meaning |
|:---:|---|
| **โญ๏ธ `bootstrap`** | bootstrap์ css๋ฅผ ์ฌ์ฉํ๊ธฐ ์ํด ์ฌ์ฉ |
| **โญ๏ธ `popper.js/core`** | Bootstrap๊ด๋ จํด์ ToolTip์ ๋ณด์ฌ์ฃผ๋ Package |
| **โญ๏ธ `jquery`** | jquery๋ฅผ ์ฌ์ฉํ๊ธฐ ์ํ package <br>*( vue.config.js ํ์ผ์ ๋ฐ๋ก ๋ง๋ค์ด์ jquery๋ฅผ ์ ์ญ์์ ์ฌ์ฉํ  ์ ์๋๋ก ํด์ค์ผํ๋ค. )* |
| **โญ๏ธ `vue-frag`** | `<template>`์์ div๋ก ๊ฐ์ธ์ผ ํ๋๋ฐ `vue-frag` package์ฌ์ฉ | ํ `<div v-frag></div>`๋ก ๊ฐ์ธ์ฃผ๋ฉด ์ค์  html์์๋ ์๋ณด์ด๊ฒ ๋ง๋ค์ด์ง. |
| **โญ๏ธ `axios`** | data๋ฅผ ์์ฒญํ  ๋ ์ค๊ฐ์ญํ ์ ํ๋ค. |
| **`swiper`** | swiper๊ธฐ๋ฅ ์ฌ์ฉ์ ํ์ css |
| **`vue-awesome-swiper`** | `component`๋ก ๋ง๋ค์ด์ฃผ๋ ์ญํ (`swiper`์ ์ธํธ) |
| **โญ๏ธ `vuejs-paginate`** | Pagination์ ์ํ Package๋ก CSS๋ก ์คํ์ผ ์ง์ ์ด ๊ฐ๋ฅ |
| **`query-string`** | URL ์ฟผ๋ฆฌ ๋ฌธ์์ด ๊ตฌ๋ฌธ ๋ถ์ ๋ฐ ๋ฌธ์์ด ํ |
| **`vue-meta`** | meta Tag์ฌ์ฉ์ ์ํ Package |
| **`vue2-editor`** | ๊ฒ์ํ์ ์๋ํฐ๋ฅผ ์ฌ์ฉํ๊ธฐ ์ํ Text Editor Package |
| **`quill`** | Editor CSS ๋ณ๊ฒฝ์ ์ํ Package |
| **`material-icons`** | material icon์ ์ฌ์ฉํ๊ธฐ ์ํ Package |
| **`fullcalendar`** | Calendar ๊ด๋ จ Package |
| **`date-fns`** | date format ๋ณ๊ฒฝ์ ์ํ Package |
| **`jquery-ui-dist`** | jquery ui ์์ ์ด๋ฒคํธ ๋ฑ๋ก์ ๋ ์ง Form์ฌ์ฉํ๊ธฐ ์ํ Package |
| **`aos`** | Animation On Scroll ์คํฌ๋กค ์ ๋๋ฉ์ด์ Package(https://michalsnik.github.io/aos/) |
| **`vue-masonry`** | masonry layout(ํํฐ๋ ์คํธ ํ์) ์๋ ์ค๋ง์ถค ํด์ฃผ๋ Package |
| **`vue-masonry-css`** | ์ `vue-masonry`๋ฅผ ์ฌ์ฉํ ๋๋ ๊ตฌ์ญ์ ๋ฏธ๋ฆฌ ์ ํด ๋๊ธฐ ๋๋ฌธ์ Pagination์ ์ฌ์ฉํ ๋๋ ๊ฐ๊ฒฉ์กฐ์  ํ๊ธฐ๊ฐ ์ฝ์ง ์๋ค. ์ด๋ฅผ ๋ณด์ํ๊ธฐ ์ํด ์ฌ์ฉํ๋ Package |

- #### ๐ jquery์ฌ์ฉ
  ***jquery์ฌ์ฉ์ ์ํด ํ๋ก์ ํธ ๋ก์ปฌ ๊ฒฝ๋ก์ `vue.config.js`ํ์ผ ์์ฑ***

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
  ***์ถ๊ฐ ํด์ค๋ค ํ๋ก์ ํธ ๋ก์ปฌ์ ์์ฑ๋์ด์๋ `.eslintrc.js`ํ์ผ์ ์๋ ์ฝ๋ ์ถ๊ฐ***
   ```javascript
   module.exports = {
    root: true,
    env: {
      // ์ถ๊ฐํด์ค๋ค
      node: true,
      jquery: true
    },
    ```
<br>

### 4๏ธโฃ `main.js` ํ์ฉ ํ๊ธฐ
  - ***`main.js`์์๋ Package๋ script, css ๋ฑ ์ ์ญ์ผ๋ก ์ฌ์ฉํ  ํญ๋ชฉ๋ค์ ์ ์ธ ํด์ค๋ค.***
    ***์๋ฅผ ๋ค์ด ์๋ ํจ์์ฒ๋ผ ์์ฃผ ์ฌ์ฉํ  ํจ์๋ฅผ ๋ฑ๋กํด์ฃผ๋ฉด pluginํ ํด์ app์ ์ฒด์์ `$scrollToTop`์ ์ฌ์ฉํ  ์ ์๋ค.***
    ```javascript
    // plugin
    const plugins = {
      install() {
        Vue.prototype.$scrollToTop = () => window.scrollTo(0, 0);
      }
    }
    ```

 -  ***๐ main.js์์ ์ ์ญ์์ ์ฌ์ฉ๊ฐ๋ฅํ plugin์ ๋ง๋ค ์ ์๋ค.(utill, api, axios ๋ฑ) ํ์ํ ๋๋ง๋ค `.vue`ํ์ผ์์ ์ ์ธํด์ฃผ๋๊ฒ ์๋๋ผ main.js์ ์ ์ธ๋์ด ์๋๊ฒ์ ๊ฐ์ ธ๋ค ์ด๋ค.***
<br>

`Home.vue`์์ Api๋ฅผ ์ฌ์ฉํ ๋ `<script>`๋ด์ `method: {}`์์ Api ํธ์ถํจ์ ์ฌ์ฉ.
 > ```javascript
 > methods: {
 >    callGetAlbum() {
 >      this.$api                 //$api๋ main.js์์ ๋ง๋  Plugin
 >        .getAlbum()             //api > index.js์์ ๋ง๋  ํจ์
 >        .then((response) => {   //getAlbum()์ ํธ์ถํ๊ณ  ๋ ๋ค์ ์คํ
 >          this.dataDummy = response.data; 
 >       // getAlbum()์ ๋ฆฌํด๊ฐ์ (LocalStorage์ dataDummy๊ฐ) response.data์ ์ ์ฅ
 >          this.$utils.setLocalStore("dataDummy", response.data);  
 >       // main.js์์ ๋ง๋ค์ด์ง $utill์์ setLocalStore()ํจ์์ 
 >       // key๊ฐ๊ณผ value๊ฐ์ ๊ฐ๊ฐ "dataDummy"์ response.data๋ฅผ ๋ฃ์ด์ค๋ค.
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

#### ๐ *`router > index.js`์์ 2-Depth ๋ฉ๋ด๋ฅผ ๋ง๋ค ๋ `children`์ ์ฌ์ฉํ์ฌ ๋ง๋ ๋ค.<br>1-Depth๋ 2-Depth์ ์ฒซ๋ฒ์งธ ํญ๋ชฉ์ ๊ฐ์ ธ์์ผ ํ๋ค๋ฉด `redirect`๋ฅผ ์ฌ์ฉํ์ฌ 2-Depth์ ์ฒซ๋ฒ์งธ ํญ๋ชฉ์ path๊ฐ์ ๊ฐ์ ธ์ค๋๋ก ํ๋ค.*
>  ```javascript
>  path: "/hello",
> // path๋ฅผ "/hello"๋ก ์ง์ ํ์ง๋ง redirect ํ๊ธฐ ๋๋ฌธ์ 
> // 1-Depth์ธ "ํฌ๋ก์ฐ" ํด๋ฆญ ์ "/hello/violin" ์ผ๋ก ์ด๋ํ๊ฒ ๋จ.
>   redirect: '/hello/violin',
>   name: "hello",
>   component: Hello,
>  ```

#### โ ***`v-bind:class=" "` `v-bind:key=" "` ๋ ๋ฐ๋ณต์ ์ผ๋ก ์ฌ์ฉํ๋ ๋ถ๋ถ์ด ์๊ธฐ์ ํธ์์ฑ์ ์ํด `:class=" "` `:key=" "`์ ๊ฐ์ ํ์์ผ๋ก ์ฌ์ฉํ๋๊ฒ ์ข์ ๋ฏํจ.***

#### โ `script` ๋ฅผ ์์ฑํ๊ณ  ์ถ์ ๋ `methods` ์์ ํจ์๋ฅผ ๋ง๋ค๊ณ  *[Life Cycle](#vue-lifecycle)* ์ ๋ง๊ฒ ํจ์๋ฅผ ํธ์ถํ๋ค.
<br>



### ๐ ์ปดํฌ๋ํธ์ ์ธ์คํด์ค ๋ฐ ์์์ ์ ๊ทผ
 - #### `ref`์์ฑ ์ฌ์ฉํ์ฌ ์์ ์์์ ๋ ํผ๋ฐ์ค ID๋ฅผ ํ ๋นํ  ์ ์๋ค.
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
 - ์์ ๊ฐ์ด ์ฌ์ฉํ๋ฉด `<TempBoardDelete>`์ ์ธ์คํด์ค ์์์ ์ ๊ทผ ๊ฐ๋ฅํจ.
> *`$refs` ๋ ์ปดํฌ๋ํธ๊ฐ ๋ ๋๋ง ๋ ํ์ ์ ๊ทผํ  ์ ์์ผ๋ฉฐ, ๋ฐ์ํ์ด ์๋. <br>์ฆ, ์ง์ ์ ์ธ ์์ ์์ ์ ์ด์๋ง ์ ํจํจ.<br> `$refs`๋ฅผ <a style="color:red">template </a>๋ <a style="color:red">computed ์์ฑ</a> ์์ ํฌํจ์ํค์ง ์๋ ๊ฒ์ด ์ข๋ค.*

 - #### `props`์์ฑ์ ์ปดํฌ๋ํธ๊ฐ์ ๋ฐ์ดํฐ๋ฅผ ์ ๋ฌํ  ์ ์๋ ํต์  ๋ฐฉ๋ฒ
   - ์์ ์ปดํฌ๋ํธ์์ ํ์ ์ปดํฌ๋ํธ๋ก ๋ด๋ณด๋ด๋ ค๋ ๋ฐ์ดํฐ ์์ฑ


## base-vue page Description
> base-vue๋ ์ฌ์ค ๋ก์ปฌ๊ฒฝ๋ก์ ์๋ App.vue๋ฅผ ๋ณด๊ณ  ์๋ ๊ฒ.<br>App.vue์์ ๋ด์ฉ์ ๋ณด๋ฉด `Accessibility`์ `Container`๋ผ๋ Component๋ฅผ import์์ผ ์ฌ์ฉํ๊ณ  ์๋ ๋ชจ์ต์ด๋ค.<br>`Container.vue`๋ฅผ ํ์ธํด๋ณด๋ฉด ๊ธฐ๋ณธ์ ์ธ HTML-layout์ธ Header-Main-Footer๋ก ๋๋ ์ ธ ์๋๊ฑธ ํ์ธ ํ  ์ ์๊ณ  ๋ง์ฐฌ๊ฐ์ง๋ก Component๋ก ์ฌ์ฉํ๋ค.

*Vue.js๋ ์ปดํฌ๋ํธ๋ค์ ์กฐํฉํด ์ ์ฒด ์ ํ๋ฆฌ์ผ์ด์์ ์์ฑํ๋ค. ์ปดํฌ๋ํธ๋ค์ ๋ถ๋ณด-์์ ๊ด๊ณ๋ก ํ์ฑ๋๋ฉฐ ์์ฑ(props)์ ํตํด ์์ ์ปดํฌ๋ํธ๋ก ์ ๋ณด๋ฅผ ์ ๋ฌํ  ์ ์๋ค.*
- <a href="http://selphy1.cafe24.com/basevue/">Home : </a>ํ์์ ๋ชจ๋๋ณ ์ต์ ๊ธ ๋ฐ ๊ณต์ง์ฌํญ๊ณผ ๋ฆฌ์คํธ ํ์์ ์ข์์์, ์กฐํ์์(์ธ๊ธฐ๊ธ) ํ์ธ
  - ํ์ด์ง ์ค๋ช
- ํฌ๋ก์ฐ
  - <a href="http://selphy1.cafe24.com/basevue/hello/static">์คํํฑ : </a>์ ์ ์ธ ์ปจํ์ธ ๋ฅผ ์ฌ๋ฌ ๋ฐฉ์(swiper, video, history)์ผ๋ก ํ์ฉ
  - <a href="http://selphy1.cafe24.com/basevue/hello/handling">ํธ๋ค๋ง : </a>์์ฃผ ์ฌ์ฉํ๋ ๊ฐ๋จํ ํธ๋ค๋ง ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/hello/slider">์ฌ๋ผ์ด๋ : </a>๋ค์ํ Swiper ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/hello/animation">์ ๋๋ฉ์ด์ : </a>AOS(Animation On Scroll) Lib๋ฅผ ํ์ฉํ ์คํฌ๋กค ์ ๋๋ฉ์ด์ ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/hello/location">๋ก์ผ์ด์ : </a>kakaomap API๋ฅผ ํ์ฉํ ์ง๋ ๊ธฐ๋ฅ ๊ตฌํ
- ๋ชจ๋1
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1table">ํ์ด๋ธ : </a>API data(๋์ ์ธ ๋ฐ์ดํฐ)๋ฅผ ํ์ด๋ธ ํํ๋ก ์ถ๋ ฅ ๋ฐ C.R.U.D ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1sort">์ ๋ ฌ : </a>ํ์ด๋ธ ํํ์ ๋ฆฌ์คํธ๋ฅผ ์ฌ๋ฌ ๋ฐฉ์์ผ๋ก ์ ๋ ฌ
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1perpage">ํผํ์ด์ง : </a>ํ์ด๋ธ ํํ์ ๋ฆฌ์คํธ์ ๊ฐฏ์๋ฅผ ์กฐ์ ํ๋ ๊ธฐ๋ฅ
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1search">๊ฒ์ : </a>ํ์ด๋ธ ํํ์ ์ปจํ์ธ ์ ๊ฒ์ ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/module1/m1category">์นดํ๊ณ ๋ฆฌ : </a>ํ์ด๋ธ ํํ์ ๋ฆฌ์คํธ๋ฅผ ์นดํ๊ณ ๋ฆฌ๋ณ ๋ถ๋ฅ
- ๋ชจ๋2
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2card">์นด๋ : </a>API data(๋์ ์ธ ๋ฐ์ดํฐ)๋ฅผ ์นด๋ ํํ๋ก ์ถ๋ ฅ ๋ฐ C.R.U.D ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2card">์ ๋ ฌ : </a>์นด๋ ํํ์ ๋ฆฌ์คํธ๋ฅผ ์ฌ๋ฌ ๋ฐฉ์์ผ๋ก ์ ๋ ฌ
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2perpage">ํผํ์ด์ง : </a>์นด๋ ํํ์ ๋ฆฌ์คํธ์ ๊ฐฏ์๋ฅผ ์กฐ์ ํ๋ ๊ธฐ๋ฅ
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2search">๊ฒ์ : </a>์นด๋ ํํ์ ์ปจํ์ธ ์ ๊ฒ์ ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/module2/m2category">์นดํ๊ณ ๋ฆฌ : </a>์นด๋ ํํ์ ๋ฆฌ์คํธ๋ฅผ ์นดํ๊ณ ๋ฆฌ๋ณ ๋ถ๋ฅ
- ๋ชจ๋3
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3more">๋๋ณด๊ธฐ : </a>๋์ ์ธ ์ปจํ์ธ ๋ฅผ ๋๋ณด๊ธฐ ๋ฒํผ์ ํตํด 5๊ฐ์ฉ ์ถ๊ฐ
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3infinite">๋ฌดํ์คํฌ๋กค : </a>์นด๋ํ์์ ๋์ ์ธ ๋ฐ์ดํฐ๋ฅผ ์คํฌ๋กค์ ๋ด๋ฆฌ๋ฉด ์๋์ผ๋ก ์ปจํ์ธ  ์ถ๊ฐ
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3masonry">Masonry : </a>๋์ ์ธ ๋ฐ์ดํฐ๋ฅผ ํํฐ๋ ์คํธ ๋ฐฉ์์์ Masonry ํจํค์ง๋ฅผ ์ฌ์ฉํ์ฌ ์๋์ผ๋ก ๋์ด ์กฐ์ ํ๋ ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3type">ํ์ : </a>๋์ ์ธ ๋ฐ์ดํฐ๋ฅผ ์ฌ๋ฌ ํ์์ผ๋ก ๋ณผ ์ ์๋ ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/module3/m3accord">์์ฝ๋์ธ : </a>๋์ ์ธ ๋ฐ์ดํฐ๋ฅผ ์์ฝ๋์ธ ๋ฐฉ์์ผ๋ก ์ถ๋ ฅ
- ๋ชจ๋4
  - <a href="http://selphy1.cafe24.com/basevue/module4/m4event">์ด๋ฒคํธ : </a>์ด๋ฒคํธ ํํ์ ๋์ ์ธ ๋ฐ์ดํฐ ์ถ๋ ฅ ๋ฐ ์ด๋ฒคํธ C.R.U.D ๊ธฐ๋ฅ ๊ตฌํ
  - <a href="http://selphy1.cafe24.com/basevue/module4/m4calendar">์บ๋ฆฐ๋ : </a>๋ฑ๋ก๋ ์ด๋ฒคํธ ๋ ์ง๋ฅผ calendar์ ์ถ๋ ฅ
  - <a href="http://selphy1.cafe24.com/basevue/module4/m4map">์ง๋ : </a>๋ฑ๋ก๋ ์ด๋ฒคํธ ์ฅ์๋ฅผ kakaomap API๋ฅผ ์ด์ฉํด ์ง๋์ ์ถ๋ ฅ
- ๋ชจ๋5
  - <a href="http://selphy1.cafe24.com/basevue/module5/m5share">๊ณต์  : </a>๊ฒ์ํ contents SNS ๊ณต์ ๊ธฐ๋ฅ ๊ตฌํ(facebook, twitter, naver, kakao, email, URL copy)
  - <a href="http://selphy1.cafe24.com/basevue/module5/m5comment">๋๊ธ : </a>๊ฒ์ํ ๋๊ธ ๊ธฐ๋ฅ ๊ตฌํ(๋๊ธ ์, ๋๊ธ๋ฑ๋ก, ์์ , ์ญ์ )
- ํ์
  - <a href="http://selphy1.cafe24.com/basevue/member/mypage">๋ง์ดํ์ด์ง : </a>๋ก๊ทธ์ธ์ ํ์ง ์์์๋ /login์ผ๋ก ์ด๋ํ๊ฒ ๋๊ณ  ๋ก๊ทธ์ธ์ ์นด์นด์ค๊ณ์ ์ผ๋ก ๋ก๊ทธ์ธ ๊ฐ๋ฅํ๋ฉฐ ๋ก๊ทธ์ธ์ ํ๊ณ ๋ ๋ค์๋ ๊ณ์  ์ ๋ณด๊ฐ ๋์จ๋ค.
  - <a href="http://selphy1.cafe24.com/basevue/member/login">๋ก๊ทธ์ธ : </a>์นด์นด์ค๊ณ์ ์ผ๋ก ๋ก๊ทธ์ธํ  ์ ์๋๋ก ๋ก๊ทธ์ธ ์ฐฝ์ด ๋์ด.
  - <a href="http://selphy1.cafe24.com/basevue/member/logout">๋ก๊ทธ์์ : </a>๋ก๊ทธ์ธ์ ํ๊ณ ๋๋ฉด ๋ก๊ทธ์ธ ํญ์ด ๋ก๊ทธ์์์ผ๋ก ๋ณ๊ฒฝ ๋๊ณ  ๋ก๊ทธ์์ํ Home์ผ๋ก ์ด๋๋จ.


***Base-Vue ํ๋ก์ ํธ ๊ตฌ์กฐ***
 ```bash
Base-vue
    โโโ vue.config.js
    โโโ README.md
    โโโ package.json
    โโโ package-lock.json
    โโโ jsconfig.json
    โโโ deploy.js
    โโโ babel.config.js
    โโโ .gitignore
    โโโ .eslintrc.js
    โโโ .browserslistrc
    โโโ src
       โโโ main.js
       โโโ App.vue
       โโโ utils                 ํํฐ ๋ฑ์ ์ ํธ๋ฆฌํฐ ํจ์
       โ  โโโ index.js
       โโโ templates             ํํ๋ฆฟ
       โ  โโโ TempCardLink.vue
       โโโ store                 ์ํ ๊ด๋ฆฌ
       โ  โโโ index.js
       โโโ settings              ๋๋ฉ์ธ, ์ฌ์ดํธ ์ ๋ณด
       โ  โโโ index.js
       โโโ router                ๋ผ์ฐํฐ
       โ  โโโ index.js
       โโโ pages                 ํ์ด์ง
       โ  โโโ Hello
       โ  โ  โโโ Animation.vue
       โ  โ  โโโ Handling.vue
       โ  โ  โโโ Hello.vue
       โ  โ  โโโ Location.vue
       โ  โ  โโโ Parallax.vue
       โ  โ  โโโ Slider.vue
       โ  โ  โโโ Static.vue
       โ  โโโ Member
       โ  โ  โโโ Auth.vue
       โ  โ  โโโ Login.vue
       โ  โ  โโโ Logout.vue
       โ  โ  โโโ Member.vue
       โ  โ  โโโ Mypage.vue
       โ  โโโ Module1
       โ  โ  โโโ M1Add.vue
       โ  โ  โโโ M1Category.vue
       โ  โ  โโโ M1Edit.vue
       โ  โ  โโโ M1Perpages.vue
       โ  โ  โโโ M1Search.vue
       โ  โ  โโโ M1Sort.vue
       โ  โ  โโโ M1Table.vue
       โ  โ  โโโ M1View.vue
       โ  โ  โโโ Module1.vue
       โ  โโโ Module2
       โ  โ  โโโ M2Add.vue
       โ  โ  โโโ M2Card.vue
       โ  โ  โโโ M2Category.vue
       โ  โ  โโโ M2Edit.vue
       โ  โ  โโโ M2Perpages.vue
       โ  โ  โโโ M2Search.vue
       โ  โ  โโโ M2Sort.vue
       โ  โ  โโโ M2View.vue
       โ  โ  โโโ Module2.vue
       โ  โโโ Module3
       โ  โ  โโโ M3Accord.vue
       โ  โ  โโโ M3Infinite.vue
       โ  โ  โโโ M3InfiniteView.vue
       โ  โ  โโโ M3Masonry.vue
       โ  โ  โโโ M3MasonryView.vue
       โ  โ  โโโ M3More.vue
       โ  โ  โโโ M3MoreView.vue
       โ  โ  โโโ M3Type.vue
       โ  โ  โโโ M3TypeView.vue
       โ  โ  โโโ Module3.vue
       โ  โโโ Module4
       โ  โ  โโโ M4Add.vue
       โ  โ  โโโ M4Calendar.vue
       โ  โ  โโโ M4Edit.vue
       โ  โ  โโโ M4Event.vue
       โ  โ  โโโ M4Map.vue
       โ  โ  โโโ M4View.vue
       โ  โ  โโโ Module4.vue
       โ  โโโ Module5
       โ  โ  โโโ M5Comment.vue
       โ  โ  โโโ M5CommentView.vue
       โ  โ  โโโ M5Share.vue
       โ  โ  โโโ M5ShareView.vue
       โ  โ  โโโ Module5.vue
       โ  โโโ Search
       โ  โ  โโโ Search.vue
       โ  โโโ Home.vue
       โ  โโโ NotFound.vue
       โโโ layouts               ํ์ด์ง ๋ ์ด์์
       โ  โโโ Accessibility.vue
       โ  โโโ Container.vue
       โ  โโโ Footer.vue
       โ  โโโ Header.vue
       โ  โโโ Main.vue
       โ  โโโ MainBottom.vue
       โ  โโโ MainBreadcrumb.vue
       โ  โโโ MainTop.vue
       โ  โโโ Navigation.vue
       โโโ components            ์ปดํฌ๋ํธ
       โ  โโโ Button
       โ  โ  โโโ ButtonAnchor.vue
       โ  โ  โโโ ButtonBasic.vue
       โ  โ  โโโ ButtonInput.vue
       โ  โ  โโโ ButtonLink.vue
       โ  โ  โโโ ButtonSubmit.vue
       โ  โ  โโโ ButtonWrap.vue
       โ  โโโ Card
       โ  โ  โโโ CardBody.vue
       โ  โ  โโโ CardFigure.vue
       โ  โ  โโโ CardFooter.vue
       โ  โ  โโโ CardGroup.vue
       โ  โ  โโโ CardLink.vue
       โ  โ  โโโ CardNone.vue
       โ  โโโ Grid
       โ  โ  โโโ GridCol.vue
       โ  โ  โโโ GridRow.vue
       โ  โโโ List
       โ  โ  โโโ ListGroup.vue
       โ  โ  โโโ ListItem.vue
       โ  โ  โโโ ListLink.vue
       โ  โ  โโโ ListNone.vue
       โ  โโโ Loading
       โ  โ  โโโ LoadingDiv.vue
       โ  โ  โโโ LoadingFloat.vue
       โ  โ  โโโ LoadingLi.vue
       โ  โ  โโโ LoadingTr.vue
       โ  โโโ Search
       โ  โ  โโโ SearchBar.vue
       โ  โโโ Share
       โ  โ  โโโ ShareEmail.vue
       โ  โ  โโโ ShareFacebook.vue
       โ  โ  โโโ ShareKakao.vue
       โ  โ  โโโ ShareNaver.vue
       โ  โ  โโโ ShareTwiter.vue
       โ  โ  โโโ ShareUrl.vue
       โ  โโโ Swiper
       โ  โ  โโโ SwiperAuto.vue
       โ  โ  โโโ SwiperCentered.vue
       โ  โ  โโโ SwiperCenteredauto.vue
       โ  โ  โโโ SwiperCustom.vue
       โ  โ  โโโ SwiperDefault.vue
       โ  โ  โโโ SwiperDynamic.vue
       โ  โ  โโโ SwiperFraction.vue
       โ  โ  โโโ SwiperFreemode.vue
       โ  โ  โโโ SwiperMultiple.vue
       โ  โ  โโโ SwiperNavigation.vue
       โ  โ  โโโ SwiperPagination.vue
       โ  โ  โโโ SwiperProgress.vue
       โ  โ  โโโ SwiperScrollbar.vue
       โ  โ  โโโ SwiperSpace.vue
       โ  โ  โโโ SwiperVertical.vue
       โ  โโโ Table
       โ     โโโ TableNone.vue
       โ     โโโ TableTbody.vue
       โ     โโโ TableTD.vue
       โ     โโโ TableTH.vue
       โ     โโโ TableThead.vue
       โ     โโโ TableTR.vue
       โ     โโโ TableWrap.vue
       โโโ assets                ๊ธฐํ ์ง์
       โ  โโโ images
       โ  โโโ scss
       โ  โโโ videos
       โโโ api                   api ํจ์
          โโโ index.js
 ```