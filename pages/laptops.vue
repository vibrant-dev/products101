<template>
  <div class="container">
    <div class="row">
      <h1>Laptops</h1>
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
            <th>Processor</th>
            <th>Clock Speed</th>
            <th>Clock Speed Turbo Boost</th>
            <th>Size</th>
            <th>RAM Expandle</th>
            <th>Cache</th>
            <th>Best Use Case</th>
            <th>Links</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(laptop, index) in laptops" :key="index">
            <td v-for="(key, keyIndex) in Object.keys(laptop)" :key="keyIndex">
              <template v-if="key === 'title'">
                <a :href="laptop.links[0].url" target="_blank">
                  {{ laptop[key] }}
                </a>
              </template>
              <template v-else-if="key === 'links'">
                <a
                  v-for="(link, linkIndex) of laptop[key]"
                  :key="linkIndex"
                  :href="link.url"
                  target="_blank"
                >
                  {{ link.name }}
                </a>
              </template>
              <template v-else>
                {{ laptop[key] }}
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
    title: "Best laptops in price ranges | Products101",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "Best and affordable laptops in different price ranges for India.",
      },
    ],
  },
  data() {
    return {
      laptops: [
        {
          title: "DELL Inspiron Pentium Quad Core",
          price: "28,596 *",
          ram: "4 GB",
          processor: "Intel Pentium Quad Core",
          clock_speed: "1.1 GHz",
          clock_speed_turbo_boost: "Upto 3.1 GHz",
          hard_disk_size: "256 GB SSD",
          ram_expandable: "Upto 16 GB",
          cache: "4 MB",
          best_use_case: 'Study and Basic multi tasking',
          links: [
            {
              name: "Flipkart",
              url: "https://www.flipkart.com/dell-inspiron-pentium-quad-core-4-gb-256-gb-GB SSD-windows-10-home-3502-laptop/p/itm69203f870345e?pid=COMGYCG8G3VFVBPA&lid=LSTCOMGYCG8G3VFVBPA8J3QCX",
            },
          ],
        },
        {
          title: "Dell Vostro 3405",
          price: "46,100 *",
          ram: "8 GB",
          processor: "AMD Ryzen 5 3500U",
          clock_speed: "2.2 GHz",
          clock_speed_turbo_boost: "No Info as of now",
          hard_disk_size: "512 GB SSD",
          ram_expandable: "Upto 16 GB",
          cache: "No Info as of now",
          best_use_case: 'Study, Programming and Multi tasking',
          links: [
            {
              name: "Amazon",
              url: "https://amzn.to/3gQu3Zi",
            },
          ],
        },
        {
          title: "Lenovo IdeaPad Slim 3 (2021)",
          price: "55,000 *",
          ram: "8 GB",
          processor: "AMD Ryzen 5 5500U",
          clock_speed: "2.1 GHz",
          clock_speed_turbo_boost: "4.0 GHz",
          hard_disk_size: "512 GB SSD",
          ram_expandable: "Upto 12 GB",
          cache: "8 MB",
          best_use_case: 'Study, Programming and Multi tasking',
          links: [
            {
              name: "Amazon",
              url: "https://amzn.to/2Zwi1i7",
            },
          ],
        },
        {
          title: "Lenovo ThinkPad E15",
          price: "69,500 *",
          ram: "8 GB",
          processor: "Intel I5 11th gen",
          clock_speed: "2.4 GHz",
          clock_speed_turbo_boost: "4.2 GHz",
          hard_disk_size: "512 GB SSD",
          ram_expandable: "Upto 32 GB",
          cache: "8 MB",
          best_use_case: 'Business, Programming and Heavy multi tasking purpose',
          links: [
            {
              name: "Amazon",
              url: "https://amzn.to/38sipza",
            },
          ],
        },
        {
          title: "Dell Vostro 5415",
          price: "56,000 *",
          ram: "8 GB",
          processor: "AMD Ryzen 5-5500U",
          clock_speed: "3.2 GHz",
          clock_speed_turbo_boost: "--",
          hard_disk_size: "512 GB SSD",
          ram_expandable: "Upto 16 GB",
          cache: "No info as of now",
          best_use_case: 'Business, Programming and Heavy multi tasking purpose',
          links: [
            {
              name: "Amazon",
              url: "https://amzn.to/3fURfrD",
            },
          ],
        },
      ],
    };
  },
};
</script>
