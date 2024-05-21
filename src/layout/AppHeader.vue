<template>
    <header class="header-global">
        <base-nav class="" transparent type="default" effect="light" expand>
            <router-link slot="brand" class="navbar-brand mr-lg-5" to="/">
                <img src="//llm4eda.oss-cn-hangzhou.aliyuncs.com/img/brand/LLM4EDA.png" alt="logo">
                <!-- <span>MemX</span> -->
            </router-link>

            <div class="row" slot="content-header" slot-scope="{closeMenu}">
                <div class="col-6 collapse-brand">
                    <router-link to="/">
                        <img src="//memx-website.oss-cn-shanghai.aliyuncs.com/img/brand/blue.png">
                    </router-link>
                </div>
                <div class="col-6 collapse-close">
                    <close-button @click="closeMenu"></close-button>
                </div>
            </div>

            <ul class="navbar-nav navbar-nav-hover align-items-lg-center ml-lg-auto">
                <nav>
                    <button class="btn btn-primary" @click="scrollToApplySection">Apply</button>
                </nav>
                <li class="nav-item">
                    <router-link to="/" class="nav-link nav-link-icon">
                        <!-- <i class="fa fa-home" style="font-size: 1.1rem;"></i> -->
                        <span class="nav-link-inner--text">Home</span>
                    </router-link>
                </li>
                <!-- <li class="nav-item">
                    <router-link to="/about" class="nav-link nav-link-icon">
                        <span class="nav-link-inner--text">About</span>
                    </router-link>
                </li> -->
            </ul>
        </base-nav>
    </header>
</template>
<script>
import BaseNav from "@/components/BaseNav";
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";

export default {
    components: {
        BaseNav,
        CloseButton,
        BaseDropdown
    },
    methods: {
        scrollToApplySection() {
            // Emit an event named "scroll-to-apply" when the button is clicked
            this.$root.$emit('scroll-to-apply');
        }
    }
};
</script>
<style></style>
