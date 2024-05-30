<script>

export default {
    name: 'AppMain',
    data() {
        return {
        products: [
            {
                visible: "/img/1.webp",
                invisible: "/img/1b.webp",
                brand: "Levi's",
                name: "RELAXED FIT TEE UNISEX",
                newprice: "14,99 €",
                oldprice: "29,99 €",
                discount: "-50%",
                label: "Sostenibilità",
            },
            {
                visible: "/img/2.webp",
                invisible: "/img/2b.webp",
                brand: "Guess",
                name: "ROSES TEE",
                newprice: "20,99 €",
                oldprice: "29,99 €",
                discount: "-30%",
                label: "",
            },
            {
                visible: "/img/3.webp",
                invisible: "/img/3b.webp",
                brand: "Come Zucchero Filato",
                name: "VOGLIA DI COLORI PASTELLO",
                newprice: "129,99 €",
                oldprice: "184,99 €",
                discount: "-30%",
                label: "",
            },
            {
                visible: "/img/4.webp",
                invisible: "/img/4b.webp",
                brand: "Levi's",
                name: "TEE UNISEX",
                newprice: "14,99 €",
                oldprice: "29,99 €",
                discount: "-50%",
                label: "Sostenibilità",
            },
            {
                visible: "/img/5.webp",
                invisible: "/img/5b.webp",
                brand: "Maya Deluxe",
                name: "STRIPE BODICE",
                newprice: "99,99 €",
                oldprice: "",
                discount: "",
                label: "Luxury",
            },
            {
                visible: "/img/6.webp",
                invisible: "/img/6b.webp",
                brand: "Esprit",
                name: "MAGLIONE - BLACK",
                newprice: "29,99 €",
                oldprice: "",
                discount: "",
                label: "Sostenibilità",
            },
        ]
        };
    },

    methods: {

    },
}

</script>

<template>
    <div class="container">
        <div class="row">

            <div class="col-33" v-for="product in products">
                <div class="content margin-top-80">
                    <div class="images">
                        <img class="visible-image" :src="product.visible" alt="img">
                        <img class="invisible-image" :src="product.invisible" alt="img">
                    </div>
                    

                    <div class="labels">
                        <div class="red-bg p-5"><span>{{ product.discount }}</span></div>
                        <div class="green-bg p-5"><span> {{  product.label }}</span></div>
                    </div>

                    <div class="clothes-info position-relative">
                        <h4> {{ product.brand }}</h4>
                        <h3> {{  product.name }}</h3>
                        <span class="red-txt"> {{  product.newprice }} </span> <span style="text-decoration: line-through;"> {{  product.oldprice }} </span>
                    </div>

                    <div class="red-heart position-relative">
                        &#10084
                    </div>
                </div>
            </div>

        </div> 
    </div>    
</template>

<style lang="scss" scoped>

$red_color: red;

.content img {
    width: 100%;
}

.labels {
    color: white;
    font-weight: bold;
    display: flex;
    gap: 10px;
    font-size: 13px;
}

.p-5 {
    padding: 5px;
}

.red-bg {
    background-color: $red_color;
    position: relative;
    bottom: 60px;
}

.green-bg {
    background-color: green;
    position: relative;
    bottom: 60px;
}

.red-txt {
    color: $red_color;
}

.clothes-info span {
    font-size: 14px;
    font-weight: bold;
}


.visible-image {
    width: 100%;
}

.invisible-image {
    display: none;
}

.images:hover .invisible-image{
    display: block;
    margin-bottom: 4px;
}

.images:hover .visible-image {
    display: none;
}

.position-relative {
    position: relative;
}

.clothes-info {
    bottom: 25px;
}

.red-heart {
    bottom: 600px;
    left: 340px;
    background-color: rgb(255, 255, 255);
    padding: 10px;
    width: 33px;
}

.red-heart:hover {
    color: $red_color;
}

</style>