<template>
  <div class="home">
    <NavBar />
    <h1>Some Title Here</h1>
    <div class="header">
      <div class="button" id="allies" @click="openModal">allies</div>
      <div class="button" id="poc" @click="openModal">black & brown people</div>
    </div>
    <div class="redline">
      <img src="../assets/redlining.png" alt="" />
    </div>
    <div class="modal" :class="{ open: isActive }">
      <div class="close-btn">
        <p @click="closeModal">X</p>
      </div>
      <div class="modal-content">
        <p class="modal-text">{{ modalText }}</p>
      </div>
      <div class="hashtag">
        <p>#InvestInBlackLives</p>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
export default {
  name: "Home",
  components: {
    NavBar,
  },
  data() {
    return {
      alliesText:
        "An overlay that pushes from the bottom based off user selection. This content is for allies. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin efficitur dignissim sem, nec porta dui maximus id. Praesent quam purus, blandit et lacus non, cursus mattis elit. Sed risus velit, pulvinar sit amet dui sed, blandit semper mauris. Cras tempus justo ac tellus aliquam, in tristique nisl mattis. Ut quis.",
      pocText:
        "An overlay that pushes from the bottom based off user selection. This content is for black and brown people. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin efficitur dignissim sem, nec porta dui maximus id. Praesent quam purus, blandit et lacus non, cursus mattis elit. Sed risus velit, pulvinar sit amet dui sed, blandit semper mauris. Cras tempus justo ac tellus aliquam, in tristique nisl mattis. Ut quis.",
      isActive: false,
      modalText: "",
    };
  },
  methods: {
    openModal(e) {
      if (!this.isActive) {
        this.isActive = true;
        if (e.target.id === "allies") {
          this.modalText = this.alliesText;
        }
        if (e.target.id === "poc") {
          this.modalText = this.pocText;
        }
      }
      console.log(this.modalText);
    },
    closeModal() {
      if (this.isActive) {
        this.isActive = false;
      }
    },
  },
  created() {
    console.log(this.isActive);
  },
};
</script>

<style lang="scss" scoped>
@import "@/global.scss";
h1 {
  margin: 100px 0 50px 0;
  font-size: 4rem;
  font-weight: 400;
}
.redline {
  img {
    width: 100%;
  }
}
.header {
  @include flex(space-around, center, row);
  .button {
    cursor: pointer;
    font-family: "Sacramento", cursive;
    width: 400px;
    color: white;
    font-size: 50px;
    border: 2px solid white;
    &:hover {
      border: 2px solid black;
      color: black;
      transition: 0.2s;
    }
  }
  #poc {
    background-color: $primary;
  }
  #allies {
    background-color: $secondary;
  }
}
.modal {
  height: 100vh;
  position: fixed;
  top: 100vh;
  background-color: rgba(255, 255, 255, 0.796);
  transition: 0.5s;
  width: 100vw;
  &-content {
    @include flex(center, center, row);
    width: 100%;
    height: 100%;
    .modal-text {
      width: 60%;
      font-weight: bold;
      font-size: 20px;
    }
  }
  .close-btn {
    position: absolute;
    right: 5%;
    top: 2.5%;
    font-size: 20px;
    p {
      cursor: pointer;
      font-weight: bold;
      &:hover {
        text-shadow: 2px 2px gray;
      }
    }
  }
  .hashtag {
    position: absolute;
    right: 5%;
    bottom: 2.5%;
    font-family: "Meddon", cursive;
    font-size: 30px;
  }
}
.open {
  transform: translateY(-100vh);
  transition: 0.5s;
}
</style>
