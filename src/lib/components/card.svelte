<script>
    import Button from "../components/button.svelte";
    export let link;
    export let title;
    export let description;
</script>
<div class="bg-gradient-to-l from-[#DEE4EA] to-[#7D8184] rounded-lg shadow-md bg-blend-black m-6 p-3" id="main">
    <h1 class=" font-extrabold text-2xl text-center p-3">
        {title}
    </h1>
    <p class="text-center text-l">
        {description}
    </p>
    <div class="lg:grid grid-cols-1 mx-3 text-center">
       <Button tag="Source Code" link={link}/>
    </div>
</div>