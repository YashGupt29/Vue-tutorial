<template>
  <div>
    <pre>
    {{ JSON.stringify(formValues, null, 2) }}
  </pre
    >
  </div>
  <form>
    <div class="flex">
      <label for="name">Name</label>
      <!-- v-modal is used to control input element -->
      <input type="text" id="name" v-model="formValues.name" />
    </div>
    <div class="flex">
      <label for="profile">Profile Summary</label>
      <textarea id="profile" v-model="formValues.profileSummary"></textarea>>
    </div>
    <div class="flex">
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a country</option>
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>
    <div class="flex">
      <label for="country">Job Location</label>
      <select id="country" multiple v-model="formValues.jobApplication">
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>
  </form>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      formValues: {
        name: '',
        profileSummary: '',
        country: '',
        jobApplication: '',
        remoteWork: ''
      }
    }
  },
  methods: {
    changeName() {
      this.name = 'MF'
    },
    increment(num, event) {
      this.count += num
      console.log(event)
    },
    decrement(num) {
      this.count -= num
    }
  }
}
</script>

<style scoped>
.flex {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>
