<template>
  <nav class="navigation">
    <div class="picture-wrapper">
      <Picture class="pic" />
    </div>
    <div class="info-tables">
      <InfoTable v-for="info in infos" :infos="info.infos" :key="info.title">
        <template slot="title">{{ info.title }}</template>
      </InfoTable>
    </div>
  </nav>
</template>

<script>
import Picture from './Picture'
import InfoTable from './InfoTable'

export default {
  name: "HelloWorld",
  components: {
    Picture,
    InfoTable
  },
  data() {
    return {
      infos: [
        {
          title: 'info',
          infos: [
            {icon: '', title: 'Name', subtitle: 'Long Johnson'},
            {icon: '', title: 'Address', subtitle: "45214 Street Name\nCity\nProvince"},
            {icon: '', title: 'Phone', subtitle: '012344567889854'},
            {icon: '', title: 'E-Mail', subtitle: 'student41@students.uni.ch'},
            {icon: '', title: 'Website', subtitle: 'name.github.io'}
          ]
        },
        {
          title: 'social',
          infos: [
            {icon: '', title: 'Skype', subtitle: 'longjohnson'},
            {icon: '', title: 'Twitter', subtitle: "twitter.com/longjohn"},
            {icon: '', title: 'LinkedIn', subtitle: 'linkedin.com/longjohn'},
            {icon: '', title: 'Facebook', subtitle: 'facebook.com/longjohn'}
          ]
        },
        {
          title: 'references',
          infos: [
            {icon: '', title: 'Peter Pedigrew', subtitle: 'http://link.com'},
            {icon: '', title: 'Short Johnson', subtitle: "http://link.org"}
          ]
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
  .navigation {
    background-color: #222222;
    padding-bottom: 80px;
  }

  .picture-wrapper {
    display: flex;
    flex: 0;
    justify-content: center;
  }
</style>
