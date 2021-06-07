<template>
  <div>
    {{ JSON.stringify(formValues, null, 2) }}
  </div>
  <br />
  <form @submit.prevent="submitForm">
    <div>
      <label for="name">Name</label>
      <input v-model.trim.lazy="formValues.name" type="text" id="name" />
    </div>

    <div>
      <label for="profile">Profile Summary</label>
      <textarea v-model="formValues.profileSummary" type="text" id="profile" />
    </div>

    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a country</option>
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <div>
      <label for="job-location">Job location</label>
      <select id="job-location" multiple v-model="formValues.jobLocation">
        <option value="india">India</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <div>
      <input
        type="checkbox"
        id="remoteWork"
        v-model="formValues.remoteWork"
        true-value="Yes"
        false-value="No"
      />
      <label for="remoteWork">Open to Remote work?</label>
    </div>

    <div>
      <label>Skill set</label>
      <input
        v-model="formValues.skillSet"
        type="checkbox"
        id="html"
        value="html"
      />
      <label for="html">HTML</label>

      <input
        v-model="formValues.skillSet"
        type="checkbox"
        id="css"
        value="css"
      />
      <label for="css">CSS</label>

      <input v-model="formValues.skillSet" type="checkbox" id="js" value="js" />
      <label for="js">JavaScript</label>
    </div>

    <div>
      <label>Years of experience</label>
      <input
        v-model="formValues.yearsOfExp"
        type="radio"
        id="0-2"
        value="0-2"
      />
      <label for="0-2">0-2</label>

      <input
        v-model="formValues.yearsOfExp"
        type="radio"
        id="3-5"
        value="3-5"
      />
      <label for="3-5">3-5</label>

      <input
        v-model="formValues.yearsOfExp"
        type="radio"
        id="6-10"
        value="6-10"
      />
      <label for="6-10">6-10</label>
    </div>

    <div>
      <label for="age">Age</label>
      <input
        @keyup.enter="submitForm"
        type="number"
        id="age"
        v-model.number="formValues.age"
      />
    </div>

    <!-- <div>
      <button type="Submit">Submit</button>
    </div> -->
  </form>
</template>

<script>
export default {
  name: 'Handling_Form',
  data() {
    return {
      formValues: {
        name: '',
        profileSummary: '',
        age: null,
        country: '',
        jobLocation: [],
        remoteWork: 'No',
        skillSet: [],
        yearsOfExp: '',
      },
    };
  },
  methods: {
    submitForm(event) {
      console.log(this.formValues);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
