<script>
    import { createEventDispatcher } from "svelte";
    const dis = createEventDispatcher();

    function clickDispatch(){
        dis('message',{
            Text:"Lorem ipsum dolor sit amet consectetur adipisicing elit Fugiat dolorum suscipit quo eaque eum, perspiciatis minima nulla corrupti deserunt in,aliquam aperiam nihil praesentium rem laudantium illo. Veritatis, asperiores expedita? ",
        })
    }
</script>
<main>
    <button on:click={clickDispatch}> For dispatcher example click here</button>
    
</main>