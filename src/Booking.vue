<template>
  <div>
    <h1>訂購產品</h1>
    <form @submit.prevent="">
      <div>
        請點選表單填寫
      </div>
      <div>
        <p>==================</p>
        <p>匯款資訊:XXXXXXXX</p>
        <p>聯絡賣家:李先生 09xx-xxx-xxx</p>
      </div>
    </form>
  </div>
</template>

<script>
import courses from './courses';

export default {
  data(){
    return {
      name:'',
      tel: '',
      time: '',
      course: 1,
    };
  },
  computed:{
    courses(){
      return courses;
    },
  },
};
</script>

<style scoped>
  .group{
    display: flex;
    flex-flow: row nowrap;
    font-size: 12px;
    margin: 1em 0;
    align-items: center;
    justify-contents: center;
  }
  label{
    flex: 0 0 40px;
    text-align: right;
    padding-right: 10px;
  }
  input, select{
    flex: 1 1;
    font-size: 12px;
    padding: 4px;
  }
  p{
    font-size: 14px;
  }
  .btns{
    text-align: center;
    margin-top: 2em;
  }
  button{
    background: #42b983;
    border: none;
    color: white;
    font-size: 12px;
    padding: .5em 2em;
    cursor: pointer;
  }
  button:hover{
    background: #55cc99;
  }
</style>
