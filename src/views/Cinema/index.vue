<template>
    <div id='main'>
        <Header title='喵喵影院'></Header>
            <div id="content">          
                <div class="cinema_menu">
                    <router-link tag="div" to="/cinema/ciList" class="city_switch">
                        全城 <i class="iconfont icon-lower-triangle"></i>
                    </router-link>
                    <router-link tag="div" to="/cinema/brand" class="brand_awitch">
                        品牌 <i class="iconfont icon-lower-triangle"></i>
                    </router-link>
                    <router-link tag="div" to="/cinema/feature" class="feature_awitch">
                        特色 <i class="iconfont icon-lower-triangle"></i>
                    </router-link>
                </div>
                <keep-alive>
                    <router-view></router-view>
                </keep-alive>
            </div>
        <TabBar></TabBar>
    </div>   
</template>

<script>
import Header from '@/components/Header';
import TabBar from '@/components/TabBar';
export default {
    name: 'Cinema',
    components: {
        Header,
        TabBar
    }
}
</script>

<style scoped>
 #content .cinema_menu{ width: 100%; height: 45px; border-bottom:1px solid #e6e6e6; display: flex; justify-content:space-around; align-items:center; background:white;}   
.cinema_menu .city_switch{ margin-left: 20px; height:100%; line-height: 45px;}
.cinema_menu .city_switch.active{ color: #ef4238; border-bottom: 2px #ef4238 solid;}
.cinema_menu .city_switch.router-link-active{ color: #ef4238; border-bottom: 2px #ef4238 solid;}
.cinema_menu .brand_awitch{ height:100%; line-height: 45px;}
.cinema_menu .brand_awitch.active{ color: #ef4238; border-bottom: 2px #ef4238 solid;}
.cinema_menu .brand_awitch.router-link-active{ color: #ef4238; border-bottom: 2px #ef4238 solid;}
.cinema_menu .feature_awitch{ margin-right:20px; height:100%; line-height: 45px;}
.cinema_menu .feature_awitch.active{ color: #ef4238; border-bottom: 2px #ef4238 solid;}
.cinema_menu .feature_awitch.router-link-active{ color: #ef4238; border-bottom: 2px #ef4238 solid;}
</style> 