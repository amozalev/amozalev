<script lang="ts">
	import PostTitle from '../../../components/PostTitle.svelte';
	import MetaTags from '../../../components/MetaTags.svelte';

	export let data;

	$: ({ meta, content } = data);
</script>

<MetaTags
	title={meta.title}
	slug={meta.slug}
	description={meta.description ?? ''}
	ogImage={meta.ogImage}
	type="article"
/>

<PostTitle post={meta} />
<svelte:component this={content} />