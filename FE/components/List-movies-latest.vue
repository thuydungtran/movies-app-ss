<template>
  <div class="list-name-movies text-white">
    <div class="_title mx-auto">
      <p class="text-center">ANIME MỚI CẬP NHẬT</p>
    </div>
    <ul class="_list">
      <li v-for="(movies, id) in moviesName" :key="id">
        {{ movies.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      moviesName: [
        { id: '1', name: 'Super Cub' },
        {
          id: '1',
          name: 'Kaguya-sama wa Kokurasetai: Tensai-tachi no Renai Zunousen OVA',
        },
        {
          id: '1',
          name: 'Kyuukyoku Shinka shita Full Dive RPG ga Genjitsu yori mo Kusoge Dattara',
        },
        { id: '1', name: 'Nanatsu no Taizai: Fundo no Shinpan' },
        { id: '1', name: 'Shadows House' },
        { id: '1', name: 'Osananajimi ga Zettai ni Makenai Love Comedy' },
      ],
    }
  },
}
</script>

<style lang="scss">
.list-name-movies {
  background: var(--componentbackground);
  ._title {
    padding-top: 10px;
    position: relative;
    line-height: 19px;
    text-align: center;
    p {
      font-weight: 600;
    }
  }

  ._list {
    padding: 10px;
    li {
      width: 100%;
      padding: 8px 6px 5px 8px;
      font-size: 13px;
      border-width: 0 0 1px;
      border-style: solid;
      border-color: #171515;
      margin-bottom: 0;
      overflow: hidden;
      text-overflow: ellipsis;
      display: inline-block;
      white-space: nowrap;
      vertical-align: middle;
      color: #ce9090;
      transition: 0.3s ease;
      cursor: pointer;
      &:hover {
        color: var(--white);
        background: #ce9090;
      }
    }
  }
}
</style>
