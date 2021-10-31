<template>
    <div>
        <h2>Blog Detail</h2>
        <p>これは、{{ $route.params.id }}のページです。</p>
    </div>
</template>
<script>
export default {
    validate({ params }){
        return /^\d+$/.test(params.id) //数字のみ
    }
}
</script>
