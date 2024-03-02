<template>
  <div class="home">

    <VForm v-slot="{ errors, values, validate }" @submit="onSubmit">

      {{ errors }} {{ values }}

      <div class="mb-3">

        <label for="email" class="form-label">Email</label>

        <VField id="email" name="email" type="email" class="form-control" :class="{ 'is-invalid': errors['email'] }"
          placeholder="請輸入 Email" rules="email|required" v-model="user.email"></VField>

        <v-error-message name="email" class="invalid-feedback"></v-error-message>

      </div>

      <button class="btn me-2 btn-outline-primary" type="button" @click="validate">驗證</button>

      <button class="btn btn-primary" type="submit">Submit</button>

    </VForm>

  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data () {
    return {
      user: {}
    }
  },
  methods: {
    onSubmit () {
      console.log(this.user)
    }
  },
  created () {
    console.log(this)
  }

}
</script>
