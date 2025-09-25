<template>
  <div class="biography">
    <h2>Biography</h2>
    <div class="biography-content">
      <div class="biography-text">
        <p v-for="(para, index) in biographyParagraphs" :key="index">{{ para }}</p>
      </div>
      <div class="catchphrases">
        <h3>Catchphrases</h3>
        <ul>
          <li v-for="(phrase, index) in phrases" :key="index">{{ phrase }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BiographySection',
  props: {
    biographyParagraphs: {
      type: Array,
      required: true
    },
    phrases: {
      type: Array,
      required: true
    }
  }
};
</script>

<style>
.biography {
  margin-bottom: 20px;
}
.biography h2 {
  border-bottom: 1px solid #ccc;
  padding-bottom: 5px;
}
.biography-content {
  display: flex;
}
.biography-text {
  flex: 1;
  margin-right: 20px;
}
.catchphrases {
  width: 200px;
  background-color: #f0f8ff;
  border: 1px solid #ccc;
  padding: 10px;
}
.catchphrases h3 {
  margin-top: 0;
}
.catchphrases ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.catchphrases li {
  background-color: #add8e6;
  border: 1px solid #87ceeb;
  padding: 5px;
  margin-bottom: 5px;
  text-align: center;
  border-radius: 5px;
}
</style>