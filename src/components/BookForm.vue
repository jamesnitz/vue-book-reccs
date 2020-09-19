<template>
  <div>
    <button @click="toggleBookForm" class="btn btn-primary">Add Book</button>
    <b-form @submit.prevent="handleSubmit" v-if="showBookForm">

      <b-form-group id="input-group-2" label="Title" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="formData.title"
          required
          placeholder="Enter Book's Title"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Author" label-for="input-1">
        <b-form-input
          id="input-1"
          v-model="formData.author"
          required
          placeholder="Enter Book's Author"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Genre:" label-for="input-3">
        <b-form-select
          id="input-3"
          v-model="formData.genre"
          :options="['Spooky', 'Scary']"
          required
        ></b-form-select>
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
  </div>
</template>

<script>
export default {
  name: 'BookForm',
  data() {
    return {
      showBookForm: false,
      formData: {
        name: '',
        age: 0,
        species: null
      }
    }
  },
  methods: {
    toggleBookForm() {
      this.showBookForm = !this.showBookForm
    }
  }
}
</script>
