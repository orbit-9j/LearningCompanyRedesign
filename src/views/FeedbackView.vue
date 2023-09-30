<template>
    <div class="issues">
        <RouterLink to="/digitalskills">&#8594; Back to re-design &#8592;</RouterLink>
    <h1>Feedback for the current Digital Skills page - Learning Company website</h1>

    <h2>Functional issues</h2>
    <ul>
        <li>a booking button has been reported to not work, though I have not tried to reproduce this issue</li>
    </ul>
    <TableComponent :rows="tables[0]"/>

    <h2>Logical/flow issues</h2>
    <h3>flow</h3>
    <TableComponent :rows="tables[1]"/>
    <h3>redundancy &amp; irrelevance</h3>
    <TableComponent :rows="tables[2]"/>
    <h3>content consistency</h3>
    <TableComponent :rows="tables[3]"/>

    <h2>Aesthetic issues</h2>
    <h3>consistency &amp; unity</h3>
    <TableComponent :rows="tables[4]"/>
    <h3>contrast</h3>
    <TableComponent :rows="tables[5]"/>
    <h3>placement</h3>
    <TableComponent :rows="tables[6]"/>
    <h3>when the browser window is snapped to the side (narrow)</h3>
    <p>users will often browse the web with 2 (or more) windows displayed on their screen, snapped to different screen areas to facilitate multitasking. this may be the only way they interact with the website and their only impression of it.</p>
    <TableComponent :rows="tables[7]"/>

    <h2 id="spelling-issues">Spelling issues</h2>
    <ul>
    <li>the booking link under &quot;Introduction to Cyber Security&quot; has a misspelled subject, the L is missing (&quot;mailto:[email address]?subject=Digita%20Training%20Booking&quot;)</li>
    <li>the &quot;Introduction to Cyber Security&quot; card misspells &quot;learners&quot; as &quot;learnes&quot;</li>
    </ul>

    <h1>original webpage reference</h1>
    <div class="webgrid">
        <div>
            <h2>full width</h2>
            <img  src="fullpage.png">
        </div>
        
        <div>
            <h2>narrow</h2>
            <img  src="narrowfullpage.png">
        </div>
    </div>
   
    <h1 class="margin">Next steps for the redesign</h1>
    <ul>
        <li>Responsive design (for tablets and smartphones)</li>
        <li>Redesign more pages (code will need to be converted to React JS to make it easier to reuse elements like cards, headers, and footers between pages)</li>
    </ul>
    </div>
    

</template>

<script>
import TableComponent from '../components/Table.vue';

    export default{
        name:'FeedbackView',
        components:{TableComponent},
        data(){
            return{
                tables:
                    [
                        [/* table */
                            [/* row */
                            { id: 123456, content: "when the browser window is snapped to the side (narrow), 2 sections ('Why Learn with our Learning Company?' & 'Our Digital Learning Solutions') are not shown. these sections are also missing from the mobile website" },
                            { id: 234567, content: "70% of webpages are viewed on mobile devices. missing sections will likely confuse and frustrate the user, reducing the likelihood that they will engage. this issue is most likely caused by the way different (incompatible) Wix elements interfere with each other" },
                            { id: 345678, content: "change the code for responsiveness (write from scratch or check the behaviour of the Wix elements)" }
                            ]
                        ],
                        [
                            [
                                { id: 456789, content: "unintuitive flow of sections" },
                                { id: 567890, content: "as a potential client, I want to read the page in this order: why should I consider a course from BLC? -> what courses do they offer? -> do they have this course for my skill level?" },
                                { id: 678901, content: "re-order the sections" }
                            ],
                            [
                                {id:7451785, content:"the skills section disrupts the flow of the page"},
                                {id:23712087, content:"It is bigger than the other sections so it takes longer to scroll past if the user is not interested in reading it"},
                                {id:2527151872, content:"reduce its length to match the other sections, either by collapsing it or implementing horizontal scrolling. I used the design of the apple store page for inspiration for the scrolling part"}
                            ]
                            
                        ],
                        [
                            [
                                { id: 111111, content: "the digital skills page has a contact form identical to the one on the contact page" },
                                { id: 222222, content: "the form is not relevant to booking a session, users may find it confusing when trying to book a session" },
                                { id: 333333, content: "replace it with a session booking form" }
                            ],
                            [
                                { id: 444444, content: "booking buttons lead to an email message with a specific subject line instead of a booking form" },
                                { id: 555555, content: "you rely on the user to provide all the information you need to book a course in one email, as they don't have a template to fill out. email buttons are useful for enquiries, but less useful for booking" },
                                { id: 666666, content: "a form structured to record information about the client, course, skill level, date & time, and other relevant information in a structured and easy to read manner, without the need to go back and forth with the client for more information" }
                            ],
                            [
                                { id: 777777, content: '"Why Learn with our Learning Company?" has a button that says "Book"' },
                                { id: 888888, content: "it does not provide information about what course the user is booking by clicking on the button, as each skill course already has its own booking button" },
                                { id: 999999, content: "remove this button" }
                            ],
                            [
                                { id: 101010, content: "each course has its own booking button" },
                                { id: 111111, content: "Hick's law violation: overwhelming number of choices for the user, when in reality all the buttons do the exact same thing" },
                                { id: 121212, content: "remove all the booking buttons under the course cards and direct the user to the singular booking form at the bottom of the page through the natural reading flow. I also added the ability for the user to skip to it from the top of the page by clicking on the 'Book Now' button in the hero element as is common for CTAs in other websites" }
                            ],
                            [
                                { id: 131313, content: "the hero (first) section has a lot of text, and the words in the 'Whether you are looking for introductory, intermediate or advanced training' part are repeated in a later section (the skill level section)" },
                                { id: 141414, content: "the hero section text should be snappy and to the point to hook the user in, and it is unnecessary to repeat information that user will read several seconds later in a following section" },
                                { id: 151515, content: "remove that phrase from the hero text. the rest of the text should remain as is since it's unique to the hero text" }
                            ]
                        ],
                        [
                            [
                                { id: 111111, content: "The &quot;Digital Communication &amp; Collaboration Fundamentals&quot; and &quot;Implementing Digital Processes &amp; Machine Learning&quot; cards are missing a full stop, all the other cards have it" },
                                { id: 222222, content: "A minor flow issue that users may stumble at when reading the cards sequentially" },
                                { id: 333333, content: "Add the missing full stops" }
                            ]
                        ],
                        [
                            [
                                { id: 111111, content: "Cards in each section have a different design (border, padding, width, background, heading style, section background colour)" },
                                { id: 222222, content: "" },
                                { id: 333333, content: "Unify the card and section styles to one style, only varying colors to create visual separation between cards of different sections. I noticed that the skills section is highlighted with a pink background, which suggests that it's the most important one. I chose not to use it in my redesign, but I am not against it. I also borrowed the colored shading from the hero images for consistency of card-shaped elements. I varied the direction of the shadow between sections to create variety" }
                            ],
                            [
                                { id: 444444, content: "Inconsistent button width/padding (the &quot;Book&quot; button under &quot;Why Learn with our Learning Company?&quot; has a set width while the other buttons' width is determined by text width and padding)" },
                                { id: 555555, content: "" },
                                { id: 666666, content: "This button was removed to remove redundancy, so no aesthetic issues were addressed for it" }
                            ],
                            [
                                { id: 777777, content: "Inconsistent heading styles (some h2's are bold, some aren't)" },
                                { id: 888888, content: "" },
                                { id: 999999, content: "Select a heading style to be applied to all headings" }
                            ],
                            [
                                { id: 101010, content: "Heading case difference in the &quot;Specially designed to equip learners with the skills to innovate and succeed&quot; section (&quot;Beginner&quot; vs &quot;INTERMEDIATE&quot; &amp; &quot;ADVANCED&quot;)" },
                                { id: 111111, content: "" },
                                { id: 121212, content: "Fix capitalization of headings" }
                            ],
                            [
                                { id: 131313, content: "Inconsistent centering/text alignment between cards in different sections. &quot;Our Digital Learning Solutions&quot; aligns paragraphs to left, other cards center them" },
                                { id: 141414, content: "" },
                                { id: 151515, content: "Center all card text" }
                            ],
                            [
                                { id: 161616, content: "Colour scheme is not consistent in use across buttons, section backgrounds, and header backgrounds with seemingly no thought behind it" },
                                { id: 171717, content: "Colour schemes are designed with meaning in mind. Each color in a company's branding represents its values. Apart from this, colors should have consistent use across elements to reduce confusion. It's common for websites to limit their accents to 1 or 2 colors, unlike this website, which makes it challenging to work with" },
                                { id: 181818, content: "I reserved yellow for buttons and link hover states, blue for helper elements (scrollbar, text field focus), and pink for the asterisks in the forms. I changed the shadow color of one of the hero images from yellow to blue as yellow is now reserved for buttons. I also thought about using one color per webpage, visually separating the various services the company offers (e.g. &quot;Digital Skills&quot; uses the pink accent color, and &quot;Work Based Learning&quot; uses yellow). Both solutions are good and a matter of personal taste" }
                            ],
                            [
                                { id: 191919, content: "When hovering over a button, each button color behaved differently (pink buttons change color to yellow, yellow buttons lose border but otherwise no changes, yellow button becomes blue)" },
                                { id: 202020, content: "" },
                                { id: 212121, content: "Instead of setting a new hover color for each colored button, I used darken(color) to make the button's existing color darker on mouseover" }
                            ],
                            [
                                { id: 222222, content: "Inconsistent size of blank space between sections. &quot;Our Digital Learning Solutions&quot; is closer to the hero section than to the &quot;Why Learn with our Learning Company?&quot; section" },
                                { id: 232323, content: "" },
                                { id: 242424, content: "Set the same top and bottom padding for each section" }
                            ],
                            [
                                { id: 252525, content: "Varying paragraph font sizes between sections (e.g. &quot;Our Digital Learning Solutions&quot; has a smaller font than the hero element paragraphs)" },
                                { id: 262626, content: "" },
                                { id: 272727, content: "Use the same font size across all paragraphs" }
                            ]
                        ],
                        [
                            [
                                { id: 111111, content: "There are black borders around buttons and images" },
                                { id: 222222, content: "The borders make the webpage appear more cluttered by adding another color in addition to the 3 accent colors. They also create emphasis on elements that do not need to be emphasized. Borders are typically used to create contrast and separation, but the button colors have good enough contrast with the background that a border is not necessary" },
                                { id: 333333, content: "Remove black borders for a cleaner look" }
                            ]
                        ],
                        [
                            [
                                { id: 111111, content: "The &quot;Contact Us&quot; button in the hero section overlaps with paragraph text on some screens" },
                                { id: 222222, content: "The user may not be able to read part of the text, which they may find frustrating" },
                                { id: 333333, content: "Rewrite the CSS to fix the way the button placement behaves, which can be done with a simple margin property and position:relative instead of absolute" }
                            ]
                        ],
                        [
                            [
                                { id: 111111, content: "The cards under &quot;Specially designed to equip learners with the skills to innovate and succeed&quot; have misaligned paragraphs, skewing the text to the right and creating extra blank space to the side of it" },
                                { id: 222222, content: "Distracts the reader" },
                                { id: 333333, content: "Rewrite the CSS to fix the position of the text on narrow screens" }
                            ],
                            [
                                { id: 444444, content: "There is a very large blank space between the hero &quot;Contact Us&quot; button and the hero paragraph text" },
                                { id: 555555, content: "This may be caused by the way the Wix theme handles image position at different screen sizes" },
                                { id: 666666, content: "I separated the hero section into 2 columns, with each column being in a self-contained wrapper that will not interfere with each other. On narrower screens, the second wrapper can be moved above the first one, allowing images to be displayed above the text (or removed altogether, with no effect on the rest of the text)" }
                            ],
                            [
                                { id: 777777, content: "The Twitter and LinkedIn links wrap around the copyright footer text in an unnatural way" },
                                { id: 888888, content: "" },
                                { id: 999999, content: "I wrapped the links into a wrapper so they cannot move away from each other when elements are moved around on narrower screens" }
                            ]
                        ]
                    ]
                }
            }
    }
</script>

