<script lang="ts">
export let icon: string;
export let title: string;
</script>

<div
  class="bg-card text-card-foreground border rounded-lg shadow-lg overflow-hidden max-w-md mx-auto my-2 min-w-[11rem]"
  data-v0-t="card"
>
  <div class="flex flex-col space-y-1.5 bg-gray-100 dark:bg-gray-800 dark:text-white p-4">
    <div class="flex items-center justify-center space-x-4">
	  <iconify-icon {icon} width="2rem" height="2rem"></iconify-icon>
      <h3 class="tracking-tight text-lg font-bold">{title}</h3>
    </div>
  </div>
</div>
