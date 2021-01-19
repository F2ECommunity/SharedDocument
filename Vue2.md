
Vue2
===
###### tags:`前端(frontend)`,`框架`,`Vue2`,`問題集`
# 生命週期 life circle
![lifecircle](https://vuejs.org/images/lifecycle.png) 
## beforeCreate
Vue組件初始化
## created
組件按照inject所指定方法，引入父層級組件provider提供的方法，並且開始觀察變數是否有改變。
## beforeMount
在組件掛載之前會先檢查是否有使用**el選擇器**(註1)，如果有則會去檢查是否有template要掛載在特定tagName。
==一般都會在這時期向後端請求資料==或者 ==使用methods或者computed== 去做自己想要做的事，例如setinterval或addEventListener之類的方法...等等

註1.在main.js中，這段程式碼很明顯就是黃色區塊。
```javascript=
new Vue({
  render: h => h(App)
}).$mount("#app");
```
Vue類別沒有提供el屬性，將會執行 $mount("#app") 把app組件裡的template掛載到\<div id="app">\</div>下。
![](https://i.imgur.com/xHMewfV.png)


## mounted
這時期template已經掛載進父組件下了，並且監聽資料綁訂的data或watch的變數是否有改變。
若有改變的話將會進入beforeUpdate，沒有改變則等待進入beforeDestroy
## beforeUpdate
在資料變更之前將會呼叫這方法執行組件要做的事。
## Updated
在資料變更後，重新渲染(rerender)呼叫這Updated執行組件要做的事。
## beforeDestroy
記得如果之前有使用setInterval或addEventListener請在這時候移除
## destroyed
這時期組件會銷毀值捯下次再度被呼叫使用在重新進入beforeCreate
# Component
## 基本組件&額外提供的方法
```javascript=
 <template>
     <div>{{helloWorld}}</div>
 </template>
 <style lang="scss">
     div{
         background-color:#111;
     }
 </style>
 <script>
 export default{
     name:"HelloWorld",
     data:function(){
         return ({
             helloWorld:"HelloWorld"
         })
     }
 }
 </script>
```
## 渲染函式
```javascript=
 <template>
     <hello-user :name="userName"/>
 </template>
 <script>
 import Vue from "vue";
 const HelloUser = Vue.component("HelloUser",{
     props:["name"]
     template:`
         <span>{{name}}</span>
     `,
 })
 export default{
     components:{
         HelloUser
     },
     data:function(){
         return ({
             userName:"Jessica"
         })
     },
    //提供的方法與上面相同
 }
 </script>
```
```javascript=
 import Vue from "vue";
 const HelloUser = Vue.component("HelloUser",{
     props:["name"],
     data:function(){
         return ({})
     },
     render(h){
         return h(h1,'Hello'+this.name)
     }
     //提供的方法與上面相同
 });
 export default{
     components:{
         HelloUser
     }
 }
```
## 狀態組件
狀態組件分成 ==**有狀態組件(Stateful Component)**== 與 ==**無狀態組件(Stateless Component)**==
一般專案資料夾建立時會把**有狀態組件**放在containers資料夾裡，**無狀態組件**則是放在components資料夾
那麼我們來看這兩個組件的定義吧!
#### 有狀態組件(Stateful Component)
1. data裡有狀態
2. 不只接收來自props的外來參數
3. 組件內有computed或methods
#### 無狀態組件(Stateless Component)
1. data裡沒有任何狀態
2. 只接收來自props的外來參數
3. 組件內沒有任何computed或methods

通常有狀態組件會傳遞給無狀態組件參數以及狀態，就像是老鳥叫菜逼八做事一樣的道理，而菜鳥好處就是不斷的被利用(無誤
<iframe src="https://codesandbox.io/embed/affectionate-heisenberg-fc4jc?fontsize=14&hidenavigation=1&module=%2Fsrc%2FApp.vue&theme=dark&view=editor"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="affectionate-heisenberg-fc4jc"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>
   
# \<template>\</template>
## slots(插槽)
大部分有開始與結尾的<tagName></tagName>都可以放入<slot></slot>或<slot/>標籤作為組件預設的插槽
### 預設
<iframe src="https://codesandbox.io/embed/slot-default-50po8?fontsize=14&hidenavigation=1&module=%2Fsrc%2FApp.vue&theme=dark&view=editor"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="slot-default"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>
   
### 命名插槽

### 插槽資料傳遞
## v-if
## v-show
## v-for
<iframe src="https://codesandbox.io/embed/agitated-poitras-675w7?fontsize=14&hidenavigation=1&module=%2Fsrc%2FApp.vue&theme=dark&view=editor"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="agitated-poitras-675w7"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

#### 應用
* 無限下拉選單-待施工

## v-on
### 自訂義事件

## 資料雙向綁訂
### v-on:input與v-bind:value
### v-model

# \<style>\</style>
```javascript=
<style lang="scss" scoped>
     div{
         background-color:#111;
     }
</style>
```
## lang
## scoped

# \<script>\</script>
```javascript=
 <script>
 export default{
     name:"HelloWorld",//組件名稱
     extend: ,//繼承單一組件提供的props、methods...等等
     minxin:[],//混合複數組件提供的props、methods...等等
     porps:{//該組件需引入的屬性
     
     },
     data:function(){//該組件內部預設的狀態
         return ({
             helloWorld:"HelloWorld"
         })
     },
     provider:{//向下提供多個子組件變數
         
     },
     inject:[//注入不同父組件提供的變數
     
     ],
     components:{//掛載其他組件至該組件下面
         
     },
     computed:{
         
     },
     methods:{//該組件提供的方法
     
     },
     watch:{//組件需要手動監聽props
     
     },
 }
 </script>
```
## name
## extend
## mixin
## data
## components
## props
## computed
## methods
## watch
```javascript=
<script>
export default{
    props:{
        name:{
            type: String,
            default: "Jessica"
        }
    }
    watch:{
        name:{//觀察props裡面的name
            immediate: false,
            deep: false,
            handler:function(newValue,oldValue){
        
            }
        }
    }
}        
</script>
```
### 提供的屬性
**immdiate** 當組件beforeCreate初始化時觀察指定的變數是否有變動，如有變動則會呼叫handler
**deep**     當觀察的值是Object時會通知
**handler**  每當資料變動時會呼叫函式，提供了變更前與變更後的值
### 使用方式
#### props
```javascript=
<script>
export default{
    props:{
        name:{
            type: String,
            default: "Jessica"
        }
    }
    watch:{
        name:{
            immediate: true,
            handler:function(newValue,oldValue){
        
            }
        }
    }
}        
</script>
```
#### data
```javascript=
<script>
export default{
    data:function(){
        return({
            name:"Jessica"
        })
    }
    watch:{
        name:{
            handler:function(newValue,oldValue){
        
            }
        }
    }
}
</script>
```
#### Object裡的值
```javascript=
<script>
export default{
    data:function(){
        return({
            user:{
                name:"Jessica",
                height: 163
            }
        })
    }
    watch:{//對象為height時由於值的型態不是Object
        "user.height":{
            handler:function(newValue,oldValue){
        
            }
        },
        user:{//對象為Object
            deep:true
            handler:function(newValue,oldValue){
        
            }
        }
    }
}
</script>
```
#### Array
```javascript=
<script>
export default{
    data:function(){
        return({
            user:[
                {
                    name:"Jessica",
                    height: 163
                },{
                    name:"John",
                    height: 176
                }
            ]
        })
    }
    watch:{
        "user.height":{
            deep:true,
            handler:function(newValue,oldValue){
        
            }
        }
    }
}
</script>
```

# 第三方套件
[awesome-vue](https://github.com/vuejs/awesome-vue)
# Q&A

