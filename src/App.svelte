<script lang="ts">
	import Feedbacklist from './components/FeedbackList.svelte'
	import FeedbackStats from './components/FeedbackStats.svelte'

	let feedback = [
		{
			id: '1',
			rating: '10',
			text: 'Qui aute ex esse ea enim do nostrud reprehenderit cillum cupidatat consequat.',
		},
		{
			id: '2',
			rating: '6',
			text: 'Qui aute ex esse ea enim do nostrud reprehenderit cillum cupidatat consequat.',
		},
		{
			id: '3',
			rating: '9',
			text: 'Qui aute ex esse ea enim do nostrud reprehenderit cillum cupidatat consequat.',
		}
	]

	$: count = feedback.length
	$: average = feedback.reduce((a, {rating}) => a + rating, 0) / feedback.length
	$: averagerounded = average.toFixed(2);
	
	const deleteFeedback = (e) => {
		const	 itemId = e.detail
		feedback = feedback.filter((item) => item.id != itemId)
	}
</script>

<main class="container">
	<FeedbackStats {count} {averagerounded}/>
	<Feedbacklist {feedback} on:delete-feedback=
	{deleteFeedback}/>
</main>
