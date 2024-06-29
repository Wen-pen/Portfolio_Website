<script>
  import { Router, Route } from "svelte-routing";
  import Home from "./lib/pages/home.svelte"
  import Projects from "./lib/pages/projects.svelte";
  import Contacts from "./lib/pages/contacts.svelte";
  export let url = ""
  </script>
  
  <Router {url}>
      <div>
          <Route path="/"><Home/></Route>
          <Route path="/projects"><Projects/></Route>
          <Route path="/contacts"><Contacts/></Route>
  
      </div>
  </Router>
  
   