<template>
    <div class="PolaroidSingle">
        <div class="PolaroidSingle_content">
            {{ title }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'PolaroidSingle',
    props: {
        title: { type: String }
    }
}
</script>

<style lang="scss" scoped>
.PolaroidSingle {
    position: relative;
    border: 4px solid var(--color-sugar);
    border-bottom: none;

    &:last-child {
        border-bottom: 4px solid var(--color-sugar);
    }

    &::before {
        content: "";
        display: block;
        padding-bottom: 100%;
    }
}

.PolaroidSingle_content {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;

    font: var(--ft-xl);
    font-weight: bold;
    color: var(--color-sugar);
    padding: 20px;

    background: linear-gradient(to bottom, rgba(0, 0, 0, 0), var(--color-coal))
}
</style>