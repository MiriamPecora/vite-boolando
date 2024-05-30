<script></script>

<template>

<div class="container header">
            <div class="row">
                <div class="col-100 header-footer-flex">
                    <div id="left-header">
                        <ul>
                            <li>Donna</li>
                            <li>Uomo</li>
                            <li>Bambini</li>
                        </ul>
                    </div>
                    <div id="center-header">
                        <img src="/img/boolean-logo.png" alt="">
                    </div>
                    <div id="right-header">
                        <img src="/img/user.png" alt="user">
                        <img src="/img/header_heart.png" alt="favorite">
                        <img src="/img/shopping_bag.png" alt="shopping bag">
                    </div>
                </div>
            </div>
        </div>


</template>

<style scoped>
.header {
    background-color: rgb(248, 111, 32);
    position: fixed;
    width: 100%;
    z-index: 1;
}

#left-header {
    font-size: 15px;
}

#center-header img {
    width: 110px;
}

#right-header img {
    width: 17px;
    margin-right: 5px;
}

</style>