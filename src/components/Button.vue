<script setup>
    // Pasar los props a el elemento
    // 1ra forma --> const props = defineProps(['operador']) - se le pasa un array
    // 2da forma -- mas facil de leer, se le pasa como objeto y se define el tipo de dato
    const props = defineProps({
        operador: String,
        fn: Function
    })
</script>

<template>
    <button
        type="button"
        class="h-10 w-10 flex items-center justify-center font-bold bg-lime-500 rounded-full hover:outline-none hover:ring-2 hover:ring-offset-2 hover:ring-lime-500 text-white text-2xl"
        @click="$emit('fn')"
    > {{ operador }} </button>
</template>