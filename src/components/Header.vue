<template>
    <div class="container">
        <h2>Quotes</h2>
        {{quoteCount}}/{{MaxCount}}
        <div class="progress">
            <div class="progress-bar" role="progressbar" aria-valuenow="70" aria-valuemin="0" aria-valuemax="100" 
            :style="{width: (quoteCount) / (MaxCount) *100 + '%'}">
            <!-- <span class="sr-only">70% Complete</span> -->
            
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        props: ['quoteCount', 'MaxCount']
    }
    
</script>

<style>

</style>
