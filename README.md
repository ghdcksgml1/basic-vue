# Vue-js

## 🧤 Vue instance 생성

```html
<div id="app">{{ name }}</div>
<script>
  new Vue({
    el: "#app",
    data: {
      name: "코지 코더",
    },
  });
</script>
```

<br/><br/>

## 🧤 데이터 양방향 바인딩

데이터 양방향 바인딩이란? 말그대로 데이터가 들어올때 양쪽에 바인딩 시켜주는 것이다.

```html
<input type="text" :value="text @keyup="updateText"><br />
{{ text }}
<script>
  new Vue({
      data:{
          text:'text'
      },
      methods:{
          updateText(event){
              this.text = event.target.value;
          }
      }
  }
</script>
```

원래는 위와같이 써줘야하지만, 줄여서 아래와 같이 써줄수도 있다.

```html
<input type="text" v-model="text" /><br />
{{ text }}
<script>
  new Vue({
      data:{
          text:'text'
      }
  }
</script>
```
