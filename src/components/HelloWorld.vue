<script LANG="ts">
export default {
  data() {
    return {
      color: 'red',
      count: 10,
      notes: [],
      noteTemp: {},
    };
  },
  methods: {
    save() {
      this.notes.push({
        text: this.noteTemp.text,
        creator: this.noteTemp.creator,
      });
      this.noteTemp = {
        text: '',
        creator: '',
      };
    },
  },
};
</script>

<template>
  <input type="text" v-model="noteTemp.text" />
  <br />
  <input type="text" v-model="noteTemp.creator" />

  <div class="div" @click="save">Salvar</div>
  <div>
    <p v-if="notes" v-for="note in notes">
      Texto:{{ note.text }} Criador:{{ note.creator }}
    </p>
  </div>
</template>

<style scoped>
.div {
  background-color: blue;
  height: 50px;
  color: white;
}
</style>
