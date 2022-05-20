<template>
  <table class="table table-striped">
    <thead>
    <tr>
      <th scope="col" id="table-head-check">
        <input type="checkbox" class="form-check-input" aria-label="Select All">
      </th>
      <th scope="col" colspan="3">최근</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="file in files" class="file-list-item">
      <th><input type="checkbox" class="form-check-input" aria-label="Select File"></th>
      <td class="thumbnail">
        <!-- 파일 썸네일 임시 -->
        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="currentColor" class="bi bi-file-earmark" viewBox="0 0 16 16">
          <path d="M14 4.5V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2h5.5L14 4.5zm-3 0A1.5 1.5 0 0 1 9.5 3V1H4a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V4.5h-2z"/>
        </svg>
      </td>
      <td class="data">
        <div>{{ file.name }}</div>
        <small>2022년 1월 1일</small>
      </td>
    </tr>
    </tbody>
  </table>
</template>
<style lang="scss">
#table-head-check {
  width: 36px;
}
.file-list-item {
  td.thumbnail {
    width: 40px;
  }
  td.data {
    small {
      color: #666;
      font-size: 75%;
    }
  }
}
</style>
<script>
export default {
  props: ['files']
}
</script>