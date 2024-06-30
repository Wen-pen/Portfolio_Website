<script>
   import { Link } from "svelte-routing";
</script>
<nav class="flex items-center justify-between flex-wrap p-6">
    <div class="flex items-center flex-shrink-0 text-white mr-6 font-bold">
     Mwenya Chibwe
    </div>
      <div>
        <Link to="/">
          <p class="inline-block text-sm px-4 py-2 leading-none  text-whitelg:mt-0">Home</p>
        </Link>
        <Link to="/projects">
          <p class="inline-block text-sm px-4 py-2 leading-none  text-whitelg:mt-0">Projects</p>
        </Link>
        <Link to="/contacts">
          <p class="inline-block text-sm px-4 py-2 leading-none  text-whitelg:mt-0">Contact Me</p>
        </Link>
      </div>
  </nav>

