<script lang="ts">
  import { moonState } from '$lib/moonState.svelte';

  function copyToClipboard() {
    navigator.clipboard.writeText(JSON.stringify(moonState)).catch((err) => {
      console.error('Could not copy text: ', err);
    });
  }
</script>

<button type="button" onclick={copyToClipboard} class="btn w-18" style:color="inherit" aria-label="Copy to clipboard">
  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
    <path
      fill="none"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="2"
      d="M8 5H6a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2v-1M8 5a2 2 0 0 0 2 2h2a2 2 0 0 0 2-2M8 5a2 2 0 0 1 2-2h2a2 2 0 0 1 2 2m0 0h2a2 2 0 0 1 2 2v3m2 4H10m0 0l3-3m-3 3l3 3"
    />
  </svg>
</button>
