<script lang="ts">
  const icons: string[] = [
    "fa-bold",
    "fa-italic",
    "fa-underline",
    "fa-image",
    "fa-link",
    "fa-align-left",
    "fa-align-center",
    "fa-align-right",
    "fa-video",
    "fa-code",
    "fa-brands fa-youtube",
    "fa-list",
    "fa-list-ol"
  ];

  const ButtonAction = (ButtonName: string) => {
    console.log(ButtonName);
  };

  const handleSelect = (e: Event) => {
    const target = e.target as HTMLSelectElement;
    console.log(target.value);
  };
</script>


<h1 class="h-16 text-2xl grid place-items-center bg-slate-800 text-white">
  Edit your Blogs here
</h1>

<div class="bg-gray-400 flex items-center p-4 gap-4 flex-wrap">


  <select id="font-selector" on:change={handleSelect} class="border border-gray-300 rounded px-4 py-2">
    <option value="Roboto">Roboto</option>
    <option value="Arial">Arial</option>
    <option value="Verdana">Verdana</option>
    <option value="Helvetica">Helvetica</option>
    <option value="Times New Roman">Times New Roman</option>
    <!-- Add more font options here -->
  </select>



  {#each icons as icon}
    <button on:click={()=>ButtonAction(icon)}
      class="fa-solid {icon} p-2 bg-slate-50 focus:bg-black focus:text-slate-50 rounded-md"
    ></button>
  {/each}



  </div>

<style>
  .fa-solid {
    transition: all 0.2s linear;
  }
</style>
