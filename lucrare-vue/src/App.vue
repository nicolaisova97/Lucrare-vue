<template>
  <div class="text-xs-center">
    <v-menu offset-y>
      <template v-slot:activator="{ on }">
        <v-btn
                color="primary"
                dark
                v-on="on"
        >
          Lucrare WEB
        </v-btn>
      </template>
      <v-list>
        <v-list-tile
                v-for="(item, index) in items"
                :key="index"

                @click=""
        >
          <v-list-tile-title :to="item.title">{{ item.title }}</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-menu>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  data: () => ({
    items: [
      { title: 'Home' },
      { title: 'Input' },
      { title: 'Output' },
      { title: 'Students' }
    ]
  })
}
</script>
