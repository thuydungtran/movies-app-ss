<template>
  <div class="container home__wrapper">
    <div class="row">
      <div class="col-md-9 p-0">
        <Carousel :movies-slide-arr="moviesSlideArr" />
      </div>
      <div class="col-md-3 p-0">
        <div class="home__list-movies-latest ml-2 scroll-dark">
          <List-movies-latest />
        </div>
      </div>
    </div>
    <div class="row home__filter bg-component">
      <div class="col-md-6 d-flex justify-content-between py-2">
        <span
          class="_filter-btn"
          :class="{ _active: filterMoviesCode == 'all' }"
          @click="filterMoviesCode = 'all'"
        >
          Tất cả
        </span>
        <span
          class="_filter-btn"
          :class="{ _active: filterMoviesCode == '1' }"
          @click="filterMoviesCode = '1'"
        >
          Hành động
        </span>
        <span
          class="_filter-btn"
          :class="{ _active: filterMoviesCode == '2' }"
          @click="filterMoviesCode = '2'"
        >
          Phép thuật
        </span>
        <span
          class="_filter-btn"
          :class="{ _active: filterMoviesCode == '3' }"
          @click="filterMoviesCode = '3'"
        >
          Harem
        </span>
      </div>
    </div>
    <div class="row bg-component">
      <section class="col-md-9 p-0 p-3">
        <List-card-movies :movies-arr="moviesRs" />
      </section>
      <div class="col-md-3"></div>
    </div>
  </div>
</template>

<script>
import ListMoviesLatest from '~/components/List-movies-latest.vue'
import ListCardMovies from '~/components/List-card-movies.vue'
import Carousel from '~/components/Carousel.vue'
export default {
  name: 'Home',
  components: { ListMoviesLatest, ListCardMovies, Carousel },
  data() {
    return {
      filterMoviesCode: 'all',
      moviesArr: [
        {
          id: 1,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '2',
          date: '2021',
          type: '1',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 2,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '2',
          image:
            'https://img.vncdn.xyz/uploads/images/doc-bo-tieu-dao-f3199.jpg',
        },
        {
          id: 3,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '1',
          date: '2021',
          type: '1',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 4,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '2',
          image:
            'https://img.vncdn.xyz/uploads/images/doc-bo-tieu-dao-f3199.jpg',
        },
        {
          id: 5,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '2',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 6,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '1',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 7,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '1',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 8,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '1',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 9,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '2',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 10,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '1',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 11,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '3',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
        {
          id: 12,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '1',
          image:
            'https://img.vncdn.xyz/uploads/images/kyuukyoku-shinka-shita-full-dive-rpg-ga-genjitsu-yori-mo-kusoge-dattara-f3357.jpg',
        },
      ],
      moviesSlideArr: [
        {
          id: 1,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '2',
          date: '2021',
          type: '1',
          image: 'https://i.ibb.co/SNSF088/home-slide1.png',
        },
        {
          id: 2,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '2',
          image: 'https://i.ibb.co/SNSF088/home-slide1.png',
        },
        {
          id: 3,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '1',
          date: '2021',
          type: '1',
          image: 'https://i.ibb.co/SNSF088/home-slide1.png',
        },
        {
          id: 4,
          name: 'Ngày mai trời lại sáng',
          auth: 'N/A',
          country: 'Mỷ',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '2',
          image: 'https://i.ibb.co/SNSF088/home-slide1.png',
        },
        {
          id: 5,
          name: 'Vệt nắng cuối trời',
          auth: 'N/A',
          country: 'Nhật Bản',
          episodes: 25,
          description:
            'Trong một biến cố bất ngờ, cậu học sinh trung học buồn tẻ Hiro Yuuki đã có được trò chơi nhập vai lặn đầy đủ Kiwame Quest. Được tạo ra bởi công nghệ tốt nhất, trò chơi tuyên bố đưa thực tế đến cùng cực',
          star: '4',
          date: '2021',
          type: '2',
          image: 'https://i.ibb.co/SNSF088/home-slide1.png',
        },
      ],
    }
  },
  computed: {
    moviesRs() {
      return this.moviesArr.filter((movie) => {
        if (this.filterMoviesCode === '1') return movie.type === '1'

        if (this.filterMoviesCode === '2') return movie.type === '2'

        if (this.filterMoviesCode === '3') return movie.type === '3'
        return movie
      })
    },
  },
}
</script>

<style lang="scss">
.home {
  &__list-movies-latest {
    height: 384px;
    background: var(--componentbackground);
    overflow-y: scroll;
  }
  &__filter {
    border-bottom: 2px solid var(--mainbackground);
    ._filter-btn {
      cursor: pointer;
      color: var(--gray2);
      transition: 0.3s ease;
      &._active {
        color: var(--white);
        font-weight: bold;
      }
      &:hover {
        color: var(--white);
      }
    }
  }
}
</style>
