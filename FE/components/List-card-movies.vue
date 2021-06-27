<template>
  <div class="row list-card-moves">
    <article
      v-for="(movie, id) in moviesArr"
      :key="id"
      class="col-md-3 col-sm-6 _card"
    >
      <a href="#">
        <div>
          <figure class="Objf TpMvPlay AAIco-play_arrow">
            <img
              :src="movie.image"
              :alt="movie.name"
              :title="movie.name"
              class="_image"
            />
          </figure>
        </div>
        <div class="_episodes">
          <span>{{ movie.episodes }}</span>
          <span>tập</span>
        </div>
        <h2 class="_title m-0">{{ movie.name }}</h2>
        <div class="_rate-group">
          <div class="_star">
            <i
              v-for="star in 5"
              :key="star"
              :class="{ active: star <= movie.star }"
              class="fas fa-star"
            ></i>
          </div>
          <span class="_date">
            <i class="far fa-calendar-alt"></i>{{ movie.date }}</span
          >
        </div>
      </a>
    </article>
  </div>
</template>

<script>
export default {
  name: 'ListCardMovies',
  props: {
    moviesArr: {
      type: Array,
      default() {},
    },
  },
}
</script>

<style lang="scss">
.list-card-moves {
  ._card {
    position: relative;
    padding-bottom: 25px;
  }
  ._image {
    width: 100%;
    height: 210px;
    border-radius: 3px;
  }
  ._title {
    color: var(--white);
    font-size: 14px;
    width: 100%;
    text-align: center;
    overflow: hidden;
    text-overflow: ellipsis;
    display: inline-block;
    white-space: nowrap;
  }
  ._rate-group {
    line-height: 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    ._star {
      font-size: 12px;
      i {
        color: var(--white);
        &.active {
          color: var(--yellow1);
        }
      }
    }
    ._date {
      font-size: 13px;
      text-align: center;
      color: var(--gray1);
      i {
        font-size: 14px;
        color: var(--gray1);
        margin-right: 5px;
      }
    }
  }
  ._episodes {
    position: absolute;
    top: 0;
    background: #ffc107;
    padding: 3px 8px;
    border-radius: 20px;
    color: white;
    margin: 5px;
    box-shadow: rgb(2 2 2 / 30%) 0 3px 8px;
    & :first-child {
      font-size: 16px;
      font-weight: bold;
    }
  }
}
</style>
