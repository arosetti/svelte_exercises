<script>
  const emojis = {
    apple: "🍎",
    banana: "🍌",
    carrot: "🥕",
    doughnut: "🍩",
    egg: "🥚",
  };

  export let name;
  const emoji = emojis[name];
</script>

<p class="text-xl">{emoji} = {name}</p>
