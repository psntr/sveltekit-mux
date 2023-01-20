<script context="module">
    export const prerender = true;
</script>

<script>
    // this prevents the custom elements from being redefined when the REPL is updated and reloads, which throws an error
    // this means that any changes to the custom element won't be picked up without saving and refreshing the REPL
    // const oldRegister = customElements.define;
    // customElements.define = function(name, constructor, options) {
    //  if (!customElements.get(name)) {
    //      oldRegister(name, constructor, options);
    //  }
    // }
    // import { page } from '$app/stores';
    import { onMount } from 'svelte';
    onMount(async () => {
        await import('@mux/mux-player');
    });
</script>

<mux-player
    playback-id="FuJSYrK0014ec2LPnm11bzC2MAySAQPqA"
    stream-type="on-demand"
/>