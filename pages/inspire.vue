<template>
  <v-layout>
    <v-flex class="text-center">
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;John Johnson</em>
          </small>
        </footer>
      </blockquote>
    </v-flex>
      <v-container fluid>
      <v-data-iterator
        :items="items"
        :items-per-page.sync="itemsPerPage"
        hide-default-footer
      >
        <template v-slot:header>
          <v-toolbar
            class="mb-2"
            color="indigo darken-5"
            dark
            flat
          >
            <v-toolbar-title>This is a header</v-toolbar-title>
          </v-toolbar>
        </template>

        <template v-slot:default="props">
          <v-row>
            <v-col
              v-for="item in props.items"
              :key="item.name"
              cols="12"
              sm="6"
              md="4"
              lg="3"
            >
              <v-card>
                <v-card-title class="subheading font-weight-bold">{{ item.name }}</v-card-title>

                <v-divider></v-divider>

                <v-list dense>
                  <v-list-item>
                    <v-list-item-content>Calories:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.calories }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Fat:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.fat }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Carbs:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.carbs }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Protein:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.protein }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Sodium:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.sodium }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Calcium:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.calcium }}</v-list-item-content>
                  </v-list-item>

                  <v-list-item>
                    <v-list-item-content>Iron:</v-list-item-content>
                    <v-list-item-content class="align-end">{{ item.iron }}</v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
            </v-col>
          </v-row>
        </template>

        <template v-slot:footer>
          <v-toolbar
            class="mt-2"
            color="indigo"
            dark
            flat
          >
            <v-toolbar-title class="subheading">This is a footer</v-toolbar-title>
          </v-toolbar>
        </template>
      </v-data-iterator>
    </v-container>
  </v-layout>
</template>
