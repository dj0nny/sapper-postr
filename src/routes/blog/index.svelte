<script>
import Post from '../../components/Post.svelte'

const baseURL = 'http://jsonplaceholder.typicode.com/posts'

let posts = []

async function fetchPosts() {
	const res = await fetch('https://jsonplaceholder.typicode.com/posts')
	posts = await res.json()
	console.log(posts)
}

fetchPosts()

</script>

<style>
.post {
  display: inline-block;
  width: 30%;
  padding: 7px;
  border: 1px solid;
  margin: 5px;
  text-align: center;
}
</style>

<svelte:head>
	<title>Blog</title>
</svelte:head>

<h1>Recent posts</h1>

<div class="posts-container">
	{#each posts as post}
		<div class="post">
			<Post post={post}></Post>
		</div>
	{/each}
</div>