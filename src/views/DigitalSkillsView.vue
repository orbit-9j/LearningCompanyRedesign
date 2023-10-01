<template>
    <section id="hero">
            <div>
                <h1>Digital Skills</h1>
                <p>Our courses are flexible, able to be delivered in person or virtually, and always deliver the relevant up to date skills.</p>
                <p>Our programmes will help you unlock the power of technology through skill development.</p>
                <p>Our training sessions are accessible to all and can be tailored to a broad spectrum of organisations, from education providers to businesses to public bodies. </p>
                <a href="#contact"><button>Book Now</button></a>
            </div>
            <div class="images">
                <img class="first" src="/Group11.jpg">
                <img class="second" src="/Group10.jpg">
            </div>
        </section>

    <CardSection :id="'why'" :heading="'Why choose our Learning Company?'"   :cards="cardGroups[0]" />

    <CardSection :id="'skills'" :heading="'Our Digital Learning Solutions'"  :cards="cardGroups[1]" />

    <CardSection :id="'levels'" :heading="'Specially designed to suit your skill level'"  :cards="cardGroups[2]" />

    <section id="contact">
        <h1>Book a Digital Skills session</h1>
        <form>
            <div id="columns">
                <div class="column">
                    <div class="formgroup">
                        <label class="required">First Name</label>
                        <input type="text" placeholder="e.g. Kat">
                    </div>
                    <div class="formgroup">
                        <label>Last Name</label>
                        <input type="text" placeholder="e.g. Jones">
                    </div>
                    <div class="formgroup" >
                        <label class="required">Email</label>
                        <input type="text" placeholder="e.g. example@mail.com" required >
                    </div>
                    <div class="formgroup">
                        <label class="required" >Course</label>
                        <select required>
                            <option value="" disabled selected>-Please Select-</option>
                            <option>Artificial Intelligence in Business</option>
                            <option>Digital Marketing & Social Media</option>
                            <option>Enhanced Working with Digital Tools</option>
                            <option>Exploiting Data: Tools for Data Analysis</option>
                            <option>UX Design & Digital Content Creation</option>             
                        </select>
                    </div>
                    <div class="formgroup">
                        <label class="required">Level</label>
                        <select required>
                            <option value="" disabled selected>-Please Select-</option>
                            <option value="">Beginner</option>
                            <option value="">Intermediate</option>
                            <option value="">Advanced</option>
                        </select>
                    </div>
                </div>

                <div class="column">
                    <div class="formgroup">
                        <label class="required">Audience</label>
                        <select required>
                            <option value="" disabled selected>-Please Select-</option>
                            <option value="">Individual learning</option>
                            <option value="">Academic workshop</option>
                            <option value="">Business training</option>
                        </select>
                    </div>
                    <div class="formgroup">
                        <label class="required">Date</label>
                        <input type="date">
                    </div>
                    <div class="formgroup">
                        <label class="required">Location</label>
                        <input type="text" placeholder="e.g. 123 Street, Town, UK or Virtual">
                    </div>
                    <div class="formgroup">
                        <label>Message</label>
                        <textarea id="message" name="message" rows="auto" cols="50" placeholder="Tell us more about yourself or your business"></textarea>
                    </div>
                </div>
            </div>
            
            <button type="submit">Submit</button>
        </form>
    </section> 


</template>

<script>
    import CardSection from '../components/CardSection.vue';
    export default{
        name:'DigitalSkillsView',
        components:{CardSection},
        data(){
            return{
                cardGroups:[[
                        {
                            id:1,
                            heading: "Tailored Support",
                            body: "Our Training Needs Analysis allows employers and staff members to share current circumstances as well as digital capabilities and goals. This allows us to personalise workshops to align with development needs and priorities within organisations. ",
                            img:"tailor.svg"
                        },
                        {
                            id: 2,
                            heading:"Digital Innovation",
                            body: "The Digital Skills Training Series focuses on developing digital skills, knowledge and confidence among participants. These sessions raises awareness of innovative uses of digital tools across organisations and helps to equip you and your team with the skills to adapt and thrive in the digital future.",
                            img:"light.svg"
                        },
                        {
                            id: 3,
                            heading:"Expert Guidance",
                            body:"Sessions are delivered bilingually by our dedicated team of digital experts. This includes participations from expert guest speakers who provide invaluable, up to date guidance from the cutting edge of digital and emerging technology.",
                            img:"expert.svg"
                        },
                    
                    ], [
                    {
                        id: 4,
                        heading: "Artificial Intelligence in Business",
                        body: "The AI revolution is reshaping the business world, offering limitless possibilities for growth, efficiency, and innovation. This course will equip participants with a grasp of AI, its tangible applications, and the ethical decisions surrounding its implementation. Through focused activities, participants will delve into the intricacies of AI and discover how to harness its capabilities to propel business excellence.",
                        objectives:["Gain a solid foundation in artificial intelligence, including its principles, concepts, and core technologies.","Learn how to leverage AI tools for practical business solutions."],
                        img:"ai.jpg"

                    },
                    {
                        id: 5,
                        heading: "Digital Marketing & Social Media",
                        body: "Unlock the potential of social media platforms as powerful marketing tools in this informative. Participants will gain insights into the pivotal role of digital marketing in the contemporary landscape and the specific impact of social media. Learn to craft engaging content, engage your organisation’s community with targeted marketing campaigns, and employ analytics to measure campaign success, enabling data-driven decisions.",
                        objectives: ["Grasp effective audience engagement strategies.", "Design goal-oriented marketing strategies that align with organisational objectives.", "Utilise analytics for measuring marketing campaign effectiveness."],
                        img:"sm.jpg"
                    },
                    {
                        id: 6,
                        heading: "Enhanced Working with Digital Tools",
                        body: "This course looks at working with digital technologies to enhance digital communication and collaboration. Explore how digital tools can elevate your work and help you better manage projects while honing the skills needed for seamless teamwork in virtual environments. Master various digital technologies, including Microsoft Teams, Miro, Slack, and more, to streamline tasks, elevate project management practices, and enhance workplace communication and collaboration.",
                        objectives:["Master the use of digital technologies, such as Microsoft Teams, Miro, Planner, Microsoft Visio, Slack, Padlet, PollEverywhere, and more, to streamline tasks and improve project management.","Understand the advantages of digital communication and collaboration and avoiding technical issues."],
                        img:"tools.jpg"
                    },
                    {
                        id: 7,
                        heading: "Exploiting Data: Tools for Data Analysis",
                        body: "Discover the power of data in this insightful course, where we explore how to collect, analyse, and leverage data for informed decision making. Participants will learn essential data protection practices, including encryption and access control. Dive into the use of data collection tools like Microsoft Forms and data analysis tools like Microsoft Excel. Gain proficiency in safeguarding data and unlocking its potential to drive strategic decisions.",
                        objectives:["Apply best practices for safeguarding sensitive information, including data encryption and access control.", "Master the effective use of tools like spreadsheets, databases, and data visualisation software for data management and analysis.", "Utilise data insights to make informed decisions."],
                        img:"analysis.jpg"
                    },
                    {
                        id: 8,
                        heading: "UX Design & Digital Content Creation",
                        body: "In today's digital age, crafting user-centric experiences is the linchpin of successful products and services. Our course is your gateway to a deep dive into the art of design and user experience (UX). Focused on understanding user needs, motivations, and behaviours, this program blends theory, real-world examples, and hands-on activities to empower participants with the skills to create visually captivating and user-friendly digital graphics that deliver exceptional user experiences.",
                        objectives:["Develop a strong foundation in design and user experience (UX) principles.","Gain insights into understanding user needs, motivations, and behaviours.", "Craft and create visually engaging and user-friendly digital graphics."],
                        img:"ui.jpg"
                    },
                ],[
                    {
                        id: 11,
                        heading: "Beginner",
                        body: "A recommended starting point. Ideal for individuals building confidence in using digital in the workplace.",
                        img:"abc.svg"
                    },
                    {
                        id: 12,
                        heading: "Intermediate",
                        body: "This could be a role-based certification to begin learning valuable on the job skills or building up skills gained in the fundamentals courses.",
                        img:"gears.svg"
                    },
                    {
                        id: 13,
                        heading: "Advanced",
                        body: "These can be Certified and/or technical certifications and can support those on the job experts looking to keep up to date with their core skills.",
                        img:"cap.svg"
                    }
                ]]
            }
        },
    }
</script>