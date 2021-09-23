<template>
	<b-container>
		<b-row class="justify-content-center">
			<h3>Sign In</h3>
			<b-col cols="sm-4">
				<label>Email address</label>
				<input type="email" class="form-control form-control-lg" />
			
				<div class="form-group">
					<label>Password</label>
					<input type="password" class="form-control form-control-lg" />
				</div>
				
				<button type="submit" class="btn btn-dark btn-lg btn-block my-2">Sign In</button>
			</b-col>
		</b-row>
	</b-container>
</template>

<script>
    export default {
		name: "Login"
    }
</script>
