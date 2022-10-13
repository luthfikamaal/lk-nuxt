<template>
  <div class="h-screen">
    <h1
      class="text-2xl p-3 rounded-md bg-green-200 text-green-600 font-semibold border-2 border-solid border-green-300"
    >
      Welcome to The Jungle!
    </h1>
  </div>
</template>

<script>
import { companyName } from "~/config/index.js";
export default {
  name: "IndexPage",
  head: {
    title: `Home - ${companyName}`,
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Home page description",
      },
    ],
  },
};
</script>
