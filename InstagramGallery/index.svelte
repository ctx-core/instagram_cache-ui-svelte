<script>
import { FA_chevron_left_solid, FA_chevron_right_solid } from '@ctx-core/fontawesome-ui-svelte'
import { medium_pathname__, medium_pathname_idx$_ } from '@ctx-core/instagram_cache'
/** @type {import('@ctx-core/be').ctx_T} */
export let ctx
const medium_pathname_ = medium_pathname__(ctx)
const medium_pathname_idx_ = medium_pathname_idx$_(ctx)
/** @type {string} */
let img_src
$: img_src = `https://instagram.com${$medium_pathname_}media/?size=l`
</script>

<div class="InstagramGallery">
	<div class="prev button" on:click={medium_pathname_idx_.medium_pathname_idx$_prev}>
		<FA_chevron_left_solid></FA_chevron_left_solid>
	</div>
	<div class="media">
		<img src={img_src} alt="">
	</div>
	<div class="next button" on:click={medium_pathname_idx_.medium_pathname_idx$_next}>
		<FA_chevron_right_solid></FA_chevron_right_solid>
	</div>
</div>
