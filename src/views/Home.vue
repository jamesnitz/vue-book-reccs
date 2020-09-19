<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <BookForm />
  </div>
</template>

<script>
// @ is an alias to /src
import BookForm from '@/components/BookForm.vue'

export default {
  name: 'Home',
  components: {
    BookForm
  }
}
</script>
