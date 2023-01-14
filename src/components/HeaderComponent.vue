
<template>
  <div class="header">
    <div class="logo">
      <img src="../assets/NFters.png" alt="nfters">
    </div>
    <div class="menubar">
      <nav>
        <RouterLink to="/">MarketPlace</RouterLink>
        <RouterLink to="/">Resources</RouterLink>
        <RouterLink to="/">About</RouterLink>
      </nav>
    </div>
    <div class="buttonGoup">
      <form action="">
        <input placeholder="Search" class="search" type="text"/>
        <div class="icon">
          <IconSearch/>
        </div>
      </form>
      <div class='file file-uploading'>
        <label for='input-file'>Upload</label>
        <input id='input-file' type='file' />
      </div>
      <button class="wallet">Connect Wallet</button>
    </div>
  </div>
</template>
<script setup>
  import IconSearch from './icons/IconSearch.vue';
</script>
<style scoped lang="scss">
.header{
  display: flex;
  padding: 1.7rem 5rem;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #EFEFEF;
  .logo {
    padding-right: 1rem;
    border-right: 1px solid #F4F4F4;
  }
  .menubar nav{
    display: flex;
    gap: 20px;
  }
  .menubar nav a{
    color:#000;
    font-size: 16px;
  }
  .menubar nav a:hover{
    background-color: transparent;
    color: #3D00B7;
  }
  .buttonGoup{
    display: flex;
    gap: 10px;
    justify-content: start;
    align-items: center;
    form{
      position: relative;
    }
    form input{
      color:#C0C0C0;
      font-weight: 300;
      border:1px solid #C0C0C0;
      border-radius: 30px;
      padding: 14px 10px;
      width: 250px;
    }
    .icon{
      position: absolute;
      top:10px;
      right:13px;
    }
    .file {
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .file > input[type='file'] {
      display: none
    }

    .file > label {
      font-size: 1rem;
      font-weight: 300;
      cursor: pointer;
      outline: 0;
      user-select: none;
      border-color: #3D00B7;
      border-style: solid;
      border-radius: 35px;
      border-width: 1px;
      background-color: #3D00B7;
      color: #fff;
      padding: 13px 40px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .file > label:hover {
      border-color: hsl(0, 0%, 21%);
    }

    .file > label:active {
      background-color: hsl(0, 0%, 96%);
    }

    .wallet{
      color:#3D00B7;
      border: 2px solid #3D00B7;
      border-radius: 25px;
      font-weight: 500;
      background-color: transparent;
      padding: 14px 35px;
      transition: .3s all ease-in-out;
      cursor: pointer;
      &:hover{
        background-color: #3D00B7;
        color:#fff;
      }
    }
  }
}

</style>
