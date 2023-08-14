<template>
  <div>
    <router-link to="/courses">Back</router-link>
    <div class="cover" :style="coverStyle"/>
    <h1>{{course.name}}</h1>
    <p>{{course.text}}</p>
  </div>
</template>

<script>
import courses from './courses';

export default {
  computed:{
    course(){
      const {id} = this.$route.params;
      return courses.find(course=>course.id == id) || {};
    },
    coverStyle(){
      return {
        backgroundImage: `url('${this.course.img}')`,
      }
    },
  },
};
</script>

<style scoped>
a{
  font-size: 10px;
  text-decoration: none;
  color: #42b983;
  line-height: 2.5em;
}
a:before{
  content: '< ';
}
.cover{
  width: 100%;
  height: 200px;
  background: center center;
  background-size: cover;
}
h1{
  color: #42b983;
}
p{
  font-size: 10px;
}
</style>
