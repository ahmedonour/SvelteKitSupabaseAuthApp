<script>
	export let user;
</script>

<div>
	<h3>This is protected route accesible only for ligged users</h3>
	<p>Hello user {user.email}</p>
</div>
<div>
	<p>User {user.email} details:</p>
	<pre>{JSON.stringify(user, null, 2)}</pre>
</div>
