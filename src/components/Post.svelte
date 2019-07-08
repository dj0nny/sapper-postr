<script>
export let post
</script>

<style>
.post-title {
  margin-bottom: 10px;
}
</style>

<div class="post-wrapper">
  <div class="post-title">
			<strong class="title">{post.title}</strong>
  </div>
  <div class="post-body">
    {post.body}
  </div>
</div>