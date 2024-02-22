<script lang="ts">
  import { onMount } from "svelte";
  import Navbar from "./Components/Navbar.svelte";
  import Users from "./Components/Users.svelte";
  import axios from "axios";
  export let id: string;
  let testList: any;

  onMount(async () => {
    axios.get("https://dummyjson.com/products").then((res) => {
      testList = res.data.products;
    });
  });
</script>

>
<div class="w-full gap-4 h-screen grid grid-cols-3 px-[20%] mt-20 bg-white">
  <Navbar test={Number(id)} />
  <Users data={testList} />
</div>
