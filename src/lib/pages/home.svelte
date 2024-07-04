<script>
    import Button from "../components/button.svelte"
    import { gsap } from "gsap/dist/gsap"
    import { onMount } from 'svelte'
    import { TextPlugin } from "gsap/dist/TextPlugin"
  import { Link } from "svelte-routing";

    let main
    gsap.registerPlugin(TextPlugin);
    onMount(() =>{
        if (main){
            gsap.from("#main" ,{
            duration: 5, 
            opacity: 0,
        })
        }
        })
</script>
 
<main bind:this={main} class="min-h-screen bg-gradient-to-t from-[#DEE4EA] to-[#7D8184] text-white bg-blend-multiply font-poppins">
    <div class="flex items-center justify-center h-32">
        <div class="m-6 w-32 bg-grey-400"></div>
    </div>
        
    <h1 class="text-6xl text-center" id="main" >
       
        🧑🏾‍💻
    </h1>
    
    <h1 class="text-white text-center font-extrabold m-3 text-4xl" id="main">
        
        Mwenya Chibwe
    </h1>

        <div class="flex flex-col items-center" id="main">
            <div class="w-96">
                <p class="text-white m-3 text-center shrink font-normal">
                    A 19 year old incoming computer science student at Nottingham Trent University. Experienced in Python, JS, C# and Dart. 
                    
                </p>
                <p class="text-white m-3 text-center shrink font-normal">
                    While my current hobbies are debating, video gaming and weightlifting, programming is my first love 🤍
                </p>
            </div>
                <Button tag={"Github Link"} link={"https://github.com/Wen-pen"}/>
                <Link to="/projects">
                <button class="bg-gradient-to-r from-[#DEE4EA] to-[#F9FCFF] rounded-lg shadow-lg p-3 font-semibold text-gray-400 mx-3 my-3">
                    My Projects
                </button>
                </Link>
                <Link to="/contacts">
                    <button class="bg-gradient-to-r from-[#DEE4EA] to-[#F9FCFF] rounded-lg shadow-lg p-3 font-semibold text-gray-400 mx-3 my-3">
                        Contact Me
                    </button>
                 </Link>
        
        </div>
</main>

