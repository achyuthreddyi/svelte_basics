<script>
	import '../node_modules/materialize-css/dist/css/materialize.min.css'
	import '../node_modules/materialize-css/dist/js/materialize.min.js'
	 import { Router,  Route } from "svelte-routing";
	 import Navbar from './layout/Navbar.svelte'
	 import home from './pages/home.svelte'
	 import about from './pages/about.svelte'
		
</script>

<!-- <main>
	<h1> hello {name}  </h1>
</main> -->

<style>
	

</style>

<Router>
<Navbar/>
<div class = "container">
 <Route path="/" component={home} />
 <Route path="/about" component={about} />

</div>


</Router>