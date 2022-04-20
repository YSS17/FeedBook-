<script lang="ts">
	import Feedbacklist from './components/FeedbackList.svelte'

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
	
	const deleteFeedback = (e) => {
		const	 itemId = e.detail
		feedback = feedback.filter((item) => item.id != itemId)
	}
</script>

<main class="container">
	<Feedbacklist {feedback} on:delete-feedback=
	{deleteFeedback}/>
</main>
