<template>
  <div class="hello">
    <div class="container">1</div>
    <div class="container2">2</div>
    <div class="container3">3</div>
    <div class="container4">3</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
// less
@color1: red;
@width:100%;
@height:100px;
.border-radius(@radius){
  -webkit-border-radius:@radius;
  -moz-border-radius:@radius;
  border-radius: @radius;
}

.border_common{
  border: 1px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  height: @height;
}
.mixin(@color: black; @margin: 10px; @padding: 20px) {
  color: @color;
  margin: @margin;
  padding: @padding;
}
.box-shadow(@x: 0; @y: 0; @blur: 1px; @color: #000) {
  -webkit-box-shadow: @arguments;
     -moz-box-shadow: @arguments;
          box-shadow: @arguments;
}
.hello {
    border: 1px double #666666;
    padding:10px;
    .border-radius(10px);
    div {
      margin-top: 10px;
      .border-radius(10px);
      .border_common;
      .box-shadow(@x:10px,@y:10px);
    }
    .container{
      color: red;     
    }
    .container2{
      color: blue;
    }
    .container3{
      color: green;
    }
}

</style>
