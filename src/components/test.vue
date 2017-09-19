<template lang="html">
  <div class="recommend">
    <div class="recommend-content">
      <div v-if="recommends.length" class="slider-wrapper">
          <slider>
            <div v-for=" item in recommends">
              <a :href="item.linkUrl">
                <img :src="item.picUrl">
              </a>
            </div>
          </slider>
      </div>
      <div class="recommend-list">
        
        <ul>

        </ul>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
import slider from '../base/slider/slider.vue'
export default {
  data() {
    return {
      recommends: [
        {
          id:1,
          linkUrl:"https://y.qq.com/m/act/maskessinger2/v3/index.html?ADTAG=jiaodiantu",
          picUrl:"http://y.gtimg.cn/music/photo_new/T003R720x288M000003IMpTu0IQFPx.jpg"
        },
        {
          id:2,
          linkUrl:"https://y.qq.com/m/digitalbum/gold/index.html?_video=true&id=2226509&g_f=shoujijiaodian",
          picUrl:"http://y.gtimg.cn/music/photo_new/T003R720x288M000001ztvX61WIuaH.jpg"
        }
      ]
    }
  },

  components: {
    slider
  },
  methods: {

  }
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
 .recommend
  position:fixed
  width:100%
  top:88px
  bottom:0
  .recommend-content
    height:100%
    overflow:hidden
    .slider-wrapper
      position:relative
      width:100%
      overflow:hidden
  .recommend-list
    .list-title
      height:65px
      line-height:65px
      text-align:center
      font-size:14px
      color:#ffcd32
    .item
      display:flex
      box-sizing: border-box
      align-items:center
      padding: 0 20px 20px 20px
      .icon
        flex: 0 0 60px
        width:60px
        padding-right:20px
      .text
        display:flex
        flex-direction: column
        justify-content:center
        flex:1
        line-height:20px
        overflow:hidden
        font-size:14px
        .name
          margin-bottom:10px
          color:#fff
        .desc
          color:rgba(255,255,255,0.3)
  .loading-container
    position:absolute
    width:100%
    top:50%
    transform:translateY(-50%)
</style>
