<template>
    <section class="section section-lg">
        <!-- <div class="shape shape-skew-gray">
        </div> -->

        <div class="container">
            <div class="row">
                <div class="mb-5">
                    <h2>The Team</h2>
                    <p class="font-weight-500">
                        MemX is an interdisciplinary research team across cognitive, social and computer sciences,
                        conducting exploratory research on interactive visual intelligence.
                        The MemX team consists of researchers from multiple universities and research labs worldwide,
                        including Fudan University, University of Colorado, University of Michigan, University of
                        Oxford, University of Glasgow, and Microsoft Research.
                        Our goal is to advance the human-centered computing pathway from human perception, emotion,
                        cognition, and finally, also hopefully, towards artificial general intelligence.
                    </p>
                </div>
                <!-- <div>
                    <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Team members</div>
                    <div class="row">
                        <div class="col-md-6 col-lg-2 mb-3" :class="{ 'cursor-pointer': person.url }"
                            v-for="person in teams" :key="person.name" @click="open(person.url)">
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                                class="img-center img-fluid shadow shadow-lg--hover"
                                style="width: 150px; height: 200px; object-fit:cover;">
                            <div class="pt-2 text-center">
                                <h5>{{ person.name }}</h5>
                                <i class="fa fa-link" v-if="person.url"></i>
                            </div>
                        </div>
                    </div>
                </div> -->


                <div>
                    <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Team members</div>
                    <div class="row">
                        <div class="col-md-12 mb-3" v-for="person in teams" :key="person.name">
                            <div class="d-flex align-items-start">
                                <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                                    class="img-start img-fluid shadow shadow-lg--hover"
                                    style="width: 150px; height: 200px; object-fit: cover; margin-right: 40px;">
                                <div>
                                    <div class="row" @click="open(person.url)">
                                        <h5 style="font-size: 1.5rem;">{{ person.name }}</h5>
                                        <i class="fa fa-link" v-if="person.url" style="margin-left: 10px;"></i>
                                    </div>

                                    <small class="text-muted" style="font-size: 1.2rem;">{{ person.title }}</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div>
                    <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Collaborators</div>
                    <div class="row">
                        <div class="col-md-12 mb-3" v-for="person in collaborators" :key="person.name">
                            <div class="d-flex align-items-start">
                                <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                                    class="img-start img-fluid shadow shadow-lg--hover"
                                    style="width: 150px; height: 200px; object-fit: cover; margin-right: 40px;">
                                <div>
                                    <div class="row" @click="open(person.url)">
                                        <h5 style="font-size: 1.5rem;">{{ person.name }}</h5>
                                        <i class="fa fa-link" v-if="person.url" style="margin-left: 10px;"></i>
                                    </div>
                                    <small class="text-muted" style="font-size: 1.2rem;">{{ person.title }}</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>


                <!-- <div>
                    <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Collaborators</div>
                    <div class="row">
                        <div class="col-md-6 col-lg-2 mb-3" :class="{ 'cursor-pointer': person.url }"
                            v-for="person in collaborators" :key="person.name" @click="open(person.url)">
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                                class="img-center img-fluid shadow shadow-lg--hover"
                                style="width: 150px; height: 200px; object-fit:cover;">
                            <div class="pt-2 text-center">
                                <h5>{{ person.name }}</h5>
                                <i class="fa fa-link" v-if="person.url"></i>
                                <small class="h6 text-muted">{{ person.title }}</small>
                            </div>
                        </div>
                    </div>
                </div> -->

                <div>
                    <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Students</div>
                    <div class="row">
                        <div class="col-md-6 col-lg-2 mb-3" :class="{ 'cursor-pointer': person.url }"
                            v-for="person in students" :key="person.name" @click="open(person.url)">
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                                class="img-center img-fluid shadow shadow-lg--hover"
                                style="width: 150px; height: 200px; object-fit:cover;">
                            <div class="pt-2 text-center">
                                <h5>{{ person.name }}</h5>
                                <i class="fa fa-link" v-if="person.url"></i>
                                <!-- <small class="h6 text-muted">Professor</small> -->
                            </div>
                        </div>
                    </div>
                </div>

                <div>
                    <div class="d-block text-uppercase mb-4" style="font-size: 1.5rem;">Alumnus</div>
                    <div class="row">
                        <div class="col-md-6 col-lg-6 mb-3" :class="{ 'cursor-pointer': person.url }"
                            v-for="person in alumnus" :key="person.name" @click="open(person.url)">
                            <img v-lazy="'//memx-website.oss-cn-shanghai.aliyuncs.com/img/photos/' + person.photo"
                                class="img-center img-fluid shadow shadow-lg--hover"
                                style="width: 150px; height: 200px; object-fit:cover;">
                            <div class="pt-2 text-center">
                                <h5>{{ person.name }}</h5>
                                <i class="fa fa-link" v-if="person.url"></i>
                                <!-- <small class="h6 text-muted">Professor</small> -->
                            </div>
                        </div>
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
                'url': 'http://lishang.org/',
                'title': '上海市特聘专家，美国普林斯顿大学博士，曾任英特尔中国研究院副院长、首席架构师，获得美国科罗拉多大学博尔德分校（终身教职）。专注于以人为中心的智能AGI系统、AI计算系统及智能体的开发，其研究成果在ICLR、NeurIPS、WWW、IMWUT、Nature Communication等国际顶尖会议和期刊上发表超过170篇论文，多次获得最佳论文奖与提名，并被引用逾8000次。在产业界亦有丰富的经验。'
            }, {
                'name': 'Robert P. Dick',
                'photo': 'Robert_P._Dick.jpg',
                'url': 'https://robertdick.org/',
                'title': '密歇根大学工程学院电气工程与计算机科学系教授，普林斯顿大学电气工程系博士。曾任西北大学电气工程与计算机科学系副教授、清华大学电子工程系的访问教授。研究领域涵盖嵌入式系统、高效、仿生机器学习、学习动态、隐私保护和对抗审查等方面。'
            }, {
                'name': 'Fan Yang',
                'photo': 'Fan_Yang.jpg',
                'url': 'https://sme.fudan.edu.cn/65/41/c31277a353601/page.htm',
                'title': '复旦大学微电子学院教授，博导，复旦大学微电子学与固体电子学博士。研究领域涵盖人工神经网络的加速、集成电路成品率分析方法及优化、高层次综合方法、大规模电路快速分析建模以及并行计算方法。'
            }, {
                'name': 'Yuhu Chang',
                'photo': 'Yuhu_Chang.jpg',
                'url': 'https://cscw.fudan.edu.cn/yhchang/list.htm',
                'title': '博士后，复旦大学计算机应用技术博士，密歇根大学电气工程与计算机科学系访问学者。研究领域为可穿戴人工通用智能、交互式人工通用智能。'
            }, {
                'name': 'Jiangli Hang',
                'photo': 'Jiangli_Hang.jpg',
                'url': 'https://cscw.fudan.edu.cn/yhchang/list.htm',
                'title': '博士后，复旦大学微电子与固体电子学博士，研究领域为电子设计自动化（EDA）、通过机器学习进行模拟电路设计以及软件开发。'
            }, {
                'name': 'Yiting Liu',
                'photo': 'Yiting_Liu.jpg',
                'url': 'https://yitingliu777.github.io/index.html',
                'title': '博士后，复旦大学计算机应用技术博士，研究领域为电子设计自动化（EDA）、VLSI物理设计、大语言模型、嵌入式系统开发。'
            }],
            collaborators: [{
                'name': 'Qin Lv',
                'photo': 'Qin_Lv.jpg',
                'url': 'https://home.cs.colorado.edu/~lv/',
                'title': '科罗拉多大学博尔德分校计算机科学系教授，普林斯顿大学计算机博士。研究聚焦于全栈数据分析，整合系统、算法和应用程序，以实现在普适计算和科学发现中的高效有效数据分析。'
            }, {
                'name': 'Ning Gu',
                'photo': 'Ning_Gu.jpg',
                'url': 'https://cscw.fudan.edu.cn/ninggu/list.htm',
                'title': '复旦大学计算机科学技术学院教授、博士生导师，复旦大学社会计算研究中心主任，中国计算机学会会士，IET(英国工程技术学会)Fellow，CCF协同计算专委会荣誉主任。长期从事以人为中心的协同计算研究，包括分布式协同、社会化协同和群智协同的理论与技术。'
            }, {
                'name': 'Tun Lu',
                'photo': 'Tun_Lu.jpg',
                'url': 'https://cscw.fudan.edu.cn/tunlu/list.htm',
                'title': '复旦大学计算机科学技术学院教授、博士生导师，复旦大学计算机科学技术学院副院长。研究领域涵盖CSCW与社会计算，人机协同与交互，群智协同，推荐系统，服务与云计算。'
            }, {
                'name': 'Dongsheng Li',
                'photo': 'Dongsheng_Li.jpg',
                'url': 'http://recmind.cn/index.html',
                'title': '微软亚洲研究院（MSRA）上海分院的首席研究经理，复旦大学计算机科学学院的兼职教授，曾在IBM中国研究院上海分院担任研究员，ACM和IEEE的高级会员，并担任多个顶级会议的程序委员会成员，例如NIPS、ICML、ICLR等。研究兴趣包括机器学习、健康人工智能和推荐系统。'
            }, {
                'name': 'Mingzhi Dong',
                'photo': 'Mingzhi_Dong.jpg',
                'url': 'https://cscw.fudan.edu.cn/mingzhidong/list.htm',
                'title': '英国巴斯大学计算机学院讲师，英国伦敦大学学院博士。研究领域涵盖理论或直观可解释的机器学习算法及其在计算机视觉、人机交互等领域的应用。'
            }, {
                'name': 'Yingying Zhao',
                'photo': 'Yingying_Zhao.jpg',
                'url': 'http://yingyingzhao.com/',
                'title': '思克莱德大学计算机与信息科学系讲师，同济大学博士。研究领域涵盖智能人机交互、机器学习和深度学习系统及应用。近年来，她的研究聚焦于构建基于视觉智能的交互式系统，旨在探索用户的注意力、情感、意图、认知和行为，并为用户提供人机交互场景下的智能服务。'
            }, {
                'name': 'Yujiang Wang',
                'photo': 'Yujiang_Wang.jpg',
                'url': 'https://eng.ox.ac.uk/people/yujiang-wang/',
                'title': '牛津大学高等研究院（苏州）研究员，在伦敦帝国学院获得计算机视觉博士学位，并分别在清华大学、伦敦帝国学院和伦敦大学学院获得了学士学位和两个荣誉硕士学位。研究兴趣主要集中在医疗人工智能、唇语识别、智能可穿戴设备等领域。'
            }, {
                'name': 'Xiaochen Yang',
                'photo': 'Xiaochen_Yang.jpg',
                'url': 'https://www.gla.ac.uk/schools/mathematicsstatistics/staff/xiaochenyang/',
                'title': '英国格拉斯哥大学数学与统计学院讲师，伦敦大学学院统计科学博士。研究方向涵盖小样本机器学习、可信机器学习以及医学科学领域的机器学习方法。'
            }, {
                'name': 'Rui Zhu',
                'photo': 'Rui_Zhu.jpg',
                'url': 'https://www.bayes.city.ac.uk/faculties-and-research/experts/rui-zhu',
                'title': '伦敦大学城市学院贝叶斯商学院副教授，伦敦大学学院统计科学系博士。研究方向涵盖统计学习，基于子空间的分类方法，光谱数据分析，高光谱图像分析，图像质量评价等.'
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
                'photo': 'del_Yifeng_Zhao.jpg',
            }, {
                'name': 'Zihao Chen',
                'photo': 'del_Zihao_Chen.jpg',
            }, {
                'name': 'Yuting Wu',
                'photo': 'del_Yuting_Wu.jpg',
            }, {
                'name': 'Xiangyao Qi',
                'photo': 'del_Xiangyao_Qi.jpg',
            }, {
                'name': 'Qi Lu',
                'photo': 'del_Qi_Lu.jpg',
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
            }, {
                'name': 'Jiawei Cheng',
                'photo': 'Jiawei_Cheng.jpg',
            }],
            alumnus: [{
                'name': 'Yutian Lu',
                'photo': 'Yutian_Lu.jpg',
            }, {
                'name': 'Ning Li',
                'photo': 'Ning_Li.jpg',
            }],
            unused: [{
                'name': 'Xianghua Ding',
                'photo': 'Xianghua_Ding.jpg',
                'url': 'https://xianghuading.com/',
                'title': 'Fudan University'
            }
            ]
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
<style></style>
