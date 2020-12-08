<template>
  <div class="list">
    <ListItem
      v-for="gift in gifts"
      :id="gift.id"
      :name="gift.name"
      :image="gift.image"
      :key="gift.id"
    />
  </div>
</template>

<script>
import ListItem from "./ListItem"
export default {
  name: "List",
  components: {
    ListItem,
  },
  props: {
    msg: String,
  },
  data: function() {
    return {
      gifts: [
        { id: 1, name: "Blender", image: require("@/assets/01_blender.png") },
        {
          id: 2,
          name: "Brooklyn Winery Tasting Kit",
          image: require("@/assets/02_wine-tasting-kit.png"),
        },
        {
          id: 3,
          name: "Phone Sanatizing Case",
          image: require("@/assets/03_phone_sanitzing_case.png"),
        },
        {
          id: 4,
          name: "Bluetooth Earbuds",
          image: require("@/assets/04_headphones.png"),
        },
        {
          id: 5,
          name: "DYI Sushi & Mochi Kits",
          image: require("@/assets/05_sushi-kit.png"),
        },
        {
          id: 6,
          name: "Royal Seat Cushion",
          image: require("@/assets/06_butt-cushion.png"),
        },
        {
          id: 7,
          name: "Mobile Photo Printer",
          image: require("@/assets/07_photo-printer.png"),
        },
        {
          id: 8,
          name: "Voluspa 12 Candle Set",
          image: require("@/assets/08_candles.png"),
        },
        {
          id: 9,
          name: "Sunday Breakfast Kit",
          image: require("@/assets/09_breakfest-kit.png"),
        },
        {
          id: 10,
          name: "YETI Wine Tumbler",
          image: require("@/assets/10_yeti-wine-tumblers.png"),
        },
        {
          id: 11,
          name: "Beers Of The World",
          image: require("@/assets/11_beer-of-the-world.png"),
        },
        {
          id: 12,
          name: "Chocolate Fountain",
          image: require("@/assets/12_chocolate-fountain.png"),
        },
        {
          id: 13,
          name: "Cornhole",
          image: require("@/assets/13_cornhole.png"),
        },
        {
          id: 14,
          name: "Desk Chair",
          image: require("@/assets/14_desk-chair.png"),
        },
        {
          id: 15,
          name: "Record Player",
          image: require("@/assets/15_record-player.png"),
        },
        {
          id: 16,
          name: "Chain Saw",
          image: require("@/assets/16_chainsaw.png"),
        },
        {
          id: 17,
          name: "Lawn Mower",
          image: require("@/assets/17_lawn-mower.png"),
        },
        {
          id: 18,
          name: "Fujifilm Instax Camera",
          image: require("@/assets/18_polaroid-camera.png"),
        },
        {
          id: 19,
          name: "Toilet Paper & Hand Sanitizer",
          image: require("@/assets/19_toilet-paper-hand-sanitizer.jpg"),
        },
        {
          id: 20,
          name: "Tortilla Blanket & Chipotle Gift Card",
          image: require("@/assets/20_tortilla-blanket.png"),
        },
        {
          id: 21,
          name: "Poker Set",
          image: require("@/assets/21_poker-set.png"),
        },
        {
          id: 22,
          name: "Puzzles & Games",
          image: require("@/assets/22_games.png"),
        },
        {
          id: 23,
          name: "3 Months of Bark Box",
          image: require("@/assets/23_barkbox.png"),
        },
        {
          id: 24,
          name: "Champagne Coupes",
          image: require("@/assets/24_champagne-coupe.png"),
        },
        {
          id: 25,
          name: "Starwars Popcorn Maker",
          image: require("@/assets/25_popcorn-maker.png"),
        },
        {
          id: 26,
          name: "Bombas Socks",
          image: require("@/assets/26_bombas-socks.png"),
        },
        {
          id: 27,
          name: "Porto Rico Coffee, Tea, & Candy",
          image: require("@/assets/27_porto-rico-coffee.png"),
        },
        {
          id: 28,
          name: "2 Jiggy Puzzles",
          image: require("@/assets/28_puzzels.png"),
        },
        {
          id: 29,
          name: "NYT Best Sellers",
          image: require("@/assets/29_nyt-best-sellers.png"),
        },
        {
          id: 30,
          name: "Clean & Sustainable Cleaning Supplies",
          image: require("@/assets/30_cleaning-products.png"),
        },
        {
          id: 31,
          name: "RFID Blocking Wallet",
          image: require("@/assets/31_RFID-blocking-wallet.png"),
        },
      ],
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}
</style>
