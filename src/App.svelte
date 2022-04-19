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
	
</script>

<main>
	<Feedbacklist {feedback}/>
</main>
