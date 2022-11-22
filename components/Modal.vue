<template>
  <div>
    <b-modal :id="'rent-car-modal'" :title="car.name" hide-footer>
      <b-alert
        :show="dismissCountDown"
        dismissible
        variant="success"
        @dismissed="dismissCountDown = 0"
        @dismiss-count-down="countDownChanged"
        class="fixed-top"
      >
        {{this.car.name}} is rented from {{this.from}} to {{this.to}} successfully

      </b-alert>
      <img :src="'../img/' + car.img" class="w-100" height="250" />
      <div>
        <label for="example-datepicker mt-3">From:</label>
        <b-form-datepicker
          id="example-datepicker"
          v-model="from"
          class="mb-2"
        ></b-form-datepicker>
      </div>
      <div>
        <label for="example-datepicker mt-3">To:</label>
        <b-form-datepicker
          id="example-datepicker"
          v-model="to"
          class="mb-2"
        ></b-form-datepicker>
      </div>
      <div class="text-danger" v-if="showError">Please enter date.</div>
      <div class="text-center">
        <b-button @click="showAlert" class="btn m-1"> Rent Now </b-button>
      </div>
    </b-modal>
  </div>
</template>

<script>
export default {
  props: ["car"],
  data() {
    return {
      from: null,
      to: null,
      dismissSecs: 5,
      dismissCountDown: 0,
      showDismissibleAlert: false,
      showError: false
    };
  },
  methods: {
    countDownChanged(dismissCountDown) {
      this.dismissCountDown = dismissCountDown;
    },

    showAlert() {
      if (this.to !== null && this.from !== null) {
        this.dismissCountDown = this.dismissSecs;
        this.showError = false;
      }
      else{
        this.showError = true;
      }
    },
  },
};
</script>

<style>
</style>