<template>
    <section class="section section-lg">
        <!-- <div class="shape shape-skew-gray">
        </div> -->

        <div class="container">
            <div class="mb-5">
                <h2>The Team</h2>
                <p class="font-weight-500">
                    MemX is an interdisciplinary research team across cognitive, social and computer sciences, conducting exploratory research on interactive visual intelligence. 
                    The MemX team consists of researchers from multiple universities and research labs worldwide, including Fudan University, University of Colorado, University of Michigan, University of Oxford, University of Glasgow, and Microsoft Research. 
                    Our goal is to advance the human-centered computing pathway from human perception, emotion, cognition, and finally, also hopefully, towards artificial general intelligence.
                </p>
            </div>
            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Team members</div>
            <div class="row">
                <div class="col-md-6 col-lg-2 mb-3" :class="{'cursor-pointer': person.url}" v-for="person in teams" :key="person.name" @click="open(person.url)">
                    <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                            class="img-center img-fluid shadow shadow-lg--hover"
                            style="width: 150px; height: 200px; object-fit:cover;">
                    <div class="pt-2 text-center">
                        <h5>{{person.name}}</h5>
                        <i class="fa fa-link" v-if="person.url"></i>
                        <!-- <small class="h6 text-muted">Professor</small> -->
                    </div>
                </div>
            </div>
            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Collaborators</div>
            <div class="row">
                <div class="col-md-6 col-lg-2 mb-3" :class="{'cursor-pointer': person.url}" v-for="person in collaborators" :key="person.name" @click="open(person.url)">
                    <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                            class="img-center img-fluid shadow shadow-lg--hover"
                            style="width: 150px; height: 200px; object-fit:cover;">
                    <div class="pt-2 text-center">
                        <h5>{{person.name}}</h5>
                        <i class="fa fa-link" v-if="person.url"></i>
                        <!-- <small class="h6 text-muted">Professor</small> -->
                    </div>
                </div>
            </div>
            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Students</div>
            <div class="row">
                <div class="col-md-6 col-lg-2 mb-3" :class="{'cursor-pointer': person.url}" v-for="person in students" :key="person.name" @click="open(person.url)">
                    <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                            class="img-center img-fluid shadow shadow-lg--hover"
                            style="width: 150px; height: 200px; object-fit:cover;">
                    <div class="pt-2 text-center">
                        <h5>{{person.name}}</h5>
                        <i class="fa fa-link" v-if="person.url"></i>
                        <!-- <small class="h6 text-muted">Professor</small> -->
                    </div>
                </div>
            </div>
            <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Alumnus</div>
            <div class="row">
                <div class="col-md-6 col-lg-2 mb-3" :class="{'cursor-pointer': person.url}" v-for="person in alumnus" :key="person.name" @click="open(person.url)">
                    <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                            class="img-center img-fluid shadow shadow-lg--hover"
                            style="width: 150px; height: 200px; object-fit:cover;">
                    <div class="pt-2 text-center">
                        <h5>{{person.name}}</h5>
                        <i class="fa fa-link" v-if="person.url"></i>
                        <!-- <small class="h6 text-muted">Professor</small> -->
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
export default {
  name: "about",
  data() {
    return {
      teams: [{
          'name': 'Li Shang',
          'photo': 'Li_Shang.jpg',
          'url': 'http://lishang.org/'
      }, {
          'name': 'Mingzhi Dong',
          'photo': 'Mingzhi_Dong.jpg',
          'url': 'https://cscw.fudan.edu.cn/mingzhidong/list.htm'
      }, {
          'name': 'Yingying Zhao',
          'photo': 'Yingying_Zhao.jpg',
          'url': 'http://yingyingzhao.com/'
      }, {
          'name': 'Yuhu Chang',
          'photo': 'Yuhu_Chang.jpg',
          'url': 'https://cscw.fudan.edu.cn/yhchang/list.htm'
      }],
      collaborators: [{
          'name': 'Qin Lv',
          'photo': 'Qin_Lv.jpg',
          'url': 'https://home.cs.colorado.edu/~lv/'
      }, {
          'name': 'Robert P. Dick',
          'photo': 'Robert_P._Dick.jpg',
          'url': 'https://robertdick.org/'
      }, {
          'name': 'Fan Yang',
          'photo': 'Fan_Yang.jpg',
          'url': 'https://sme.fudan.edu.cn/65/41/c31277a353601/page.htm'
      }, {
          'name': 'Ning Gu',
          'photo': 'Ning_Gu.jpg',
          'url': 'https://cscw.fudan.edu.cn/ninggu/list.htm'
      }, {
          'name': 'Tun Lu',
          'photo': 'Tun_Lu.jpg',
          'url': 'https://cscw.fudan.edu.cn/tunlu/list.htm'
      }, {
          'name': 'Dongsheng Li',
          'photo': 'Dongsheng_Li.jpg',
          'url': 'http://recmind.cn/index.html'
      }, {
          'name': 'Xianghua Ding',
          'photo': 'Xianghua_Ding.jpg',
          'url': 'https://xianghuading.com/'
      }, {
          'name': 'Yujiang Wang',
          'photo': 'Yujiang_Wang.jpg',
          'url': 'https://eng.ox.ac.uk/people/yujiang-wang/'
      }, {
          'name': 'Xiaochen Yang',
          'photo': 'Xiaochen_Yang.jpg',
          'url': 'https://www.gla.ac.uk/schools/mathematicsstatistics/staff/xiaochenyang/'
      }, {
          'name': 'Rui Zhu',
          'photo': 'Rui_Zhu.jpg',
          'url': 'https://www.bayes.city.ac.uk/faculties-and-research/experts/rui-zhu'
      }],
      students: [{
          'name': 'Zhenyu Xu',
          'photo': 'Zhenyu_Xu.jpg',
      }, {
          'name': 'Rui Zhang',
          'photo': 'Rui_Zhang.jpg',
      }, {
          'name': 'Zhouyang Lu',
          'photo': 'Zhouyang_Lu.jpg',
      }, {
          'name': 'Hailin Xu',
          'photo': 'Hailin_Xu.jpg',
      }, {
          'name': 'Yixuan Chen',
          'photo': 'Yixuan_Chen.jpg',
      }, {
          'name': 'Wentao Pan',
          'photo': 'Wentao_Pan.jpg',
      }, {
          'name': 'Changkai Fang',
          'photo': 'Changkai_Fang.jpg',
      }, {
          'name': 'Fang Dong',
          'photo': 'Fang_Dong.jpg',
      }, {
          'name': 'Anrui Chen',
          'photo': 'Anrui_Chen.jpg',
      }, {
          'name': 'Yubin Shi',
          'photo': 'Yubin_Shi.jpg',
      }, {
          'name': 'Xiang Luo',
          'photo': 'Xiang_Luo.jpg',
      }, {
          'name': 'Yifeng Zhao',
          'photo': 'Yifeng_Zhao.jpg',
      }, {
          'name': 'Zihao Chen',
          'photo': 'Zihao_Chen.jpg',
      }, {
          'name': 'Yuting Wu',
          'photo': 'Yuting_Wu.jpg',
      }, {
          'name': 'Xiangyao Qi',
          'photo': 'Xiangyao_Qi.jpg',
      }, {
          'name': 'Qi Lu',
          'photo': 'Qi_Lu.jpg',
      }, {
          'name': 'Guojie Zhao',
          'photo': 'Guojie_Zhao.jpg',
      }, {
          'name': 'Chenyu Wang',
          'photo': 'Chenyu_Wang.jpg',
      }, {
          'name': 'Xianwei Wang',
          'photo': 'Xianwei_Wang.jpg',
      }, {
          'name': 'Siyuan Tang',
          'photo': 'Siyuan_Tang.jpg',
      }, {
          'name': 'Jixian Zhou',
          'photo': 'Jixian_Zhou.jpg',
      }, {
          'name': 'Hengjie Cao',
          'photo': 'Hengjie_Cao.jpg',
      }, {
          'name': 'Mengyi Chen',
          'photo': 'Mengyi_Chen.jpg',
      }, {
          'name': 'Mingkai Gao',
          'photo': 'Mingkai_Gao.jpg',
      }, {
          'name': 'Tianlin Lu',
          'photo': 'Tianlin_Lu.jpg',
      }, {
          'name': 'Yifeng Yang',
          'photo': 'Yifeng_Yang.jpg',
      }, {
          'name': 'Hejin Huang',
          'photo': 'Hejin_Huang.jpg',
      }],
      alumnus: [{
          'name': 'Yutian Lu',
          'photo': 'Yutian_Lu.jpg',
      }, {
          'name': 'Ning Li',
          'photo': 'Ning_Li.jpg',
      }]
    };
  },
  methods: {
    open(url) {
      if (url) {
        window.open(url)
      }
    },
  },
};
</script>
<style>
</style>
