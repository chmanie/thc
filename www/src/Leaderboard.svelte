<script lang="ts">
  import { address } from "./stores/burnerWallet";
  import { leaderboard, ensAddresses } from "./stores/thc";
  import Leaderboard from "./components/Leaderboard.svelte";
</script>

{#if $leaderboard && $address && $ensAddresses}
  <Leaderboard
    address={$address}
    ensAddresses={$ensAddresses}
    leaderboard={$leaderboard}
  />
{/if}
