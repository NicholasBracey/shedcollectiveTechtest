<template>
<v-app>

  <template>
    <v-app id="rating">
      <v-content>
        <v-container fluid fill-height>
          <v-layout align-center justify-center>

            <v-card class="elevation-16 text-xs-center" width="658">

              <div class="mt-5">
                <div class="rating-title">
                  How did we do?
                </div>
                <div class="copy mt-2">
                  Please let us know how your food delievery was.<br>It will really help us to keep improving our service!
                </div>
              </div>

              <div class="text-xs-center mt-4">
                <div class="copy">
                  How would you rate your food?
                </div>

                <v-rating v-model="rating1" color="yellow darken-3" background-color="grey darken-1" empty-icon="$vuetify.icons.ratingFull" half-increments hover large></v-rating>
              </div>

              <div class="text-xs-center mt-4">
                <div class="copy">
                  How would you rate your delivery driver?
                </div>

                <v-rating v-model="rating2" color="yellow darken-3" background-color="grey darken-1" empty-icon="$vuetify.icons.ratingFull" half-increments hover large></v-rating>
              </div>

              <div class="text-xs-center mt-4">
                <div class="copy">
                  How would you rate your overall experience?
                </div>

                <v-rating v-model="rating3" color="yellow darken-3" background-color="grey darken-1" empty-icon="$vuetify.icons.ratingFull" half-increments hover large></v-rating>
              </div>

              <div class="mt-2">
                <v-btn color="#0021FF" large>Submit feedback</v-btn>
              </div>

            </v-card>

          </v-layout>
        </v-container>
      </v-content>
    </v-app>
  </template>
</v-app>
</template>

<script>
export default {
  data: () => ({
    rating1: 4
  })
}
</script>

<style>
.rating-title {
  font-size: 31px;
}

.copy {
  font-size: 21px;
}

.v-btn__content{
  color: white;
  text-transform: none;
}
</style>
