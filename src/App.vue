<template>
  <form @submit.prevent="submitForm">
    <div>
      <pre>
    {{ JSON.stringify(formValues, null, 2) }}

  </pre>
      <br />
      <hr />
    </div>
    <div>
      <label for="name">Name</label>
      <input id="name" v-model.trim="formValues.name" />
    </div>
    <br />
    <div>
      <label for="profile">Profile summary</label>
      <textarea id="profile" v-model="formValues.profile"></textarea>
    </div>
    <br />
    <div>
      <label for="country">Select country</label>
      <select id="country" v-model="formValues.country">
        <option value>Select country</option>
        <option value="US">United States</option>
        <option value="GB">United Kingdom</option>
        <option value="CA">Canada</option>
      </select>
    </div>
    <br />

    <div>
      <label for="job-location">Select job location</label>
      <select id="job-location" multiple v-model="formValues.joblocation
      ">
        <option value>Select country</option>
        <option value="US">United States</option>
        <option value="GB">United Kingdom</option>
        <option value="CA">Canada</option>
      </select>
    </div>
    <br />
    <div>
      <label for="job-type">Select job type</label>
      <input type="checkbox" v-model="formValues.jobtype" true-value="yes" false-value="no" />
    </div>
    <br />
    <!-- submit btn -->
    <button type="submit">Submit</button>
  </form>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        profile: "",
        country: "",
        joblocation: [],
        remotework: 'no',
      }
    };
  },
  methods: {
    submitForm() {
      console.log("Form submitted!");
      console.log(this.formValues);
    }

  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
