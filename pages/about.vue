<template>
  <div>
    <h1 class="text-2xl">{{ person.name }}</h1>
    <div>
      {{ person.about }}
    </div>
  </div>
</template>

<script>
import { companyName, urlAPI } from "~/config/index.js";
export default {
  data() {
    return {
      person: {
        name: "Muhammad Luthfi Kamal",
        about:
          "  Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque enim ut quas ad. Laborum tempore, modi incidunt odit voluptas provident quam tempora amet magnam! Error laboriosam dolorum blanditiis placeat aut cupiditate non temporibus minima ea voluptas quibusdam reprehenderit possimus repellat voluptatem necessitatibus, doloremque veritatis ab quos similique! Unde animi ea deserunt magni provident soluta accusamus esse eos qui obcaecati beatae quis, a quae aliquam ex modi autem aperiam laudantium fuga rem nisi iusto? Aliquid quos minima voluptatem nam eum nemo, illo fuga obcaecati voluptatibus sunt quidem? Necessitatibus sint, hic quas iure deleniti mollitia magni minus ducimus dolor voluptatibus? Quam, velit?",
      },
    };
  },
  name: "AboutPage",
  head: {
    title: `About - ${companyName}`,
  },
};
</script>
