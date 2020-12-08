<template>
  <div class="door-container">
    <div class="door" @click="openDoor" :class="{ 'door-open': showGift }">
      <h2 v-show="!showGift">Gift #{{ id }}</h2>
      <div class="present" v-show="showGift">
        <p>{{ name }}</p>
        <img :src="image" alt="" class="gift-photo" @click.stop="toggleModal" />
        <input type="text" @click.stop />
      </div>
    </div>
    <Modal
      :name="name"
      :img="image"
      v-if="showModal"
      @close="showModal = false"
    />
  </div>
</template>

<script>
import Modal from "./Modal"
export default {
  name: "ListItem",
  components: {
    Modal,
  },
  props: {
    id: Number,
    name: String,
    image: String,
  },
  data: function() {
    return {
      showGift: false,
      showModal: false,
      person: "",
    }
  },
  methods: {
    openDoor() {
      this.showGift = !this.showGift
    },
    toggleModal() {
      this.showModal = !this.showModal
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.door-container {
  padding: 20px;
}
h2 {
  margin: 0 0 5px;
  color: #003b5c;
}
.door {
  background-color: #6cc2ff;
  width: 200px;
  height: 215px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 5px;
}

.door:hover {
  background-color: #0bd4b8;
}

.door.door-open {
  cursor: auto;
}

.present {
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  box-sizing: border-box;
}

.gift-photo {
  display: block;
  max-width: 150px;
  max-height: 75px;
  margin: 0 auto;
  cursor: pointer;
}

p {
  margin: 0 0 10px;
  color: #ffffff;
  font-weight: 600;
}

input {
  border: 0;
  outline: 0;
  margin-top: 10px;
  text-align: center;
  border-radius: 5px;
  padding: 8px 0;
  background-color: #003b5c;
  color: #ffffff;
  font-size: 1em;
}
</style>
