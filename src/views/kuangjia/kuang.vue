<template>
    <div class="warp">
        <div class="nav">
            <div class="header-1">育路出国留学网-专注出国留学提供高质量的留学规划服务</div>
            <header>
                <div class="a">
                    <div class="header-left">
                        <img src="http://cg.yuloo.com/images/yuloo-logo.png" alt="">
                    </div>
                    <div class="header-center">出国留学</div>
                    <div class="header-right">
                        <div>
                            <svg class="icon" aria-hidden="true">
                                <use xlink:href="#icon-31liebiao"></use>
                            </svg>
                        </div>
                    </div>
                </div>
            </header>
            <div class="tu">
                <img src="http://cg.yuloo.com/images/banner3.jpg" alt="">
            </div>
            <div class="breadcrumb">
                当前位置：首页>出国留学网
            </div>
            <wwh></wwh>
            <zwhz></zwhz>
            <lxyr></lxyr>
            <lx></lx>
            <country  v-for="(item,index) in data" :key='index' :data='item'/>
        </div>
        <footer>
            <div>
                <svg class="icon" aria-hidden="true">
                    <use xlink:href="#icon-dianhua"></use>
                </svg>
                电话咨询
            </div>
            <div class="footer-center">
                <svg class="icon" aria-hidden="true">
                    <use xlink:href="#icon-dianhua"></use>
                </svg>
                电话咨询
            </div>
            <div>
                <svg class="icon" aria-hidden="true">
                    <use xlink:href="#icon-dianhua"></use>
                </svg>
                电话咨询
            </div>
        </footer>
    </div>
</template>
<script>
import wwh from "@/views/wwh/wwh.vue";
import lx from "@/views/zwhzlx/index.vue";
import lxyr from "@/views/ply/lxyr.vue";
import zwhz from "@/views/ply/zwhz.vue";
import country from '@/components/country.vue'
export default {
    components:{
        wwh,
        country,
        zwhz,
        lxyr,
        lx
    },
    data(){
        return {
            data:[{
                name:'美国',
                icon:'#icon-meiguo',
                background:'#f8fafb',
                recommend:'美国留学院校推荐',
                recommends:''
            },
            {
                name:'英国',
                icon:'#icon-yingguo',
                background:'#f4f8fb',
                recommend:'英国留学院校推荐',
                recommends:''
            },
            {
                name:'加拿大',
                icon:'#icon-jianada',
                background:'#f9f4f6',
                recommend:'加拿大本硕留学院校推荐',
                recommends:'加拿大中学推荐'
            },
            {
                name:'澳大利亚',
                icon:'#icon-aodaliya',
                background:'#f8fafb',
                recommend:'澳大利亚留学院校推荐',
                recommends:''
            },
            {
                name:'小语种',
                icon:'',
                background:'#f5f4f8',
                recommend:'韩国预科留学院校推荐',
                recommends:'韩国大学推荐'
            }]
        }
    }
}
</script>

<style lang='scss' scoped>
.icon {
    width: 1em; height: 1em;
    vertical-align: -0.15em;
    fill: currentColor;
    overflow: hidden;
}
.warp{
    width: 100%;
    height: 100%;
    background-color: #F5F7F9;
}
.nav{
    padding-bottom: .4rem;
    .header-1{
        width: 95%;
        margin: 0 auto;
        height: .4rem;
        line-height: .4rem;
        color: #838c94;
        font-size: .12rem;
    }
    header{
        width: 100%;
        height: .7rem;
        background: #fff;
        .a{
            width: 95%;
            height: 100%;
            margin: 0 auto;
            display: flex;
            padding: .1rem 0;
            box-sizing: border-box;
            .header-left{
                width: .84rem;
                height: .3rem;
                margin: .1rem 0;
                box-sizing: border-box;
                img{
                    width: 100%;
                    height: 100%;
                }
            }
            .header-center{
                width: .8rem;
                height: .3rem;
                margin: .1rem 0;
                text-align: center;
                font-size: .12rem;
                color: #fff;
                line-height: .3rem;
                background: url(http://cg.yuloo.com/images/public/jb.jpg);
            }
            .header-right{
                width: .5rem;
                height: .5rem;
                flex: 1;
                div{
                    width: .44rem;
                    height: .34rem;
                    background: #fff;
                    float: right;
                    margin-top: .08rem;
                    margin-right: .15rem;
                    margin-bottom: .08rem;
                    text-align: center;
                    border: .01rem solid #f2f2f2;
                    border-radius: .05rem;
                    font-size: .25rem;
                }
            }
        }
    }
    .tu{
        width: 100%;
        height: 1.1rem;
        img{
            width: 100%;
            height: 100%;
        }
    }
    .breadcrumb{
        width: 95%;
        margin: 0 auto;
        height: .4rem;
        line-height: .4rem;
        color: #838c94;
        font-size: .12rem;
    }
}





footer{
    width: 100%;
    height: .4rem;
    background:#337ab7;
    position: fixed;
    left: 0;
    bottom: 0;
    display: flex;
    div{
        width: 33%;
        height: 100%;
        text-align: center;
        line-height: .4rem;
        color: #fff;
    }
    .footer-center{
        border-left: .01rem solid #fff;
        border-right: .01rem solid #fff;
    }
}
</style>
