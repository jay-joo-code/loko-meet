<script lang="ts">
	import PageContainer from '$lib/glue/components/PageContainer.svelte';
	import TextInput from '$lib/glue/components/TextInput.svelte';
	import DatePicker from '$lib/glue/components/DatePicker.svelte';
	import { addDays } from 'date-fns';

	let name = '';
	let startDate = new Date();
	let endDate = addDays(new Date(), 7);
</script>

<PageContainer title="Create event">
	<div class="space-y-4">
		<p>Create event</p>
		<TextInput label="Event name" bind:value={name} />
		<div class="flex space-x-4">
			<DatePicker bind:value={startDate} label="Start date" />
			<DatePicker bind:value={endDate} label="End date" />
		</div>
	</div>
</PageContainer>
