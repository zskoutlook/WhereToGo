<template>
<div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :cities="cities" :hot="hotCities"></city-list>
    <city-alphabet :cities="cities"></city-alphabet>
</div>
</template>

<script>
import axios from 'axios'
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'

export default {
    data: function () {
        return {
            cities: {},
            hotCities: []
        }
    },
    name: 'city',
    components: {
        CityHeader: CityHeader,
        CitySearch: CitySearch,
        CityList: CityList,
        CityAlphabet: CityAlphabet
    },
    methods: {
        getCityInfo: function () {
            axios.get('/api/city.json')
                .then(this.handleGetCityInfoSucc)
        },
        handleGetCityInfoSucc: function (res) {
            res = res.data
            if (res.ret && res.data) {
                const data = res.data
                this.cities = data.cities
                this.hotCities = data.hotCities
            }
        }
    },
    mounted: function () {
        this.getCityInfo()
    }
}
</script>

<style>   </style>
