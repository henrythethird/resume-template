<template>
  <div class="profile-wrapper">
    <div class="profile"></div>
  </div>
</template>

<script>
export default {
  name: 'Picture'
}
</script>

<style lang="scss" scoped>
  .profile-wrapper {
    height: 270px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .profile {
    display: block;
    background-color: white;
    width: 200px;
    height: 200px;
    padding: 0px;
    border-radius: 100%;
    
    background-image: url(https://images.pexels.com/photos/542282/pexels-photo-542282.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260);
    background-size: cover;
    background-position: center;

    border: 2px solid white;

    transition: padding 200ms, border-radius 250ms;

    &:hover {
      padding: 20px;
      border-radius: 0;
    }
  }
</style>
