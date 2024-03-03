<script>
    import Card from "./Card.svelte";
    export let item
</script>

<Card>
    <div class="num-display">
        {item.rating}
    </div>
    <div class="close">X</div>
    <p>
        {item.text}
    </p>
</Card>

<!-- stopped at 30:07 -->
