<template>
  <v-app id="rating">
    <main>
      <v-img class="img_rating" src="https://pbs.twimg.com/media/Cpg9zadVMAA48Bl.png"></v-img>

      <div class="text-xs-center">
        <v-btn color="#FB9F44" @click="dialog = true">Show me what you got!</v-btn>
      </div>

      <v-dialog v-model="dialog" transition="dialog-bottom-transition" width="659">
        <v-container>
          <v-card>
            <v-icon @click="dialog = false">cancel</v-icon>

            <v-card-title class="justify-center rating__title pt-5">How did we do?</v-card-title>
            <p
              class="rating__copy mt-2 mr-4 ml-4"
            >Please let us know how your food delievery was. It will really help us to keep improving our service!</p>

            <div class="text-xs-center mt-4">
              <h2 class="rating__subhead">How would you rate your food?</h2>
              <v-rating
                v-model="foodRating"
                color="yellow darken-3"
                background-color="grey darken-1"
                empty-icon="$vuetify.icons.ratingFull"
                half-increments
                hover
                large
              ></v-rating>
            </div>

            <div class="text-xs-center mt-4">
              <h2 class="rating__subhead">How would you rate your delivery driver?</h2>

              <v-rating
                v-model="driverRating"
                color="yellow darken-3"
                background-color="grey darken-1"
                empty-icon="$vuetify.icons.ratingFull"
                half-increments
                hover
                large
              ></v-rating>
            </div>

            <div class="text-xs-center mt-4">
              <h2 class="rating__subhead">How would you rate your overall experience?</h2>

              <v-rating
                v-model="overallRating"
                color="yellow darken-3"
                background-color="grey darken-1"
                empty-icon="$vuetify.icons.ratingFull"
                half-increments
                hover
                large
              ></v-rating>
            </div>

            <div class="text-xs-center pb-5">
              <v-btn @click="handleSubmit" color="#0021FF" large>Submit feedback</v-btn>
            </div>
          </v-card>
        </v-container>
      </v-dialog>
    </main>
  </v-app>
</template>

<script>
/* eslint-disable */
export default {
  data: () => ({
    foodRating: 3,
    driverRating: 3,
    overallRating: 3,
    dialog: false
  }),
  methods: {
    handleSubmit() {
      alert(
        `food rating: ${this.foodRating}, driver rating: ${
          this.driverRating
        }, overall rating: ${this.overallRating}`
      );
    }
  }
};
</script>

<style scoped lang="postcss">
.container {
  box-shadow: 0;
}

.v-dialog:not(.v-dialog--fullscreen) {
  box-shadow: none !imporant;
}

.rating {
  font-family: 'Helvetica', sans-serif;
}

.rating__content {
  padding: 1em 2em;
}

.rating__title {
  font-size: 2.5em;
  font-weight: bold;
}

.rating__subhead {
  padding: 1em 2em;
}

.rating__copy {
  font-size: 1.5em;
  text-align: center;
}

.v-icon {
  position: absolute;
  top: -20px;
  right: -10px;
  font-size: 60px;
  color: #000;
  cursor: pointer;
}

.v-btn {
  color: white;
  text-transform: none;
  font-weight: bold;
  padding: 1.5em 2.5em;
  line-height: 3px;
  margin: 1em;
  text-align: center;
}

.img_rating {
  margin: 0 auto;
  width: 300px;
}
</style>
