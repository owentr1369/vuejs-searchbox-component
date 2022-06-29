<template>
  <div class="searchbar">
    <div id="searchBox">
      <img
        src="../assets/icons/gglogo.svg"
        alt=""
        id="googleIcon"
        @click="open"
      />
      <input
        type="text"
        name=""
        id=""
        placeholder="Search Goodle or type a URL"
      />
      <img src="../assets/icons/mic.svg.png" alt="" class="mic-icon" />
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    open: function () {
      const searchBox = document.getElementById("searchBox");
      searchBox.classList.toggle("active");
    },
  },
};
</script>

<style lang="scss" scoped>
.searchbar {
  width: 100%;
  min-height: 100vh;
  background-color: #f0f3ff;
  display: flex;
  justify-content: center;
  align-items: center;
  #searchBox {
    border-radius: 55px;
    padding: 30px;
    background-color: #f0f3ff;
    display: flex;
    align-items: center;
    box-shadow: 6px 6px 10px -1px rgba(0, 0, 0, 0.15),
      -6px 6px 10px -1px rgba(255, 255, 255, 0.7);
  }
  input {
    font-size: 20px;
    /* width: 500px; */
    width: 0;
    border: 0;
    background-color: transparent;
    outline: none;
    /* margin-left: 10px; */
    transition: 0.6s ease-out;
  }

  #googleIcon {
    width: 50px;
    cursor: pointer;
  }
  .mic-icon {
    /* width: 30px; */
    width: 0;
  }
  .active {
    input {
      width: 500px;
      padding: 12px 20px;
    }
    .mic-icon {
      width: 30px;
    }
  }
}
</style>