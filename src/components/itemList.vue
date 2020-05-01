<template>
  <div>
    <div>ItemList</div>
    <div v-for="item in items" :key="item.name">
      <div class="item">
        <div class="name">名前: {{ item.name }}</div>
        <div class="price">{{ item.price }} 円</div>
      </div>
    </div>
    <div>
      <label>
        名前
        <input type="text" v-model="newItemName" />
      </label>
      <label>
        価格
        <input type="number" v-model="newItemPrice" />
      </label>
      <button @click="add">add</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ItemList",
  data() {
    return {
      items: [
        { name: "たまご", price: 100 },
        { name: "りんご", price: 160 }
      ],
      newItemName: "",
      newItemPrice: 0
    };
  },
  computed: {
    itemListMessage() {
      return "名前" + this.price;
    }
  },
  components: {}
};
</script>

<style></style>