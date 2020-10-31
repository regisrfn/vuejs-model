<template>
<div class="header" :class="{ scrollClass: isActive }">
    <VueLogo class="logo" alt="logo" />
    <nav>
        <ul class="header__links hidden-menu" :class="{ checked: isChecked }">
            <li>
                <router-link to="/">Home</router-link>
            </li>
            <li>
                <a href="#">Information</a>
            </li>
            <li>
                <router-link to="/about">About</router-link>
            </li>
            <button>Services</button>
        </ul>
    </nav>
    <nav>
        <ul class="header__links header__register">
            <li>
                <a href="#">Login</a>
            </li>
            <li>
                <a href="#">Register</a>
            </li>
        </ul>
    </nav>

    <input v-model="isChecked" type="checkbox" class="header__btn" id="navbar-btn" />
    <label for="navbar-btn" class="navbar-icon" :class="{ checked: isChecked }">
        <span class="navbar-icon__line"></span>
    </label>
</div>
</template>

<script>
import VueLogo from "@/img/logo.svg";

export default {
    data() {
        return {
            isActive: false,
            isChecked: false,
        };
    },
    components: {
        VueLogo,
    },
    created() {
        window.addEventListener("scroll", this.handleScroll);
    },
    destroyed() {
        window.removeEventListener("scroll", this.handleScroll);
    },
    methods: {
        handleScroll(event) {
            const scrollY = window.scrollY;
            if (scrollY > 10) {
                this.isActive = true;
            } else {
                this.isActive = false;
            }
        },
    },
};
</script>
