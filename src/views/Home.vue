<template>
  <div class="home">
    <v-list>
      <v-list-tile v-for="(item,i) in items" :key="i" avatar>
        <v-list-tile-content>{{i}}. {{item}}</v-list-tile-content>
        <v-list-tile-action>
          <v-icon @click="remove(i)">delete</v-icon>
        </v-list-tile-action>
      </v-list-tile>
      <v-text-field
        v-model="newItem"
        @click:append="addItem"
        solo
        label="Add item"
        append-icon="add"
      ></v-text-field>
    </v-list>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  data: () => ({
    items: ["Bananas", "Spinach", "Icecream"],
    newItem: ""
  }),
  methods: {
    remove(index) {
      const list = this.items;
      const newList = [
        ...list.slice(0, index),
        ...list.slice(index + 1, list.length)
      ];
      this.items = newList;
    },
    addItem() {
      const list = this.items;
      const newList = [...list, this.newItem];
      this.items = newList;
    }
  }
};
</script>

<style lang="scss" scoped>
.home {
  padding: 20px;
}
</style>
