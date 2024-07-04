<script>
    import { gsap } from "gsap/dist/gsap"
    import { onMount } from 'svelte'
    import { TextPlugin } from "gsap/dist/TextPlugin"
    import Nav from "../components/nav.svelte";
    import Button from "../components/button.svelte";

    let main
</script>

<main bind:this={main} class="min-h-screen bg-gradient-to-t from-[#DEE4EA] to-[#7D8184] text-white bg-blend-multiply font-poppins" >
 
    <Nav/>
    <div class="flex items-center justify-center h-32"></div>
    <h1 class="text-center text-white font-extrabold text-4xl p-3 m-3" id="main">
        Contact Me
    </h1>
    <div class="flex flex-col items-center" id="main">
        <a href="https://www.instagram.com/damnmlc/">
            <button type="button" class="bg-gradient-to-r from-[#DEE4EA] to-[#F9FCFF] rounded-full shadow-lg p-5 font-semibold text-gray-400 mx-3 my-3">
                    Instagram Link
            </button>
        </a>
        <a href="https://x.com/mwenyamail877">
            <button type="button" class="bg-gradient-to-r from-[#DEE4EA] to-[#F9FCFF] rounded-full shadow-lg p-5 font-semibold text-gray-400 mx-3 my-3">
                X/Twitter Link
            </button>
        </a>
        <a href="mailto:mwenyamail877@gmail.com">
            <button type="button" class="bg-gradient-to-r from-[#DEE4EA] to-[#F9FCFF] rounded-full shadow-lg p-5 font-semibold text-gray-400 mx-3 my-3">
                Email Link
            </button>
        </a>
    </div>
</main>