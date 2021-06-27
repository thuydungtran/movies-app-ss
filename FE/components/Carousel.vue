<template>
  <VueSlickCarousel :arrows="false" :dots="true" :autoplay="false">
    <div
      v-for="(movie, id) in moviesSlideArr"
      :key="id"
      class="row carousel__slide-atom"
    >
      <div class="_content col-md-8">
        <a href="#">
          <div class="_content_title">{{ movie.title }}</div>
        </a>
        <p class="_content_info">
          <span class="_star"></span>
          <span class="_date"></span>
          <span class="_tap">1996</span>
        </p>
        <div class="_description">
          <p>
            Mở đầu câu truyện, cậu học sinh trung học 17 tuổi (trong truyện
            tranh là 16) Shinichi Kudo (Jimmy Kudo) bị biến thành cậu bé Conan
            Edogawa. Shinichi trong phần đầu của Thám tử lừng ...
          </p>
          <p class="_director"><span>Đạo diễn:</span> N/A</p>
          <p class="_genre">
            <span>Thể loại:</span>
            <i class="Button STPa AAIco-more_horiz"></i>
          </p>
        </div>
        <a
          href="https://hoathinh247.com/phim-tham-tu-lung-danh-conan-73.html"
          class="Button TPlay AAIco-play_arrow"
          >Xem <strong>Phim</strong></a
        >
      </div>
      <img class="_image-bg" :src="movie.image" alt="image-slide" />
    </div>
  </VueSlickCarousel>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
  components: {
    VueSlickCarousel,
  },
  props: {
    moviesSlideArr: {
      type: Array,
      default() {},
    },
  },
  data() {
    return {}
  },
}
</script>

<style lang="scss">
.carousel {
  &__slide-atom {
    position: relative;
    ._content {
      position: absolute;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.4);
      color: #fff;
      &_title {
        font-size: 37px;
        color: white;
        font-weight: bold;
      }
    }
    // ._image-bg {
    //   width: 100%;
    // }
  }
}
// slick-slider customization
.slick-slider {
  .slick-dots {
    bottom: 15px;
    li {
      button {
        &::before {
          font-size: 12px;
          color: var(--white);
        }
      }
    }
  }
}
</style>
