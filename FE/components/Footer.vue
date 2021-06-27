<template>
  <div class="row mt-2 p-2 footer bg-component">
    <div class="footer--border col-md-12 d-flex">
      <div class="_policy col-md-7">
        <a class="text-white text-hover-yellow" href="#">XEM PHIM</a>
        <a class="text-white text-hover-yellow" href="#">THUẬT NGỬ</a>
        <a class="text-white text-hover-yellow" href="#">CHÍNH SÁCH RIÊNG TƯ</a>
        <a class="text-white text-hover-yellow" href="#">ĐIỀU KHOẢN SỬ DỤNG</a>
      </div>
      <div class="_contact col-md-5">
        <a
          class="_contact--icon text-hover-yellow"
          href="https://www.facebook.com/thitsot.cachua"
          ><i class="fab fa-facebook-square"></i
        ></a>
        <a
          class="_contact--icon text-hover-yellow"
          href="https://twitter.com/Binh40821629"
          ><i class="fab fa-twitter-square"></i
        ></a>
        <a class="_contact--icon text-hover-yellow" href="#"
          ><i class="fab fa-youtube-square"></i
        ></a>
      </div>
    </div>
    <div class="col-md-12">
      <div class="_web-description py-4">
        <a href="#" rel="nofollow" title="Anime"> Anime</a
        ><a href="#" rel="nofollow" title="anime vietsub"> Anime vietsub</a
        ><a href="#" rel="nofollow" title="anime online"> Anime online</a
        ><a href="#" rel="nofollow" title="anime hay"> Anime hay</a
        ><a href="#" rel="nofollow" title="anime hot"> Anime hot</a
        ><a href="#" rel="nofollow" title="One Piece"> One Piece</a
        ><a href="#" rel="nofollow" title="Naruto"> Naruto</a
        ><a href="#" rel="nofollow" title="Conan"> Conan</a
        ><a href="#" rel="nofollow" title="anime nhanh"> Anime nhanh</a
        ><a href="#" rel="nofollow" title="hoat hinh"> Hoat hinh</a
        ><a href="#" rel="nofollow" title="xem hoat hinh"> Xem hoat hinh</a
        ><a href="#" rel="nofollow" title="hoat hinh vietsub">
          Hoat hinh vietsub</a
        >
      </div>
      <p class="_copy pb-2">
        <a class="_content" target="_blank" href="#"
          >xxxx không chịu trách nhiệm đối với bất kỳ nội dung nào được đăng tải
          trong trang web này. Mọi nội dung đều được sưu tầm và nhúng vào
          website tương tự như công cụ tìm kiếm Google. Nếu có vấn đề liên quan
          đến bản quyền, vui lòng email xxxxcom@gmail.com. Copyright ® 2018
          xxxx. All Rights Reserved.</a
        >
      </p>
    </div>
  </div>
</template>
<style lang="scss">
.footer {
  &--border {
    border-bottom: 2px solid var(--mainbackground);
  }
  ._policy {
    display: flex;
    align-items: center;
    justify-content: space-around;
  }
  ._contact {
    display: flex;
    justify-content: flex-end;
    &--icon {
      color: var(--white);
      font-size: 45px;
      margin: 0 5px;
    }
  }
  ._web-description {
    display: flex;
    justify-content: center;
    a {
      color: var(--gray2);
      transition: 0.3s ease;
      &:hover {
        color: var(--white);
      }
    }
  }
  ._copy {
    text-align: center;
    ._content {
      font-size: 12px;
      color: var(--gray2);
      transition: 0.3s ease;
      &:hover {
        color: var(--white);
      }
    }
  }
}
</style>
