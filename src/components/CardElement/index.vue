<template>
    <div class="card">
        <h3>{{title}}</h3>
        <p>
            {{description}}
        </p>
    </div>
</template>

<script>

export default {
    name: 'CardElement',
    props: {
        title: String,
        description: String
    }
}
</script>