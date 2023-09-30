

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
                <img class="first" src="Group 11.jpg">
                <img class="second" src="Group 10.jpg">
            </div>
        </section>

    <CardSection :id="'why'" :heading="'Why Learn with our Learning Company?'"  :group="'sec2'" :cards="cardGroups[0]" />

    <CardSection :id="'skills'" :heading="'Our Digital Learning Solutions'" :group="'main'" :cards="cardGroups[1]" />

    <CardSection :id="'levels'" :heading="'Specially designed to equip learners with the skills to innovate and succeed'" :group="'sec3'" :cards="cardGroups[2]" />

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
                            <option>Digital Communication & Collaboration Fundamentals</option>
                            <option>Creating Engaging Digital Content</option>
                            <option>Digital Marketing & Social Media</option>
                            <option>Introduction to Cyber Security</option>
                            <option>Understanding Data Analysis & Protection</option>
                            <option>Implementing Digital Processes & Machine Learning</option>
                            <option>Project Management & Ownership</option>
                            <option>Microsoft Office Applications</option>                
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
                            body: "Our Training Needs Analysis allows employers and staff members to share current circumstances as well as digital capabilities and goals. This allows us to personalise workshops to align with development needs and priorities within organisations"
                        },
                        {
                            id: 2,
                            heading:"Digital Innovation",
                            body: "The Digital Skills Training Series focuses on developing digital skills, knowledge and confidence among participants. These sessions raises awareness of innovative uses of digital tools across organisations."
                        },
                        {
                            id: 3,
                            heading:"Expert Guidance",
                            body:"Sessions are delivered bilingually by our dedicated team of digital experts. This includes participations from expert guest speakers who provide invaluable, up to date guidance from the cutting edge of digital and emerging technology."
                        },
                    
                    ], [
                    {
                        id: 4,
                        heading: "Creating Engaging Digital Content",
                        body: "This session focuses on developing in-demand skills within the digital media industries, focusing on three key areas: User Experience (UX) Design, Graphic Design and Web Development."
                    },
                    {
                        id: 5,
                        heading: "Digital Marketing & Social Media",
                        body: "Learners who complete this session will have a solid understanding of social media technologies and digital marketing best practices and will be equipped with the skills they need to develop and execute effective digital marketing campaigns."
                    },
                    {
                        id: 6,
                        heading: "Introduction to Cyber Security",
                        body: "This session will give learners a solid foundation in cyber security principles and best practices, enabling them to take an active role in protecting their personal and professional assets against cyber threats. It is ideal for individuals who are new to the field of cyber security and for those seeking to improve their understanding."
                    },
                    {
                        id: 7,
                        heading: "Understanding Data Analysis & Protection",
                        body: "The training course focuses on the digital data landscape and is designed for learners seeking to gain expertise in data protection and data analysis. The course covers the fundamentals of data privacy and security, including an overview of relevant regulations. It also introduces learners to the basics of data analysis and data visualization."
                    },
                    {
                        id: 8,
                        heading: "Implementing Digital Processes & Machine Learning",
                        body: "This session helps learners to understand and implement digital transformation processes and introduces learners to the basics of artificial intelligence and machine learning,. It also introduces advanced technologies, including Machine Learning and provide an overview of cloud computing and virtualisation and their impact on modern business."
                    },
                    {
                        id: 9,
                        heading: "Project Management & Ownership",
                        body: "This session provides a comprehensive overview of the project management lifecycle, from project initiation and planning to execution and closing. We will focus on methodologies and tools that can be utilised to ensure smooth management and ownership of future projects."
                    },
                    {
                        id: 10,
                        heading: "Microsoft Office Applications",
                        body: "The Microsoft Office training courses include programs such as Excel, PowerBI, Outlook, Teams and more. These courses are available as online or in-person training sessions and can be delivered at the beginner, intermediate or advanced levels, depending on the needs of the individual."
                    }
                ],[
                    {
                        id: 11,
                        heading: "Beginner",
                        body: "A recommended starting point. Ideal for individuals building confidence in using digital in the workplace."
                    },
                    {
                        id: 12,
                        heading: "Intermediate",
                        body: "This could be a role-based certification to begin learning valuable on the job skills or building up skills gained in the fundamentals courses."
                    },
                    {
                        id: 13,
                        heading: "Advanced",
                        body: "These can be Certified and/or technical certifications and can support those on the job experts looking to keep up to date with their core skills."
                    }
                ]]
            }
        },
    }
</script>