<template>
  <div>
    <pre>
    {{ JSON.stringify(formValues, null, 2) }}
  </pre
    >
  </div>
  <form @submit="submitForm">
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
    <div>
      <input id="check" v-model="formValues.remoteWork" true-value="yes" false-value="no" />
      <label for="check">Are you open to work?</label>
    </div>
    <div class="flex">
      <label>Skill-Set</label>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillSet" />
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet" />
      <label for="css">CSS</label>
      <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet" />
      <label for="javascript">javascript</label>
    </div>
    <div class="flex-box">
      <label>Years Of Expirience</label>
      <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExprience" />
      <label for="0-2">0-2</label>
      <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExprience" />
      <label for="3-5">3-5</label>
      <input type="radio" id="6-10" value="6-10" v-model="formValues.yearsOfExprience" />
      <label>6-10</label>
    </div>
    <div>
      <button>Submit</button>
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
        jobApplication: [],
        remoteWork: 'no',
        skillSet: [],
        yearsOfExprience: ''
      }
    }
  },
  methods: {
    submitForm(e) {
      e.preventDefault()
      console.log(this.formValues)
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
label {
  font-weight: bold;
  font-size: large;
}
.flex-box {
  display: flex;
  gap: 20px;
}
</style>
