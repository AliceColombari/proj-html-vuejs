<template>
    <div class="section-card">
        <div class="my_container w-100 position-relative">
            <div class="image-container">
                <img :src="require(`../assets/image/${cardData.img}`)" alt="" class="w-100">

                <div class="text">
                    <div class="text-secondary fs-7">{{cardData.data}}</div>
                    <ul class="fs-5">
                        <li>{{cardData.title}}</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
export default {
    name: "SixSectionCard",
    props: {
        'cardData': Object
    }

}
</script>

<style scoped lang="scss">

.section-card {

    .image-container {
        overflow: hidden;

        img {
            box-shadow: 3px 3px 5px grey;
            border-radius: 10px;
            transition: transform 1s;
        }

        &:hover {
            transform: scale(1.1);
        }
    }

    .text {
        position: absolute;
        bottom: -10%;
        left: 50%;
        transform: translate(-50%, -50%);
        padding: 20px 0px 10px 20px;

        background-color: #fff;
        border-radius: 10px;
        box-shadow: 3px 3px 5px grey;
        width: 80%;

        ul li::marker {
            color: #00D9A6;
        }

    }

}


</style>