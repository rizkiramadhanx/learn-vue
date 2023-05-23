<!-- methods -->
<template>
  <pre>
    {{ JSON.stringify(formValues) }}
  </pre>
  <form @submit="submitForm">
    <div class="form-group">
      <label>Name</label>
      <input type="text" v-model="formValues.name" />
    </div>
    <div class="form-group">
      <label for="address">Address</label>
      <textarea id="address" v-model="formValues.address" />
    </div>
    <div class="form-group">
      <label for="country">country</label>
      <select name="country" id="country" v-model="formValues.country">
        <option value="indonesia">indo</option>
        <option value="malaysia">Malay</option>
        <option value="kamboja">Kamboja</option>
      </select>
    </div>

    <div class="form-group">
      <label for="job">job</label>
      <select
        name="job"
        class="tall-select"
        id="job"
        multiple
        v-model="formValues.job"
      >
        <option value="indonesia">indo</option>
        <option value="malaysia">Malay</option>
        <option value="kamboja">Kamboja</option>
      </select>
    </div>

    <div>
      <input
        id="remote-job"
        type="checkbox"
        v-model="formValues.remoteWork"
        true-value="ya"
        false-value="no"
      />
      <label for="remote-job">job</label>
    </div>

    <div>
      <input
        id="remote-job"
        value="css"
        type="checkbox"
        v-model="formValues.skillSet"
      />
      <label for="remote-job">CSS</label>
      <input
        id="remote-job"
        value="html"
        type="checkbox"
        v-model="formValues.skillSet"
      />
      <label for="remote-job">HTML</label>
      <input
        id="remote-job"
        value="js"
        type="checkbox"
        v-model="formValues.skillSet"
      />
      <label for="remote-job">JS</label>
    </div>
    <div>
      <input value="3-5" type="radio" v-model="formValues.experience" />
      <label>3 - 5</label>
      <input value="6-10" type="radio" v-model="formValues.experience" />
      <label>6-10</label>
      <input value="10-15" type="radio" v-model="formValues.experience" />
      <label>10 - 15</label>
    </div>
    <button type="submit">Submit</button>
  </form>
</template>

<script lang="ts">
export default {
  name: 'Video 16',
  data() {
    return {
      formValues: {
        name: '',
        address: '',
        country: '',
        job: [],
        remoteWork: 'no',
        skillSet: [],
        experience: '',
      },
    };
  },
  methods: {
    submitForm(event: any) {
      event.preventDefault();
      console.log(this.formValues);
    },
  },
};
</script>

<style scoped>
input {
  padding: 4px;
}
input:focus {
  outline: none;
}

.tall-select {
  height: 100px;
}

select {
  height: 30px;
}

select:focus {
  outline: none;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 4px;
}
</style>
