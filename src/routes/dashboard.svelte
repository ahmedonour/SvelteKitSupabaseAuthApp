<script>
	export let user;
</script>

<div>
	<h3>This is protected route accesible only for ligged users</h3>
	<p>Hello user {user.email}</p>
</div>
<div>
	<p>User {user.email} details:</p>
	<!-- <pre>{JSON.stringify(user, null, 2)}</pre> -->
	<main>
		<h1>Hello {user.email}</h1>
	</main>
</div>
<style>
	main{
		width: 100vw;
		height: 50vh;
		background-color: brown;
		display: grid;
		place-items: center;
	}
	main h1{
		color: aliceblue;
		font-family:  Helvetica, sans-serif;

	}

</style>
