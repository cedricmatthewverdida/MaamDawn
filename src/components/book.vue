<template>

      <v-dialog
        transition="dialog-top-transition"
        max-width="600"
        dark
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            outlined
            large
            rounded
            color="white"
            v-bind="attrs"
            v-on="on"
          >Book Now</v-btn>
        </template>
        <template v-slot:default="dialog">
          <v-card>
            <v-toolbar
              color="primary"
              dark
            >Evelyn Waterpark Ticket in Cagayan de Oro</v-toolbar>
            <v-card-text>
              <Steps/>
            </v-card-text>
            <v-card-actions class="justify-end">
              <v-btn
                text
                @click="dialog.value = false"
              >Close</v-btn>
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>

</template>


<script>
import Steps from '~/components/steps.vue'
export default {
    components:{
        Steps
    }
}
</script>