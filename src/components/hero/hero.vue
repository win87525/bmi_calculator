<template>
    <section>
        <div>
            <div class="titleBox">
                <h1>Body Mass
                    Index Calculator
                </h1>
                <p>Better understand your weight in relation to your height using our body mass index (BM) calculator.
                    While BMI is not the sole determinant of a healthy weight, it offers a valuable starting point to
                    evaluate your overall health and well-being.</p>
            </div>
            <div class="bmiBox">
                <h3>Enter your details below</h3>
                <div>
                    <div class="switchBtn">
                        <input type="checkbox" id="Metric" name="switchBtn" v-model="metric_checked">
                        <label for="Metric">Metric</label>
                    </div>
                    <div class="switchBtn">
                        <input type="checkbox" id="Imperial" name="switchBtn" v-model="imperial_checked">
                        <label for="Imperial">Imperial</label>
                    </div>
                </div>
                <div v-if="metric_checked">
                    <div class="input_box">
                        <p class="body-s">Height</p>
                        <div>
                            <input type="number" placeholder="0" id="height" maxlength="5">
                            <label for="height" class="heading-m">cm</label>
                        </div>
                    </div>
                    <div class="input_box">
                        <p class="body-s">Weight</p>
                        <div>
                            <input type="number" placeholder="0" id="weight" maxlength="5">
                            <label for="weight" class="heading-m">kg</label>
                        </div>
                    </div>
                </div>
                <div class="results" v-if="metric_checked">
                    <h3>Welcome！</h3>
                    <p>Enter your height and weight and you’ll see your BMI result here</p>
                </div>
            </div>
            <figure>
                <img src="../../assets/img/logo.svg" alt="">
            </figure>
        </div>
    </section>
</template>
<script setup>
import { ref, watch } from 'vue';

const metric_checked = ref(true);
const imperial_checked = ref(false);

watch(metric_checked, (newValue) => {
    if (newValue) {
        imperial_checked.value = false;
    }
});

watch(imperial_checked, (newValue) => {
    if (newValue) {
        metric_checked.value = false;
    }
});
</script>

<style scoped>
@import '/src/assets/css/hero.css';
</style>
