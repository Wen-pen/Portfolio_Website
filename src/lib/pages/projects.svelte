<script>
    import { gsap } from "gsap/dist/gsap"
    import { onMount } from 'svelte'
    import { TextPlugin } from "gsap/dist/TextPlugin"
    import Nav from "../components/nav.svelte"
    import Card from "../components/card.svelte";
    let main  

    let globalRepoArr = [];

    let github_grabber = async () => {
    try {
        let response = await fetch("https://api.github.com/users/Wen-pen/repos");
        let repoParsed = await response.json();
        globalRepoArr.length = 0; // Clear the global array before updating
        for (const item of repoParsed) {
            let name = item.name;
            let description = item.description;
            let link = item.html_url
            let repoObj = { name: name, description: description, link: link };
            globalRepoArr.push(repoObj);
        }
    } catch (error) {
        console.error("An error occurred:", error);
        throw error;
    }
};

// Example usage:
github_grabber().then(() => {
    console.log(globalRepoArr); // The global array should now be updated
});
</script>

<main bind:this={main} class="min-h-screen bg-gradient-to-t from-[#DEE4EA] to-[#7D8184] text-white bg-blend-multiply font-poppins  text-wrap">
    <Nav/>
    <h1 class="text-center font-bold text-4xl p-3" id="main">
        My Projects
    </h1>
    <div class=" md:grid grid-cols-2 text-wrap" id="main">
       {#each globalRepoArr as repo}
            <Card title={repo.name} description={repo.description} link={repo.link}/>
       {/each}
    </div> 
</main>
