# Oleg Yasko #
## Web Developer ##

### Personal details: ###

Date of Birth: the 27th of November, 1981  
Age: 38 y.o.  
Nationality: Ukrainian  
City of residense: Zaporozhye, Ukaine  
Skype: fenixol3  
E-mail: fenixoleg7@gmail.com  

### My skills: ###
* PHP
* html/css
* Yii2/ Yii1
* Vue.js

### Code examples ###
```
BX.Vue.component('bx-day',
    {
        props: {
            dayName: String,
            dayNumber: String,
        },
        data(){
            return{
                isActive:false,
                isAdd: false
            }
        },
        computed: {
            checkProgram () {
                return this.$store.getters.getCheckProgram
            },
            new_schedules () {
                return  this.$store.getters.getNewSchedules(this.dayNumber);
            },
            subjects () {
                return this.$store.getters.getSubjects
            },
            checkFinishShedules () {
                return this.$store.getters.checkFinishShedules
            }
        },
        watch: {
            checkProgram : function () {
                this.isActive = true;
            }
        },
        methods:{
            addSchedal(item){
                this.$store.dispatch('changeSchedule', {
                    lesson: item,
                    day: this.dayNumber,
                    update: true
                });
                this.$store.dispatch('scheduleChangeAddHours',{id:item.id});
                this.isAdd = false;
            },
            hide: function() {
                this.isAdd = false;

            }
        },
        template: `
                    <div class="day" :class="{'active': isActive}" v-click-outside="hide">
                        <div class="day__header">
                            <span>{{ dayName }}</span>
                        </div>
                        <div class="day__card">
                            <ul>
                                <li v-for="(item, index) in new_schedules">
                                    <bx-lesson v-if="index != new_schedules.length - 1" v-bind:lesson_val="item" v-bind:day="dayNumber" v-bind:last="false"/>
                                    <bx-lesson v-else v-bind:lesson_val="item" v-bind:day="dayNumber" v-bind:last="true"/>
                                   
                                </li>
                                <li v-if="isAdd">
                                    <div class="lesson edit">
                                        <div class="date_time_label"></div>
                                        <div class="lesson__title">
                                            <span class="number"></span>
                                            <span class="title"></span>
                                        </div>
                                        <transition name="slide-fade">
                                             <ul>
                                                <li v-for="(item, index) in subjects">
                                                    <a href="#" key="item.id" @click="addSchedal(item,index)">{{ item.name }}</a>
                                                </li>
                                            </ul>
                                        </transition>
                                    </div>
                                </li>
                                
                            </ul>
                            <div class="footer__day">
                            
                                <button class="timetable__btn"  v-if="isActive" @click="isAdd = !isAdd">
                                    <span class="add__btn" ></span>
                                    <label class="status-red" v-if="checkFinishShedules"></label>
                                </button>
                                
                            </div>
                        </div>
                    </div>`
    }); 
```

### Professional experience: ###
Freelancer at Upwork.com
2018 - Present
[My profile for Upwork:] (https://www.upwork.com/freelancers/~01ac21aa36060eed06)

- Yii
- Yii2
- CSS/HTML/Bootstrap
- WordPress
- Vue.js

Freelancer at Freelancehunt.ru 
2011 - Present
My profile: https://freelancehunt.com/freelancer/Freelancer_Oleg.html 
- Yii
- Yii2
- CSS/HTML/Bootstrap
- WordPress

Web Developer | Realty Promotion Group
June 2014 — january 2015
Saint Petersburg, realtypromotion.ru
IT, System Integration, Internet
- Bitrix
- PSD to HTML;
- WordPress;

Web Developer | Flickshine
August 2013 - June 2014
I was junior specialist at the company and my tasks were:
- PSD to HTML;
- WordPress;
- Yii.
It was my first job as a Web Developer and I am really thankful for the experience I got there.  

Design Engineer | Krankomplekt
July 2010 - January 2013
My tasks were:
- Technical and Design Documentation Development;
- Modeling in AutoCad and SolidWorks;
- Staff Management  

Design Engineer | Konecranes Ukraine
January 2006 - January 2010
My tasks were:
- Technical and Design Documentation Development;
- Modeling in AutoCad and SolidWorks.
Other Experiences
Design Engineer

### Education: ###

1997 - 2001 Zaporozhye Hydroenergetic College ZNTU
College degree, Mechanical Engineering

2001-2005 Zaporizhzhya National Technical University
Master's degree, Technical Engineering
### Languages: ###

Russian - Native
Ukrainian - Native
English - Basic, ability to work with technical documentationsgi