<template>
  <div class="container">
    <div class="row">
      <h1>Ear Phones</h1>
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
            <th>Micro Phone Present</th>
            <th>Noice Control</th>
            <th>Links</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(product, index) in products" :key="index">
            <td v-for="(key, keyIndex) in Object.keys(product)" :key="keyIndex">
              <!-- <template v-if="key === 'title'">
              <a :href="products.links[0].url" target="_blank">
                {{ products[key] }}
              </a>
            </template> -->
              <template v-if="key === 'links'">
                <a
                  v-for="(link, linkIndex) of product[key]"
                  :key="linkIndex"
                  :href="link.url"
                  target="_blank"
                >
                  {{ link.name }}
                </a>
              </template>
              <template v-else>
                {{ product[key] }}
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
    title: "Best ear phones in price ranges | Products101",
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
      products: [
        {
          title: "Sony MDR-EX150AP Wired",
          price: "899 *",
          micro_phone: "Yes",
          noice_control: "Active Noise Cancellation",
          links: [
            {
              name: "Amazon",
              url: "https://amzn.to/3pjn6EZ",
            },
          ],
        },
        {
          title: "realme Wired in Ear Buds 2",
          price: "599 *",
          micro_phone: "Yes",
          noice_control: "--",
          links: [
            {
              name: "Amazon",
              url: "https://amzn.to/3jjgrH0",
            },
          ],
        },
      ],
    };
  },
};
</script>
