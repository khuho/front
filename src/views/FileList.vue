<template>
  <section id="section-file-list">
    <Sidebar/>
    <div class="container-fluid">
      <h1>디렉토리</h1>
      <FileList :files="files"/>
    </div>
  </section>

</template>
<style lang="scss">
#section-file-list {
  display: flex;
  &>nav {
    width: 200px;
  }
  &>.container {
    flex: 1;
  }
}
h1 {
  margin: 20px;
  font-size: 24px;
}
</style>
<script>
import Sidebar from '../components/Sidebar';
import FileList from '../components/FileList';

export default {
  components: {Sidebar, FileList},
  data() {
    return {
      files: [
        {name: '파일1'},
        {name: '파일2'}
      ]
    }
  }
}
</script>
