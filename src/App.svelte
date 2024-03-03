<script>
	import FeedbackList from "./components/FeedbackList.svelte";

		let feedback = [
			{
				id: 1,
				rating: 9,
				text: 'Vivamus posuere lorem tempor, lacinia nibh ut, consectetur felis. In congue mauris quam, a suscipit orci pharetra eget. Phasellus in ipsum a eros feugiat auctor at vel purus.' 
			},
			{
				id: 2,
				rating: 5,
				text: 'Vivamus posuere lorem tempor, lacinia nibh ut, consectetur felis. In congue mauris quam, a suscipit orci pharetra eget. Phasellus in ipsum a eros feugiat auctor at vel purus.' 
			},
			{
				id: 3,
				rating: 7,
				text: 'Vivamus posuere lorem tempor, lacinia nibh ut, consectetur felis. In congue mauris quam, a suscipit orci pharetra eget. Phasellus in ipsum a eros feugiat auctor at vel purus.' 
			},
		]
</script>

<main>
	<FeedbackList {feedback} />
</main>
