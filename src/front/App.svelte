<script>
	import Router from 'svelte-spa-router';

	import ContactsTable from './ContactsTable.svelte';
	import EditContact from './EditContact.svelte';

	import NotFound from './NotFound.svelte';

	import Home from './Home.svelte';
	import GUI1 from './GUI1/Home.svelte';


	const routes = {
		"/": Home,
		"/contact/:contactName": EditContact,
		"/gui1": GUI1,
		"/gui2": GUI1,
		"*": NotFound
	};
</script>

<main>
	<h1>Contact Manager</h1>
	<Router {routes} />
	<ContactsTable></ContactsTable>
</main>