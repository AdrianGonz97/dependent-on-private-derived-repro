<script lang="ts">
	class SomeState {
		opts: { baz: boolean };
		#foo = $derived.by(() => this.opts.baz);
		bar = $derived.by(() => ({ foo: this.#foo }));

		constructor(opts: { baz: boolean }) {
			this.opts = opts;
		}
	}

	let some_state = new SomeState({ baz: true });
</script>

{some_state.bar.foo}
