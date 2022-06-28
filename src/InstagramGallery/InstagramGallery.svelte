<script lang="ts">
import { type Ctx } from '@ctx-core/object'
import { FA_chevron_left_solid, FA_chevron_right_solid } from '@ctx-core/fontawesome-ui-svelte'
import { medium_pathname__, medium_pathname_idx__ } from '@ctx-core/instagram_cache'
export let ctx:Ctx
const medium_pathname_ = medium_pathname__(ctx)
const medium_pathname_idx_ = medium_pathname_idx__(ctx)
let img_src//region
$: img_src = `https://instagram.com${$medium_pathname_}media/?size=l`//endregion
</script>

<div class="InstagramGallery">
	<div class="prev button" on:click={medium_pathname_idx_.prev_medium_pathname}>
		<FA_chevron_left_solid></FA_chevron_left_solid>
	</div>
	<div class="media">
		<img src="{img_src}" alt="">
	</div>
	<div class="next button" on:click={medium_pathname_idx_.next_medium_pathname}>
		<FA_chevron_right_solid></FA_chevron_right_solid>
	</div>
</div>
