<template>
  <div id="app">
    <h1>gibeom</h1>
    <TodayLuck v-for="luck in lucks" :key="luck" :propsLuck="luck"/>
  </div>
</template>

<script>
import TodayLuck from './components/TodayLuck'
export default {
  name: 'app',
  components: {
    TodayLuck,
  },
  data: function(){
    return {
      lucks: [
        {
          star: '물병자리',
          lucky_msg: '오늘 괜한 조급함으로 일을 그르치게 될 수도 있으니 급할수록 돌아..'
        },
        {
          star: '물고기자리',
          lucky_msg: '전반적으로 그리 좋지 않은 상황에 위치해 있군요. 특히 금전운이 ..'
        },
        {
          star: '쌍둥이자리',
          lucky_msg: '특별한 길운은 없지만 그렇다고 짓궂은 운명의 훼방을 걱정할 필요..'
        },
        {
          star: '천칭자리',
          lucky_msg: '열정적인 당신이 유연하고, 차분함까지 겸비하고 있다면, 동료들의 ..'
        },
        
      ]
    }
  },
  computed: {
    time: function(){
      return new Date()
    },
    // this.input이 바뀌면 filteredInput도 바뀌어야 한다. 즉 종속된 것
    filteredInput: function(){
      return this.input.replace(/바보|똥개|꺼져/g, '**')
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
