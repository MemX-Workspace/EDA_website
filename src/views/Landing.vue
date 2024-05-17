<template>
    <div>
        <hero></hero>

        <section class="section bg-secondary">
            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-lg-10">
                        <h2 class="display-3">Event Open to All Undergraduate and Graduate Students Interested in LLM
                            for EDA</h2>
                        <p class="lead">This summer school aims to offer undergraduate and graduate students a
                            comprehensive and hands-on learning experience in LLM for EDA. Led by a team of seasoned
                            veterans and rising stars in the EDA field, the program covers everything from fundamental
                            concepts to cutting-edge research topics in LLM for EDA.</p>
                    </div>
                </div>
            </div>
        </section>


        <section class="section">
            <div class="container">
                <div class="row">
                    <div :class="{ 'research_card': true }" id="pj1">
                        <img class="research_img" src="/img/Educational Lecture.png" alt="图片">
                        <div class="small_font_title" style="margin: 5% 0">Educational Lectures</div>
                        <div class="small_font_text" style="color: #7d7d7f;">
                            Dive into the essentials of LLM for EDA.</div>
                    </div>

                    <div :class="{ 'research_card': true }" id="pj2">
                        <img class="research_img" src="/img/Hackathon.png" alt="图片">
                        <div class="small_font_title" style="margin: 5% 0">Hackathon</div>
                        <div class="small_font_text" style="color: #7d7d7f;">Collaborate, compete, and stand a chance to
                            win significant prizes. Note: Hackathon participation is only available in-person.</div>
                    </div>

                    <div :class="{ 'research_card': true }" id="pj3">
                        <img class="research_img" src="/img/Dinner.png" alt="图片">
                        <div class="small_font_title" style="margin: 5% 0">Networking Dinners</div>
                        <div class="small_font_text" style="color: #7d7d7f;">Connect with peers and professionals over
                            delicious meals.</div>
                    </div>

                </div>
            </div>
        </section>

        <section class="section">
            <div class="container-fluid" style="padding-left: 15%; padding-right: 15%;">
                <div>
                    <h2 class="mb-5" style="margin-left: 250px;">Calendar</h2>
                    <div class="container" style="display: flex; flex-direction: row;">
                        <div class="table-responsive" style="width: 40%;">
                            <table class="table table-striped table-bordered">
                                <thead>
                                    <tr>
                                        <th>6月21日</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr v-for="(event, index) in events.slice(0, 7)" :key="index" :id="'event_' + index"
                                        @mouseenter="showDetails_1(index)" @mouseleave="closeDetails">
                                        <td>
                                            <strong>{{ event.time }}&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;{{
                        event.name }}</strong><br>
                                            {{ event.speaker.replace(/ /g, '&nbsp;') }}
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                        <div class="card" style="width: 60%;">
                            <div class="card-body">
                                <component :is="eventDescription_1"></component>
                            </div>
                        </div>
                    </div>

                    <div class="container" style="display: flex; flex-direction: row; margin-top: 40px;">
                        <div class="table-responsive" style="width: 40%;">
                            <table class="table table-striped table-bordered">
                                <thead>
                                    <tr>
                                        <th>6月22日</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr v-for="(event, index) in events.slice(7, 14)" :key="index"
                                        :id="'event_' + index" @mouseenter="showDetails_2(index)"
                                        @mouseleave="closeDetails">
                                        <td>
                                            <strong>{{ event.time }}&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;{{
                        event.name }}</strong><br>
                                            {{ event.speaker.replace(/ /g, '&nbsp;') }}
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                        <div class="card" style="width: 60%;">
                            <div class="card-body">
                                <component :is="eventDescription_2"></component>
                            </div>
                        </div>
                    </div>

                    <div class="container" style="display: flex; flex-direction: row; margin-top: 40px;">
                        <div class="table-responsive" style="width: 40%;">
                            <table class="table table-striped table-bordered">
                                <thead>
                                    <tr>
                                        <th>6月23日</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr v-for="(event, index) in events.slice(14, 15)" :key="index"
                                        :id="'event_' + index" @mouseenter="showDetails_3(index)"
                                        @mouseleave="closeDetails">
                                        <td>
                                            <strong>{{ event.time }}&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;{{
                        event.name }}</strong><br>
                                            {{ event.speaker.replace(/ /g, '&nbsp;') }}
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                        <div class="card" style="width: 60%;">
                            <div class="card-body">
                                <!-- <component :is="eventDescription_3"></component> -->
                            </div>
                        </div>
                    </div>

                </div>


            </div>
        </section>


        <section class="section">
            <div class="container-fluid" style="padding-left: 15%; padding-right: 15%;">
                <div>
                    <h2 class="mb-5">Hackathon</h2>
                </div>
                <div class="card">
                    <div class="card-body">
                        <p class="card-text dark-text" style="font-size: 1.2em; line-height: 1.6;">
                            <strong>Date:</strong> Friday, June 21, 20:00 - Sunday, June 23, 10:00<br><br>
                            <strong>Event:</strong> Develop an LLM-based EDA framework<br><br>
                            <strong>Description:</strong> Join us for an exciting two-day collaborative event where
                            participants will work together to develop an innovative framework using Language Models
                            (LLM) in Electronic Design Automation (EDA). This event offers a unique opportunity to
                            explore the integration of LLM with EDA processes, enhancing both your skills and
                            understanding of these cutting-edge technologies.<br><br>
                            <strong>Competition Details:</strong><br>
                        <ul style="list-style-type: none; padding-left: 0;">
                            <li>&#8226; Topic Announcement: The specific challenge will be revealed at the start of the
                                event,
                                ensuring a level playing field and stimulating creativity.</li>
                        </ul>
                        <strong>Generous rewards:</strong><br>
                        <ul style="list-style-type: none; padding-left: 0;">
                            <li>&#8226; First Prize: 5000￥</li>
                            <li>&#8226; Second Prize: 3000￥</li>
                            <li>&#8226; Third Prize: 1000￥</li>
                        </ul>
                        </p>

                        <img src="/img/Hackathon.png" alt="Hackathon Image" class="img-fluid mx-auto d-block"
                            style="max-width: 100%; height: auto;">
                    </div>
                </div>
            </div>
        </section>




        <section class="section" id="apply-section">
            <div class="container-fluid" style="padding-left: 15%; padding-right: 15%;">
                <div>
                    <h2 class="mb-5">Apply</h2>
                </div>
                <div class="row">
                    <div class="col-md-5">
                        <div class="card" style="height: 400px;">
                            <div class="card-body">
                                <h5 class="card-title" style="color: #333; font-weight: bold;">1.Scan this QR code to
                                    join our Wechat Group</h5>
                                <img src="/img/Apply QR.png" class="img-fluid" alt="二维码">
                            </div>
                        </div>
                    </div>

                    <div class="col-md-2 d-flex justify-content-center align-items-center">
                        <div class="arrow">
                            <i class="fa fa-arrow-right fa-2x"></i>
                        </div>
                    </div>

                    <div class="col-md-5">
                        <div class="card"
                            style="height: 400px; border-radius: 20px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);">
                            <div class="card-body">
                                <h5 class="card-title" style="color: #333; font-weight: bold;">2.Fill out the
                                    application questionnaire</h5>
                                <p class="card-text" style="color: #666; font-size: 16px;">Please click the button below
                                    to fill out the registration questionnaire:</p>
                                <div style="text-align: center;"> <!-- 将按钮居中 -->
                                    <a href="https://docs.google.com/forms/d/e/1FAIpQLSfQU5CovEQXtTLBYhn3Caon0rDK-l5LiVGS0JpJbWg3FIAaWg/viewform?pli=1"
                                        target="_blank" class="btn btn-primary"
                                        style="font-size: 16px; border-radius: 20px; padding: 10px 20px; margin-top: 15%; width: 80%;">Questionnaire</a> <!-- 调整按钮的padding -->
                                </div>
                            </div>
                        </div>
                    </div>
                </div>


            </div>
        </section>

    </div>
</template>

<script>
import Hero from "./components/Hero";
import Products from "./components/Products";
import Dinner from "./Lecture/Dinner.vue";
import Lecture0 from "./Lecture/Lecture0.vue";
import Lecture1 from "./Lecture/Lecture1.vue";
import Lecture2 from "./Lecture/Lecture2.vue";
import Lecture3 from "./Lecture/Lecture3.vue";
import Lecture4 from "./Lecture/Lecture4.vue";
import Lecture5 from "./Lecture/Lecture5.vue";
import Lecture6 from "./Lecture/Lecture6.vue";
import Lecture7 from "./Lecture/Lecture7.vue";
import Lecture8 from "./Lecture/Lecture8.vue";
import Lecture9 from "./Lecture/Lecture9.vue";



export default {

    created() {
        // Listen for the "scroll-to-apply" event emitted by AppHeader.vue
        this.$root.$on('scroll-to-apply', this.scrollToApplySection);
    },
    beforeDestroy() {
        // Remove the event listener when the component is destroyed to prevent memory leaks
        this.$root.$off('scroll-to-apply', this.scrollToApplySection);
    },

    name: "home",
    components: {
        Hero,
        Products,
        Dinner,
        Lecture0,
        Lecture1,
        Lecture2,
        Lecture3,
        Lecture4,
        Lecture5,
        Lecture6,
        Lecture7,
        Lecture8,
        Lecture9
    },
    data: () => {
        return {
            name: '',
            contact: '',
            message: '',
            tip: 'Place Order',
            events: [
                { time: "09:00 - 09:10", name: "Opening speech", speaker: "曾璇 教授          杨帆 教授          黄将历 博士", description: Lecture0 },
                { time: "10:00 - 12:00", name: "Exploring LLMs: Milestones, Techniques, and Challenges", speaker: "黄将历 博士", description: Lecture1 },
                { time: "12:00 - 13:00", name: "Lunch", speaker: "", description: Lecture1 },
                { time: "13:00 - 14:50", name: "AI Agents: Towards Human-level Software Developer", speaker: "刘怡婷 博士", description: Lecture2 },
                { time: "15:10 - 17:00", name: "Knowledge-Enhanced LLMs with Retrieval-Augmented Generation", speaker: "徐海琳", description: Lecture3 },
                { time: "17:00 - 18:30", name: "Happy Hour", speaker: "", description: Dinner },
                { time: "18:30 - 20:30", name: "LLM for data-scarce domain-specific problems", speaker: "陈子豪", description: Lecture4 },
                { time: "08:30 - 10:20", name: "The representation learning of LLM", speaker: "尚笠 教授          Robert Dick 教授", description: Lecture5 },
                { time: "10:40 - 12:00", name: "LLM and Electronic Design Automation", speaker: "余备 教授", description: Lecture6 },
                { time: "12:00 - 14:00", name: "Lunch", speaker: "", description: Lecture5 },
                { time: "14:00 - 15:20", name: "LLM for Integrated Circuit Testing", speaker: "黄宇 教授", description: Lecture7 },
                { time: "15:40 - 17:00", name: "LLM for Register-Transfer-Level Code Generation", speaker: "贺培鑫 博士", description: Lecture8 },
                { time: "17:00 - 18:30", name: "Happy Hour", speaker: "", description: Dinner },
                { time: "18:30 - 19:50", name: "LLM for Integrated Circuit Verification", speaker: "周海 教授", description: Lecture9 },
                { time: "11:00 - 12:00", name: "Hackathon Awards & Closing", speaker: "杨帆教授", description: "颁奖" }
            ],
            eventDescription_1: Lecture0,
            eventDescription_2: Lecture5,
            // : '注册并完成签到流程',
        }
    },
    mounted() {

        $('[data-toggle="tooltip"]').tooltip({
            delay: { "show": 0, "hide": 0 }, // 设置显示和隐藏的延迟时间
            boundary: "window", // 设置工具提示的边界为窗口
            container: "body" // 将工具提示附加到body元素，避免显示问题
        });

        // 首次加载时,需要调用一次
        this.screenWidth = window.innerWidth;
        this.setSize();


        // 窗口大小发生改变时,调用一次
        window.onresize = () => {
            this.screenWidth = window.innerWidth;
            this.setSize();
        }

    },
    methods: {
        scrollToApplySection() {
            // Scroll to the section with id "apply-section"
            const applySection = document.getElementById('apply-section');
            if (applySection) {
                applySection.scrollIntoView({ behavior: 'smooth' });
            }
        },

        showDetails_1(index) {
            if (index >= 0 && index < this.events.length) {
                this.eventDescription_1 = this.events[index].description;
            } else {
                this.eventDescription_1 = "暂无详情";
            }
        },
        showDetails_2(index) {
            index += 7;
            if (index >= 0) {
                this.eventDescription_2 = this.events[index].description;
            } else {
                this.eventDescription_2 = "暂无详情";
            }
        },
        showDetails_3(index) {
            index += 13;
            if (index >= 0) {
                this.eventDescription_3 = this.events[index].description;
            } else {
                this.eventDescription_3 = "暂无详情";
            }
        },
        closeDetails() {

        },
    }
};
</script>

<style>
.section {
    padding: 50px 0;
    /* Adjust padding as needed */
}

.container {
    display: flex;
    justify-content: center;
}

.row {
    display: flex;
}

.research_card {
    width: 300px;
    /* Adjust card width as needed */
    height: 400px;
    /* Adjust card height as needed */
    margin: 0 20px;
    /* Adjust margin between cards as needed */
    border-radius: 10px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    /* Smooth transition for hover effect */
    cursor: pointer;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    /* Add shadow for 3D effect */
}

.research_card:hover {
    transform: scale(1.05);
    /* Increase size on hover */
    box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.2);
    /* Increase shadow on hover */
}

.research_img {
    width: 100%;
    /* Make image fill the card */
    height: 50%;
    /* Adjust image height as needed */
    object-fit: cover;
    /* Maintain aspect ratio */
    padding: 10px;
}

.small_font_title {
    text-align: center;
    margin-top: 10px;
    /* Adjust margin as needed */
    font-weight: bold;
    font-size: 1.3rem;
    /* Adjust font size as needed */
}

.small_font_text {
    text-align: center;
    margin-top: 10px;
    /* Adjust margin as needed */
    color: #7d7d7f;
    font-size: 1rem;
    /* Adjust font size as needed */
    line-height: 1.4;
    /* Adjust line height as needed */
}

.research_text_warpper {
    padding: 40px;
    background-color: #f8f9fa;
    /* 背景颜色 */
    border: 1px solid #dee2e6;
    /* 边框样式 */
    border-radius: 10px;
    /* 圆角 */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    /* 阴影效果 */
    width: 1020px;
    height: 250px;
}

.research_text {
    font-size: 20px;
    /* 设置你想要的字体大小 */
    font-weight: bold;
    /* 加粗文本 */
}

.text_line_height {
    line-height: 1.6;
    /* 行高 */
}

.dark-text {
    color: #333;
}
</style>