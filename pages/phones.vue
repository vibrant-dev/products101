<template>
  <div class="container">
    <div class="row">
      <h1>Phones</h1>
    </div>
    <div class="row">
      <BackToHome />
    </div>
    <div class="row">
      <table class="table">
        <thead>
          <tr>
            <th>Name</th>
            <th>Price</th>
            <th>RAM</th>
            <th>ROM</th>
            <th>Camera</th>
            <th>Battery</th>
            <th>Processor</th>
            <th>Charger</th>
            <th>Display Type</th>
            <th>Hybrid Slim Slot</th>
            <th>Operating System</th>
            <th>Links</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(phone, index) in phones" :key="index">
            <td v-for="(key, keyIndex) in Object.keys(phone)" :key="keyIndex">
              <template v-if="key === 'title'">
                <a :href="phone.links[0].url" target="_blank">
                  {{ phone[key] }}
                </a>
              </template>
              <template v-else-if="key === 'links'">
                <a
                  v-for="(link, linkIndex) of phone[key]"
                  :key="linkIndex"
                  :href="link.url"
                  target="_blank"
                >
                  {{ link.name }}
                </a>
              </template>
              <template v-else>
                {{ phone[key] }}
              </template>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: "Best phones in price ranges | Products101",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "Best and affordable phones in different price ranges for India.",
      },
    ],
  },
  data() {
    return {
      phones: [
        {
          title: " realme 8s 5G",
          price: "14, 999 *",
          ram: "6 GB",
          rom: "128 GB",
          camera: "64MP + 2MP + 2MP | 16MP Front Camera",
          battery: "5000 mAh",
          processor: "MediaTek Dimensity 810 5G Processor",
          charger: "33W",
          display_type: "Full HD+ Display",
          hybrid_slim_slot: "No",
          operating_system: "Android 11",
          links: [{
            name: "flipkart",
            url: "https://www.flipkart.com/motorola-edge-20-fusion-5g-cyber-teal-128-gb/p/itm638d8c580d653?pid=MOBG4RBEYVQGPYPC&cmpid=product.share.pp",
          }],
        },
      ],
    };
  },
};
</script>
