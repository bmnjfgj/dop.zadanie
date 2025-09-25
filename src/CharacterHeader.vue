<template>
  <div class="info-row">
    <img :src="imageSrc" alt="SpongeBob" class="character-image">
    <table class="personal-table">
      <thead>
      <tr>
        <th>Data type</th>
        <th>Data value</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="item in personalData" :key="item.type">
        <td>{{ item.type }}</td>
        <td>
          {{ item.value }}
          <span v-if="item.color" :class="['color-box', item.color]"></span>
        </td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'CharacterHeader',
  props: {
    imageSrc: {
      type: String,
      required: true
    },
    personalData: {
      type: Array,
      required: true
    }
  }
};
</script>

<style>
.info-row {
  display: flex;
  align-items: flex-start;
  margin-bottom: 20px;
}
.character-image {
  width: 200px;
  height: auto;
  border: 2px solid #87ceeb;
  border-radius: 10px;
  margin-right: 20px;
}
.personal-table {
  width: 100%;
  border-collapse: collapse;
}
.personal-table th, .personal-table td {
  border: 1px solid #ccc;
  padding: 8px;
  text-align: left;
}
.personal-table th {
  background-color: #a9a9a9;
}
.color-box {
  display: inline-block;
  width: 20px;
  height: 20px;
  vertical-align: middle;
  margin-left: 5px;
}
</style>