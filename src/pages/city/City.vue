<template>
  <div>
    <city-header></city-header>
    <city-container :city="cityList"></city-container>
  </div>
</template>

<script>
import axios from 'axios'
import CityHeader from './components/Header'
import CityContainer from './components/Container'
export default {
  name: 'City',
  data () {
    return {
      cityList: {},
      litter: ''
    }
  },
  components: {
    CityHeader,
    CityContainer
  },
  mounted () {
    this.getCityInfo()
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json').then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      this.cityList = res.data.data
    }
  }
}
</script>

<style scoped lang="stylus"></style>
