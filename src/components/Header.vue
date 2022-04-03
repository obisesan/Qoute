<template>
    <div class="row">
        <div class="col-sm-12">
        <h3>Quotes Added</h3>
        <div class="progress">
            <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemax="100" aria-valuemin="0"
            :style="{width:(qouteCount / maxQoute * 100 + '%')}">
                 {{qouteCount}} / {{maxQoute}}
            </div>
        </div>
        </div>
    </div>
</template>
<script>
export default {
   props:['qouteCount', 'maxQoute'],
}
</script>
<style scoped>

</style>