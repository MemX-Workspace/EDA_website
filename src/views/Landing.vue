<template>
    <div>
        <hero></hero>

        <section class="section bg-secondary">
            <div class="container">
                <div class="row text-center justify-content-center">
                    <!-- <div class="col-lg-10"> -->
                        <!-- <h2 class="display-3">Build something</h2> -->
                        <p class="lead">MemX defines wearable and interactive AGI, a unification of wearable technology and artificial general intelligence (AGI), MemX aims to advance the human-centered computing pathway from human perception, emotion, cognition, and finally, also hopefully, towards human-centered AGI.</p>
                    <!-- </div> -->
                </div>
            </div>
        </section>

        <section class="section">
            <div class="container">
                <div class="row">

                    <div class="col-md-6 col-lg-4 mb-5 mb-lg-0">
                        <div class="px-4">
                            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Professor</div>
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Li_Shang.jpg'"
                                 class="rounded img-center img-fluid shadow shadow-lg--hover"
                                 style="width: 200px; object-fit:cover;">
                            <div class="pt-4 text-center">
                                <h5 class="title">
                                    <span class="d-block mb-1">Li Shang</span>
                                    <small class="h6 text-muted">Professor</small>
                                </h5>
                                <div class="mt-3">
                                    <base-button tag="a" href="https://cscw.fudan.edu.cn/lishang/list.htm" target="_blank" type="info" icon="fa fa-dribbble" rounded icon-only></base-button>
                                    <base-button tag="a" href="mailto:lishang@fudan.edu.cn" target="_blank" type="primary" icon="fa fa-send" rounded icon-only></base-button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- <div class="col-md-6 col-lg-3 mb-5 mb-lg-0">
                        <div class="px-4">
                            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Co-directors</div>
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Yingying_Zhao.jpg'"
                                 class="rounded img-center img-fluid shadow shadow-lg--hover"
                                 style="width: 200px; object-fit:cover;">
                            <div class="pt-4 text-center">
                                <h5 class="title">
                                    <span class="d-block mb-1">Yingying Zhao</span>
                                    <small class="h6 text-muted">Postdoc</small>
                                </h5>
                                <div class="mt-3">
                                    <base-button tag="a" href="https://cscw.fudan.edu.cn/yingyingzhao/list.htm" target="_blank" type="info" icon="fa fa-dribbble" rounded icon-only></base-button>
                                </div>
                            </div>
                        </div>
                    </div> -->

                    <div class="col-md-6 col-lg-4 mb-5 mb-lg-0">
                        <div class="px-4">
                            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Collaborators</div>
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Mingzhi_Dong.jpg'"
                                 class="rounded img-center img-fluid shadow shadow-lg--hover"
                                 style="width: 200px; object-fit:cover;">
                            <div class="pt-4 text-center">
                                <h5 class="title">
                                    <span class="d-block mb-1">Mingzhi Dong</span>
                                    <small class="h6 text-muted">Postdoc</small>
                                </h5>
                                <div class="mt-3">
                                    <base-button tag="a" href="https://cscw.fudan.edu.cn/mingzhidong/list.htm" target="_blank" type="info" icon="fa fa-dribbble" rounded icon-only></base-button>
                                    <base-button tag="a" href="mailto:mingzhidong@gmail.com" target="_blank" type="primary" icon="fa fa-send" rounded icon-only></base-button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-md-6 col-lg-4 mb-5 mb-lg-0">
                        <div class="px-4">
                            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">&nbsp;</div>
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Yuhu_Chang.jpg'"
                                 class="rounded img-center img-fluid shadow shadow-lg--hover"
                                 style="width: 200px; object-fit:cover;">
                            <div class="pt-4 text-center">
                                <h5 class="title">
                                    <span class="d-block mb-1">Yuhu Chang</span>
                                    <small class="h6 text-muted">Postdoc</small>
                                </h5>
                                <div class="mt-3">
                                    <base-button tag="a" href="https://cscw.fudan.edu.cn/yhchang/list.htm" target="_blank" type="info" icon="fa fa-dribbble" rounded icon-only></base-button>
                                    <base-button tag="a" href="mailto:yuhu@memx.life" target="_blank" type="primary" icon="fa fa-send" rounded icon-only></base-button>
                                </div>
                            </div>
                        </div>
                    </div>
<!--                     
                    <div class="col-sm-3 col-6">
                        <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Professor</div>
                        <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Li_Shang.jpg'" alt="Prof. Shang" class="img-fluid rounded shadow-lg" style="width: 150px;">
                    </div>
                    <div class="col-sm-3 col-6">
                        <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Collaborators</div>
                        <a href="http://yingyingzhao.com/">
                        <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Yingying_Zhao.jpg'" alt="" class="img-fluid rounded shadow" style="width: 150px;"></a>
                    </div>
                    <div class="col-sm-3 col-6 mt-5 mt-sm-0">
                        <div class="d-block text-uppercase font-weight-bold mb-4" style="font-size: 1.5rem;">&nbsp;</div>
                        <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Mingzhi_Dong.jpg'" alt="" class="img-fluid rounded shadow" style="width: 150px;">
                    </div>
                    <div class="col-sm-3 col-6 mt-5 mt-sm-0">
                        <div class="d-block text-uppercase font-weight-bold mb-4" style="font-size: 1.5rem;">&nbsp;</div>
                        <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/Yuhu_Chang.jpg'" alt="" class="img-fluid rounded shadow" style="width: 150px;">
                    </div> -->
                </div>
            </div>
        </section>


        <section id="works" class="section bg-secondary" style="margin-top: 2rem;">
            <div class="container">
                <div class="row row-grid align-items-center">
                    <div class="col-md-12 order-md-2">
                        <img src="//memx-website.oss-cn-shanghai.aliyuncs.com/img/slide/intro.png" class="img-fluid floating">
                    </div>
                </div>
            </div>
        </section>
        

        <section id="works" class="section">
            <div class="container">
                <div class="row row-grid align-items-center">
                    <!-- <div class="col-md-6">
                        <div class="card bg-default shadow border-0">
                            <img v-lazy="'img/slide/attention.png'" class="card-img-top">
                            <blockquote class="card-blockquote">
                                <svg preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 583 95"
                                     class="svg-bg">
                                    <polygon points="0,52 583,95 0,95" class="fill-default"></polygon>
                                    <polygon points="0,42 583,95 683,0 0,95" opacity=".2" class="fill-default"></polygon>
                                </svg>
                                <h4 class="display-3 font-weight-bold text-white">Memorable Moments</h4>
                                <p class="lead text-italic text-white">in Daily Life</p>
                            </blockquote>
                        </div>
                    </div> -->

                    <div class="col-md-6 order-md-2">
                        <img src="//memx-website.oss-cn-shanghai.aliyuncs.com/img/slide/attention.png" class="img-fluid floating">
                    </div>
                    
                    <div class="col-md-6 order-md-1">
                        <div class="pr-md-5">
                            <!-- <img width="100px" src="img/icons/memx/attention.png" style="margin-bottom: 2rem;"> -->
                            <h3 class="font-weight-extra-bold" style="color: #506cac">MemX4Attention</h3>
                            <span class="underline">See what you see</span>
                            <p class="font-weight-normal">Personalized moment auto-capturing</p>
                            <div class="mb-4"><span class="quote">
                                <img width="12px" src="img/icons/common/quote_leading.png" style="position: relative; top: -3px;">
                                Sharing the world in your eyes
                                <img width="12px" src="img/icons/common/quote_closing.png" style="position: relative; top: 3px;">
                            </span></div>
                            <!-- <a href="#" class="font-weight-bold text-warning mt-5">Explore more</a> -->
                            <router-link to="/pub">
                                <base-button tag="a" href="#" class="mb-3 mb-sm-0 btn-sm btn-round button-more border-none" type="default">
                                    Explore more
                                </base-button>
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="section bg-secondary">
            <div class="container">
                <div class="row row-grid align-items-center">
                    <div class="col-md-6 order-md-1">
                        <img src="//memx-website.oss-cn-shanghai.aliyuncs.com/img/slide/emotion.png" class="img-fluid floating">
                    </div>
                    <div class="col-md-6 order-md-2">
                        <div class="pl-md-5">
                            <!-- <img width="100px" src="img/icons/memx/emotion.png" style="margin-bottom: 2rem;"> -->
                            <h3 class="font-weight-extra-bold" style="color: #506cac">MemX4Emotion</h3>
                            <span class="underline">Feel what you feel</span>
                            <p class="font-weight-normal">Deep emotionship understanding</p>
                            <div class="mb-4"><span class="quote">
                                <img width="12px" src="img/icons/common/quote_leading.png" style="position: relative; top: -3px;">
                                Dreaming of sentiment visions
                                <img width="12px" src="img/icons/common/quote_closing.png" style="position: relative; top: 3px;">
                            </span></div>
                            <router-link to="/pub">
                                <base-button tag="a" href="#" class="mb-3 mb-sm-0 btn-sm btn-round button-more border-none" type="default">
                                    Explore more
                                </base-button>
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <div class="container">
                <div class="row row-grid align-items-center">
                    <div class="col-md-6 order-md-2">
                        <img src="//memx-website.oss-cn-shanghai.aliyuncs.com/img/slide/cognition.png" class="img-fluid floating">
                    </div>
                    <div class="col-md-6 order-md-1">
                        <div class="pl-md-5">
                            <!-- <img width="100px" src="img/icons/memx/cognition.png" style="margin-bottom: 2rem;"> -->
                            <h3 class="font-weight-extra-bold" style="color: #506cac">MemX4Cognition</h3>
                            <span class="underline">Think what you think</span>
                            <p class="font-weight-normal">Understanding your dogs</p>
                            <div class="mb-4"><span class="quote">
                                <img width="12px" src="img/icons/common/quote_leading.png" style="position: relative; top: -3px;">
                                Looking into the eyes of your dogs
                                <img width="12px" src="img/icons/common/quote_closing.png" style="position: relative; top: 3px;">
                            </span></div>
                            <router-link to="/pub">
                                <base-button tag="a" href="#" class="mb-3 mb-sm-0 btn-sm btn-round button-more border-none" type="default">
                                    Explore more
                                </base-button>
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <products></products>

        <section id="contact bg-secondary" class="section pt-lg-0 pb-lg-0 section-contact-us">
            <div class="container">
                
                <div class="row justify-content-center">
                    <div class="col-lg-8">
                        <card gradient="secondary" shadow body-classes="p-lg-5">
                            <h4 class="mb-1">Contact Us</h4>
                            <p class="mt-0">
                                <!-- Feel free to leave a message and place an order if you are interested. -->
                                Feel free to leave a message if you have any questions or feedback.
                                Please fill out the form below and we'll get in touch.
                            </p>
                            <form>
                                <div class="row">
                                    <div class="col-md-12">
                                        <div class="form-group"><div class="input-group">
                                            <div class="input-group-prepend">
                                                <span class="input-group-text"><i class="ni ni-user-run"></i></span>
                                            </div>
                                            <input type="text" class="form-control" id="name" placeholder="Your name" v-model="name">
                                        </div></div>
                                    </div>
                                </div>

                                <div class="row">
                                    <div class="col-md-12">
                                        <div class="form-group"><div class="input-group">
                                            <div class="input-group-prepend">
                                                <span class="input-group-text"><i class="ni ni-email-83"></i></span>
                                            </div>
                                            <input type="text" class="form-control" id="contact" placeholder="Email address or phone number" v-model="contact">
                                        </div></div>
                                    </div>
                                </div>
                                
                                <div class="row">
                                    <div class="col-md-12">
                                    <div class="form-group">
                                        <textarea class="form-control" id="message" rows="3" placeholder="Type a message..." v-model="message"></textarea>
                                    </div>
                                    </div>
                                </div>
                            </form>
<!-- 
                            <base-input class="mt-1"
                                        alternative
                                        placeholder="Your name"
                                        addon-left-icon="ni ni-user-run">
                            </base-input>
                            <base-input alternative
                                        placeholder="Email address"
                                        addon-left-icon="ni ni-email-83">
                            </base-input>
                            <base-input class="mb-4">
                                    <textarea class="form-control form-control-alternative" name="name" rows="4"
                                              cols="80" placeholder="Type a message..."></textarea>
                            </base-input> -->
                            <base-button type="default" round block size="lg" @click="submit">
                                {{tip}}
                            </base-button>

                            <!-- <div class="alert alert-success mt-2 text-center" role="alert">
                                Sent successfully
                            </div> -->
                        </card>
                    </div>
                </div>
            </div>
        </section>



        
    </div>
</template>

<script>
import Hero from "./components/Hero";
import Products from "./components/Products";

export default {
  name: "home",
  components: {
    Hero,
    Products
  },
  data: () => {
    return {
      name: '',
      contact: '',
      message: '',
      tip: 'Place Order'
    }
  },
  mounted() {
    this.$nextTick(function () {
      if ('/works' === this.$route.path || '/products' === this.$route.path) {
        // console.log(this.$route.path)
        const ref = this.$route.path.replace('/', '#')
        const el = document.querySelector(ref)
        if (el) {
          el.scrollIntoView(true)
        //   el.scrollIntoView({behavior: "smooth", block: "center", inline: "nearest"})
        }
      }
    })
  },
  methods: {
    submit: function (event) {
        if (!this.name) {
            this.tip = 'Please enter your name and send again'
        } else if (!this.contact) {
            this.tip = 'Please enter your contact and send again'
        } else if (!this.message) {
            this.tip = 'Please enter message and send again'
        } else {
            this.tip = 'Placing...'
            const AV = require('leancloud-storage');
            const { Query, User } = AV;
            AV.init({
            appId: "tQNLSFWLEcr2otLmMbz7vvUP-gzGzoHsz",
            appKey: "4s6pmNW3L1jizoK2YRag7aqk",
            serverURL: "https://tqnlsfwl.lc-cn-n1-shared.com"
            });
            const Message = AV.Object.extend('Message');
            const message = new Message();
            message.set('name', this.name);
            message.set('contact', this.contact);
            message.set('message', this.message);
            message.save().then((message) => {
                this.tip = 'Placed successfully'
            })
        }
    }
  }
};
</script>
