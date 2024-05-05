<template>
    <section>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </section>

</template>
<style scoped lang="scss">
@import '../assets/scss/base.scss';

section {
    padding: 0 10%;
    width: 100%;
    position: absolute;
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    gap: $gap;
    opacity: .1;
    z-index: -999;

    div {
        background: #b17272;
        width: 100%;
        height: 280rem;
    }
}
</style>