<script>
	import FeedbackList from "./components/FeedbackList.svelte";
	import FeedbackStats from "./components/FeedbackStats.svelte";

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

		$: count = feedback.length
		$: average = feedback.reduce((a, {rating})=> a + rating, 0)/feedback.length

		const deleteFeedback = (e)=>{
			const itemId =e.detail
			feedback = feedback.filter((item)=>item.id != itemId)
		}
</script>

<main class="container">
	<FeedbackStats {count} {average} />
	<FeedbackList {feedback} on:delete-feedback={deleteFeedback} />
</main>
