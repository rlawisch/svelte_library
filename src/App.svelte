<script>
	import { Router, Route } from "svelte-routing";

	import Library from "./library/Library.svelte";
	import Detail from "./detail/Detail.svelte";
	import Create from "./create/Create.svelte";

	export let url = '';
</script>

<Router {url}>
	<main>
		<Route path="/">
			<Library />
		</Route>
		<Route path="/books/:id" let:params>
			<Detail id={params.id} />
		</Route>
		<Route path="create">
			<Create />
		</Route>
	</main>
</Router>
