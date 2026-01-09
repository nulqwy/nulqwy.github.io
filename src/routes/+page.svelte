<script lang="ts">
	import { m } from '$lib/paraglide/messages.js';
	import LineBreak from '../lib/decorations/LineBreak.svelte';
	import LinkCard from '../lib/LinkCard.svelte';
	import Section from '../lib/Section.svelte';
	import Paragraph from '../lib/text/Paragraph.svelte';
	import Text from '../lib/text/Text.svelte';
	import Title from '../lib/text/Title.svelte';

	import gh_logo from '$lib/assets/icons/github-mark-white.svg';
	import dc_logo from '$lib/assets/icons/discord-mark-white.svg';
	import tg_logo from '$lib/assets/icons/telegram-white-icon.svg';
</script>

<div class="mt-5 text-center">
	<Title>{m.about_whom()}</Title>
	<Text>{m.short_desc()}</Text>
</div>

<div class="my-12">
	<Section name={m.section_socials()} flex>
		<LinkCard href="https://github.com/nulqwy" desc="github" icon={gh_logo} />
		<LinkCard href="https://discord.com/users/565207149618135042" desc="discord" icon={dc_logo} />
		<LinkCard href="https://t.me/nulqwy" desc="telegram" icon={tg_logo} />
	</Section>

	<Section name={m.section_projects()} flex>
		<Text>
			{@html m.no_projects()}
		</Text>
	</Section>
</div>

<LineBreak />

<Section name="info" separator={false}>
	<Paragraph name={m.info_about_title()}>{m.info_about()}</Paragraph>

	<Paragraph name={m.info_hobbies_title()}>{m.info_hobbies()}</Paragraph>

	<Paragraph name={m.info_knowledge_title()}>{@html m.info_knowledge()}</Paragraph>
</Section>
