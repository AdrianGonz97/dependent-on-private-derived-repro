<script lang="ts">
	class SomeState {
		opts: { baz: boolean };
		#foo = $derived.by(() => this.opts.baz);

		constructor(opts: { baz: boolean }) {
			this.opts = opts;
		}
	}

	new SomeState({ baz: true });
</script>
