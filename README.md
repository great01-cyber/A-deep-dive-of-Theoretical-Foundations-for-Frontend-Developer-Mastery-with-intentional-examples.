# A deep dive of Theoretical Foundations for Frontend Developer Mastery with intentional examples.

![Knight Capital Incident](images/developerImage.jpg "Knight Capital")


Have you ever abandoned an app right at the sign‑up page? Or felt uneasy navigating a website because the buttons were scattered randomly, the colors clashed, and the layout felt confusing and unnecessarily complex? Maybe you were asked to complete twenty fields in one go. You carefully fill everything out, hit Submit — and only then are you told your password doesn’t meet some hidden, unspoken requirement. A requirement that was never communicated upfront.

Instead of clear guidance, you’re met with a vague, almost mocking message: “Invalid input.”  
Invalid how, you wonder.

Required fields weren’t marked. There was no real‑time validation. No helpful red outline showing which field was wrong. Just a generic prompt telling you to “go back and correct missing information,” as if you’re supposed to magically know what the system wants.

So you scroll. You search. You guess.
And you are now already getting frustrated. 
The reason you are frustrated is simple, no one enjoys repeating a task they thought they had already completed — especially when the mistakes could have been prevented with clear guidance along the way.
Also, you manage to fill in the form and you tap the Submit button.
Nothing happens.
No loading spinner.
No subtle animation.
No confirmation message.
No success screen.
Just silence.
For a brief moment, you’re left wondering: Did it go through?
So you tap again. And maybe… one more time.
At this point, you become fed up and either postpone the signup process to when you have the time, and as usual, most may not return unless it’s really important to them.
This is how poor user experience quietly creates bigger problems.

These frustrations often arise because frontend developers either overlook or are unaware of the essential design principles and learning theories that underpin a smooth, intuitive user experience. As a frontend developer, your interface should minimise cognitive load, provide immediate clarity, and guide users effortlessly through every task.

In this tutorial, I will introduce the academic theories that should inform and elevate your frontend decisions. You might wonder: What do academic theories have to do with frontend development? The answer is simple. Academic theories are not abstract ideas; they are the result of rigorous scientific investigation — controlled experiments, validated models, and decades of research into how humans think, learn, perceive, and interact with information.

Because these theories are grounded in evidence rather than opinion, they offer reliable guidance for building interfaces that align with how the human brain actually processes information. Applying them to frontend development means you are not designing by guesswork or personal preference; you are applying tested, scientific insights to create clearer, faster, more humane user experiences.

In other words, when you build with academic theory in mind, your frontend becomes more than just visually appealing — it becomes cognitively efficient, behaviourally aligned, and measurably easier for users to navigate.

Based on the above I propose the following laws will guide your development. Let’s start by looking at Fitt’s law.

**Fitts’s Law:** 
Fitt’s law is a brainchild of Paul Fitts. He was among the early psychologists who recognised that many human errors result from flawed design rather than simple human weakness. During World War II, he studied airplane cockpit layouts and concluded that numerous incidents attributed to pilot error were actually caused by poor design decisions. Based on his findings, he postulated that the time required to acquire/reach a target is determined by the distance to the target and the size of the target. See diagram illustration below.


![Knight Capital Incident](images/2.png "Knight Capital")

![Knight Capital Incident](images/1.png "Knight Capital")



From the above, between Target B and Target C, it will be faster to interact with Target C than Target B simply because of the distance (Target B is farther away). Interestingly, though Target A and Target C are at the same distance, Target C will still be faster to interact with and less error-prone because of its larger size. In simple terms, Fitt’s Law tells us that the time required to move to a target depends on two main factors: the distance to the target and the size of the target. The farther away an element is, the longer it takes to reach. The smaller it is, the more precision it demands thereby increasing interaction time and the likelihood of errors. Conversely, closer and larger targets reduce cognitive load, motor effort, and frustration. In a nutshell, Fitts’s main message to developers is to reduce the distance users must travel on the screen and to make important buttons large and visually dominant. Imagine placing a submit button at the top-right corner of the screen. After a user finishes filling out a long form, they must then move their cursor or thumb all the way back to the top-right corner just to submit the form. Ideally, the best place to position the submit button is at the bottom, where the form ends. Another example of this is - placing the related buttons like “Add to Cart” button and “Check out Button” in opposite directions. This will cause extra thumb movement across the screen, thereby increasing interaction.

Design Takeaway from Fitt’s Law: As a frontend developer, you should always ensure your targets (by target I mean primary buttons/(Call-to-action buttons) such as "Subscribe Now," "Pay Now," "Create Account," or "Sign Up") are large and visually dominant. I strongly recommend making the Call-to-Action (CTA) the most recognisable button on the screen; this is backed by UI theory. Additionally, place your CTA buttons in a natural position that feels convenient for the user. Specifically, place your targets close to the thumb. It is much faster for a user to interact within the "natural zone" than the "hard zone" (see figure). Also use padding to increase the interactive area. By doing this, you are increasing the size of the targets. Now imagine a menu that disappears because your cursor moves a few inches away from the menu, simply because the developer  failed to use effective padding to increase the interactive area that will be really frustrating to the user. 

A fundamental principle that also emerges from Fitt’s Law is the idea of infinite targets. This concept also emerges from Fitts’s Law.When an interface element is placed at the very edge or corner of a screen, it becomes effectively “infinite” because the cursor cannot move beyond the screen boundary. The edge acts as a physical barrier, allowing the user to fling the mouse in that direction without precision or careful aiming. As a result, corners and edges become the fastest, easiest, and most reliable places for users to access important controls.

This is why operating systems such as Apple’s macOS and Microsoft Windows position their most essential menus and buttons at these locations. The macOS Apple Menu sits in the top‑left corner, Windows historically placed the Start button in the bottom‑left corner, and both systems anchor taskbars, docks, and notification areas along screen edges. These placements reduce cognitive load, minimise motor effort, and increase interaction speed because users do not need to slow down or correct their cursor movement. The screen itself “catches” the pointer.

In essence, infinite targets transform small interface elements into large, easy‑to‑hit zones simply by leveraging the geometry of the screen. What this means for developers: Place your most important and frequently used actions where users can reach them with the least effort. Screen edges and corners act as natural stopping points, meaning users cannot overshoot them. This transforms even small buttons into large, easy‑to‑hit interaction zones. By anchoring navigation bars, primary actions, and essential menus along these boundaries, you reduce cognitive load, speed up interaction, and create interfaces that feel more intuitive. 

![Knight Capital Incident](images/3.png "Knight Capital")

From the image above, we can see that the call-to-actions buttons on each of the screens are the most visually dominant button and largest in size and also blacked within the natural region. This makes it faster/easier to interact with. 

![Knight Capital Incident](images/4.png "Knight Capital")

Place your Call-to-actions button  within the natural zone.

**Hicks Law**: 
Hick’s Law is a psychological principle that describes the relationship between the number of choices presented to a user and the time it takes them to make a decision. It was formulated by William Edmund Hick in 1952. The law states that as the number of options increases, the decision time increases logarithmically. In simple terms, more choices slow users down, while fewer choices speed up decision-making. 

![Knight Capital Incident](images/5.png "Knight Capital")
Literally, this is how users feel when they encounter a form that asks for too much information upfront. The longer the form gets, the more frustrated they become. An example of this is Overloading menus with too many items, Presenting long, unorganized forms,Too many call-to-actions (CTAs) on one screen and Nested menus with excessive depth etc. All of these creates friction and can lead to cognitive overload.

As a developer, avoid overwhelming users with too many buttons, menu items, or actions at once. Avoid cluttered navigation menus. In fact, it’s been said that SEO engines find it harder to track too many menus. Hide advanced options under “More” or use progressive disclosure. Use progressive disclosure to break multi-step forms and complex decisions into smaller steps. Organise options into logical categories so users can process information faster (An example of this is, placing “delete” and “edit” options together, as they often go together). Reduce decision anxiety, as too many choices create doubt and friction (It’s been said that the more you ask from a user, the less you get). I also advise using recommended labels, showing brief descriptions, providing visual previews, and using comparison tables wisely to show comparison between products especially when they have many characteristics. An example of a comparison table is shown below:

![Knight Capital Incident](images/6.jpg "Knight Capital")

Use of comparison table to compare products

https://drive.google.com/file/d/1sY-tb9W1QDnyrH9dd3NSYsteP9WoMT27/view?usp=drive_link

Progressive Disclosure.MOV

From the video above, instead of showing all the menu details at once, it is better to hide them initially. As you can see, the additional information only appears when the arrow down button is pressed. This approach prevents overwhelming the user and keeps the interface clean and focused. Also, rather than showing advanced configuration options by default, display only the most commonly used settings. Advanced options can be hidden under an expandable section like “Advanced” or “More Settings.

**Gestalt Principles**: In the 1920s, a group of German psychologists Max Wertheimer, Kurt Koffka, and Wolfgang Köhlern introduced what are now known as the Gestalt Principles. Their work sought to understand how humans perceive and interpret visual information. The word “Gestalt” is German for “unified whole,” reflecting the core idea behind the theory: people naturally perceive objects as organised patterns and complete forms rather than as separate, disconnected parts. These principles explain how the human mind structures visual elements to make sense of the world. Over time, they have become highly influential in fields such as design, user experience (UX), psychology, and data visualization, where understanding perception is critical.

Some of the key Gestalt principles include:

**Proximity**: Elements that are placed close to each other are perceived as a group, while those spaced far apart are seen as separate. In UI design, this is why we group labels directly next to their corresponding input fields.

Example: In a blog feed, the "Title," "Author," and "Date" should have small margins between them (8px), while the space between one blog post card and the next should be much larger (40px). This tells the user's brain: "These three text strings belong to this specific post."

**Similarity**: We naturally group elements that share similar visual characteristics, such as color, shape, size, or orientation. For example, even if buttons are spread across a page, if they are all the same shade of blue, the user understands they perform similar functions.

**Example**: If your primary "Submit" button is blue with rounded corners, every other primary action on your site should look exactly the same. If you suddenly use a square red button for a primary action, the user will be confused because the "similarity" is broken.

**Continuity**: The human eye prefers to follow a continuous path or curve rather than jagged or broken lines. We perceive items aligned on a line or curve as being related. This is often used in navigation menus or horizontal carousels to guide the user's gaze.

**Example**: A Horizontal Carousel where the last visible card is slightly "cut off" at the edge of the screen. This visual break creates a path that encourages the user to keep scrolling; their eyes follow the line of cards.

**Closure**: When we look at a complex arrangement of visual elements, we tend to look for a single, recognisable pattern. If an image is missing parts, our brains fill in the gaps to "close" the shape. This is a favorite technique for minimalist logo design.

**Example**: Iconography. A "hamburger menu" (three lines) isn't a literal drawer, but our brains "close" the shape to understand it represents a menu. Similarly, a segmented circular loading spinner is just a few moving lines, but we perceive it as a continuous rotating circle.

**Figure/Ground**: This principle describes the mind's tendency to separate an object (the figure) from its surrounding area (the ground or background). In web design, using a "modal" or "pop-up" relies on this; by blurring the background, you force the user to see the pop-up as the focal figure.

**Example**: Modals or Lightboxes. When a user clicks "Login," the background site often dims (the "Ground") while the login box stays bright and centered (the "Figure"). This immediate depth change tells the user exactly where their attention belongs.
      Common Fate: Elements that move in the same direction are perceived as more related than elements that are stationary or move in different directions. Think of a dropdown menu: when all sub-items slide down together, they are clearly part of the same "unit."
**Example**: Expandable Accordions. When you click a FAQ header and five sub-items slide down at the exact same speed and direction, the "Common Fate" tells the user that all those items belong to that specific category. If they flew in from different directions, the relationship would be lost
    Focal Point: Whatever stands out visually will capture and hold the viewer’s attention first. This is essentially the principle of emphasis. A bright "Sign Up" button in a sea of gray text acts as the focal point, directing the user's primary action.

**Example**: An Alert Banner or a Pricing Table. In a three-tier pricing table (Basic, Pro, Enterprise), the "Pro" column is often slightly larger or a different color. This creates a focal point that draws the eye to the "recommended" option immediately.

**Design Takeaway from Gestalt**: Always group labels with their specific input, make all “Delete” buttons the same color, all “Next” buttons the same color, If you are using a horizontal scroll (like a row of cards), always show a "peek" of the next card off-screen. This uses the Principle of Closure (or lack thereof) to signal to the user that there is more to see if they swipe. Also please note, aligning items vertically creates a clear “path” for the eye. 

Since we are talking about human perception, this will be a good time to introduce the Von Restorff Effect. While they both approach design from opposite angles, they are two sides of the same coin: Gestalt explains how we group things together, while Von Restorff explains how we notice when something doesn't belong to a group.

**Von Restorff Effect (The Isolation Effect)**: This effect is saying “If all but one item of a list are similar in some dimension, memory for the different item will be enhanced. This is a brainchild of  Hedwig von Restorff posited 1933. In principle it states: “An item that stands out is more likely to be remembered than other items.” Unique or visually distinct elements grab attention and are more memorable. The core takeaway of the Von Restorff Effect is that distinctiveness dictates memory. When a user interacts with an interface, their brain naturally seeks patterns to minimize cognitive effort. While consistency is generally a virtue in design, a perfectly uniform layout can lead to "banner blindness" or habituation, where the user stops noticing details. By strategically breaking a pattern through changes in color, size, shape, or spacing—a designer can "isolate" an element, triggering a biological response that flags the item as high-priority. I understand this is beginning to relate to Fitt’s law, but remember Fitt’s law is more about distance and the size of/to the target.

In practical application, the Isolation Effect is most frequently observed in the design of Calls-to-Action (CTAs). On a page filled with neutral-toned text and standard navigation links, a single button rendered in a vibrant, high-contrast color (like "Emergency Red" or "Primary Brand Blue") leverages the Von Restorff Effect. This visual "hitch" in the user's scan path ensures that the most important action—such as "Buy Now" or "Sign Up"—is the first thing they notice and the last thing they forget. A practical example of this seen below.

https://drive.google.com/file/d/133aVUCo8U_t0WiZT62wz2Mr9D3gbm7yo/view?usp=drive_link
Von Restorff Effect (The Isolation Effect).MOV

Design Takeaway from Von Restorff Effect: So because users notice and remember distinctive elements more than uniform ones, make important buttons, alerts, or messages visually stand out (color, size, shape). Attention is limited, therefore isolate key information instead of blending it with clutter. Because important actions can be overlooked if not prominent, use contrasting colors, bold typography, or animations to guide users. Because visual salience improves recall, critical notifications or CTAs are placed where users are most likely to see them. However, please note as a frontend dev, you have to be careful with over-differentiation. If you have five different buttons all trying to be "unique" with different colors and animations, you create cognitive overload. The Von Restorff Effect only works when there is a clear, consistent pattern to break.

![Knight Capital Incident](images/7.jpg "Knight Capital")

**Gestalt Principles**

**Jackob’s Law**: According Jackob’s law, Users spend most of their time on other sites. This means they prefer your site to work the same way as all the others they already know. For example “Hamburger” menus, top navigation, and search boxes are well-known web features. Users don’t have to think much or wonder what a feature is for. So introducing a different kind of search bar may warrant your user to think about what it's for. 

However, while Jakob’s Law is a cornerstone of UX, I believe it can sometimes stifle innovation. Because this creates a "standardization trap" where we prioritise familiarity over actual efficiency. A perfect example of this is the Pie Menu (or Radial Menu). Leveraging Fitts’s Law, we know that the time to reach a target depends on distance and size. In a Linear Menu, the distance to the last item is much farther than the distance to the first. In a radial Menu, every slice is at an equal distance from the cursor’s starting point. Also, because the slices are wedge-shaped, the "target size" effectively becomes infinite as you move further from the center encouraging faster interaction.

Now, despite being mathematically the most efficient menu type, Radial menus are rarely used in web development because they violate Jakob’s Law. Users are so accustomed to linear lists that introducing a superior radial pattern may feel "broken" or confusing to them. Therefore we are essentially stuck with a less efficient design simply because "that’s how it’s always been done." This reminds of quotes by Rear Admiral Grace M. Hopper, a pioneering American computer scientist. “The most damaging phrase in the language is, ‘we’ve always done it this way.’ By strictly following Jakob’s Law, designers often reach a "local maximum." This means they have the best possible version of a standard design, but they are missing out on a completely different, better design because they refuse to break the mold. 

So according to Jackob’s law:  Navigation menus should be placed where users expect them; logos should be clickable and positioned at the top left; and icons for search, carts, profiles, and settings must be easily recognizable. Ultimately, aligning forms, buttons, and layouts with common conventions reduces cognitive load. However, I enjoy implementing innovative elements by balancing them with the Aesthetic-Usability Effect. Research suggests that users are more tolerant of minor usability hurdles/changes if an interface is visually pleasing and innovative. 

The aesthetic-usability effect is a psychological effect discovered in UX research. It’s a cognitive bias where users perceive more visually appealing designs as easier to use and more effective, even if they are not. Attractive interfaces mask minor usability flaws and foster positive emotions, making users more patient and forgiving. For example, if a new pattern like a Pie Menu is beautifully designed, users are often more willing to develop the new muscle memory required to master it. Taking this further, you can apply your "Aesthetic-Usability" experiments to the core value loop of your app. If your app is about photo editing, you can innovate the editing tools with a Pie Menu, but keep the Save button exactly where they expect it. I will say be conventional where it matters, be innovative where it delights.

**Miller's Law**: This is a brainchild of George A Miller. It’s about “The Magical Number Seven, Plus or Minus Two”. This law basically says the average person can only keep 7 (±2) items in their working memory. Miller emphasised that the brain doesn’t just store raw items — it groups them into chunks. Since the human brain can only hold roughly 7 (±2)   "chunks" of information at once, developers should break long strings of data into smaller units. Instead of 1234567890, use 123-456-7890.Aim for roughly 5 to 9 primary navigation items. If you have more, use categories to group them. This allows the user to memorize the "category" as one chunk rather than individual links. Also, long forms are the enemy of Miller’s Law. If a user sees 30 input fields, their brain treats it as a single, massive, stressful task. Therefore use a Progressive Stepper. By showing only 5–7 fields per page, the user feels a sense of completion at each stage and is less likely to abandon the process. 

Also, when providing results (like on an e-commerce site), don't expect users to compare 50 items at once. Provide robust filters. This allows users to narrow down the "set" of information to a size their brain can actually process and compare.

![Knight Capital Incident](images/8.jpg "Knight Capital")

Image of progressive stepper

From the image above, you can see a progress bar along with a stepper that indicates progress through multiple stages. As the user completes the first page and clicks the “Continue” button, they are directed to the second page, and the progress bar updates to reflect their advancement. This provides the user with a clear sense of forward movement and accomplishment. Breaking the process into multiple steps also helps reduce cognitive overload. If all the information were presented on a single page, users might feel overwhelmed or unsure where to start. By guiding users step by step, the interface becomes more manageable, encouraging completion and improving the overall user experience. Since we are discussing about progressive stepper, this will be a good time to discuss the goal-gradient hypothesis, originally proposed by the behaviorist Clark Hull in 1932. It states that the tendency to approach a goal increases with proximity to the goal. This means users accelerate their engagement as they near task completion. This is effective for progress tracking, gamification, and rewards. The takeaway here is, because users are more motivated near completion, percentages or progress bars should  be used prominently. Because small wins boost engagement, therefore micro-achievements, badges, or confetti can be shown when users are near a goal. Ensure tasks are broken into measurable milestones. For example, an E-learning website may have words like: “You’ve completed 8 of 10 lessons — almost there!”. Fitness apps: “3 km done, 2 km to go” etc. 

But what happens when a goal is not completed? Why do we sometimes feel uncomfortable leaving things unfinished? that discomfort is explained by another psychological principle called the Zeigarnik Effect — the tendency for people to remember and feel tension about incomplete tasks

**Zeigarnik Effect**: The Zeigarnik Effect is a psychological principle stating that people remember unfinished or interrupted tasks better than completed ones. Memory begins with sensory input, which is processed into short-term memory. Unfinished tasks persist in our thoughts, leading to active recall. This ongoing engagement can turn them into long-term memories, enhancing recall until resolved. This increases engagement, encourages task completion, improves retention, and drives conversions.

So because people remember unfinished tasks better than completed ones (Zeigarnik Effect), developers use progress indicators to make users aware that something is incomplete and motivate them to finish it. Break long forms into multi-step processes to encourage completion. display profile completion percentages (e.g., 70% complete) to push users toward 100%. This is the single reason why e-commerce platforms send abandoned cart reminders to bring users back to complete their purchase, apps use streak systems to encourage daily engagement and habit formation. Learning platforms show course completion bars to motivate users to finish modules. Developer use checkmarks, animations, or confirmations when steps are completed. 

https://drive.google.com/file/d/1HxQ-EpYok-lEei2BfjR84qPiW89ziBmf/view?usp=drive_link
@Goal Gradient.MOV

**Tesla’s Law**: This law was proposed by Lawrence Tesla. He was a computer scientist known for his work on human-computer interaction, and he contributed significantly to making software more user-friendly, including work on cut, copy, and paste functionality. This law is otherwise known as the Law of conservation of complexity. The core Idea here is  every process has a certain amount of “inherent complexity" that cannot be removed. You can only decide who handles it: the user or the system. Examples of these inherent complexity can be translating user actions into correct operations behind the scenes, handling unreliable or slow network connections. Connecting with third-party APIs, services, or legacy systems, sorting large datasets quickly or performing complex search operations managing version changes and compatibility issues, managing state, interactions, and animations without confusing the user. All of these can be inherently complex, however it is the job of the developer to deal with the complexity.

As a developer, always try as much as possible to push complexity to the system. For example, instead of making a user type their full address manually, use an Auto-complete API (Google’s Places and Map is best for this). The complexity of finding and validating the address still exists, but the software handles the work for them. A practical example would be, let’s say you are designing a student platform, when designing a student app where users need to enter their university name. A practical approach would be to store an array of all universities in the UK in your codebase (This is the hardpart Tesla hinted). As the user types, they do not need to enter the full name, and their full university name is shown of course relating to what they have typed. For instance, if they intend to type “University of Sheffield,” simply typing “Sheff” should prompt the system to display the full university name, which they can then select.

In Dart, a package like fuzzysearch can be used to implement this kind of intelligent matching. The advantage of this approach is greater than it first appears. It improves data consistency because users often enter the same information in different ways. For example, some users might type “Uni of Sheff,” others “Sheffield University,” and others “Uni of Sheffield,” while all are referring to “University of Sheffield.” This is how messy data is created, and it creates more work for data analysts. Little wonder that data analysts spend up to 70% of their time cleaning data. If developers invest more time in structuring how data is collected to ensure consistency, there would be far less work downstream for analysts. This same logic should be applied in how we collect date, time, and other information. I will strongly advise that apart from people's names and email addresses, developers try to standardize data collected. Use data & Time Pickers, Stepper controls, Input masks, checkboxes, dropdown menu & radio button, toggle switches. etc. The essence of removing complexity from the user is not only to improve usability, but also to ensure that the data collected is standardised, structured, and consistent.

https://drive.google.com/file/d/1Tb8UrVxaLVpPQgJY_BN17w1KHe8wBhLT/view?usp=drive_link
@Tesla.webm

You see as the user tries to search for ‘sheffield’, related text is shown, and the user can select.

**Peak End Rule**: In 1993, four researchers Daniel Kahneman, Barbara Fredrickson, Charles Schreiber, and Donald Redelmeier invited volunteers into a lab for what sounded like a simple experiment. The task was straightforward: place a hand into a container of painfully cold water. In the first round, participants kept their hand in 14°C water for 60 seconds. It was uncomfortable, sharp, and unpleasant but after one minute, it was over. In the second round, they again endured 60 seconds in 14°C water. But this time, they were asked to keep their hand in for an extra 30 seconds. The temperature was raised slightly to 15°C. Still cold. Still unpleasant. Just slightly less intense.

Objectively, the second experience was worse. It lasted longer 90 seconds instead of 60. More total pain. More suffering.

Later, the researchers asked a simple question:

“If you had to repeat one of the trials, which would you choose?” Surprisingly, most participants chose the longer one.

Why would anyone choose more pain?

The researchers realised something profound: people don’t remember experiences by calculating total discomfort. Instead, the mind summarizes the experience using just two key moments — the most intense point (the peak) and the final moment (the end). In both trials, the peak pain was the same: 14°C. But the longer trial ended slightly better, at 15°C. That small improvement at the end reshaped how the entire episode was remembered. The participants’ “experiencing self” suffered more during the longer trial. But their “remembering self” preferred it because it ended on a less painful note. From this, the researchers introduced what became known as the Peak–End Rule: we judge experiences largely by their most intense moment and how they finish, not by how long they last.

Since people largely judge an experience by how it ends, developers focus on designing satisfying confirmation screens and smooth exit interactions. Concentrate less on making every single moment perfect and instead prioritise optimising the peak and final moments. A negative ending can overshadow an otherwise good experience, so carefully avoid frustrating final steps such as unexpected fees or confusing confirmations. Emotional intensity strongly shapes memory, which is why many apps incorporate celebration animations, rewards, or success messages at key moments to leave a lasting positive impression.

https://drive.google.com/file/d/1IKACDppEmYpx-5Y-Ito63N0l39e5Py7K/view?usp=sharing
@PeakEndRule.MOV

**Postel’s Law (The Robustness Principle)**: Proposed by Jon Postel in the 1980s for networking protocols. Principle: “Be conservative in what you send, be liberal in what you accept.” Be strict/clear about the data or actions you output (guidelines, instructions, feedback. Be forgiving of user input errors (allow mistakes, autocorrect, flexible formats). This can also translate to ‘Precision in system communication and Flexibility in human interaction’. Many legacy systems fail because they require a user to type in a very specific format (e.g., MM/DD/YYYY). If the user types 2024-05-01, the system crashes or throws a frustrating error.

**Be Liberal (Input)**: Allow the user to type the date or phone number however they want. Use regex or libraries (like date-fns or libphonenumber) to parse various formats: (555) 123-4567, 5551234567, or 555.123.4567.

**Be Conservative (Output)**: Once the data is in your system, normalize it. When you send it to your database or display it back to the user in a confirmation email, use one single, clear, and standardized format (like ISO 8601: 2024-05-01). 

If a password is incorrect, the message should be direct and helpful, such as, “Incorrect password. Please try again.” Password requirements should also be communicated clearly, for example, stating that a password must contain at least eight characters and one capital letter. This ensures users understand expectations and reduces confusion. Another practical example of this principle can be seen in disappearing menus, especially dropdown or hover-based navigation menus. Many websites use menus that appear when a user hovers over them with a mouse. However, problems occur when the menu disappears the moment the cursor moves slightly outside the menu boundary. If the user accidentally moves the mouse a few inches away while trying to select an option, the menu vanishes instantly, forcing them to start over. This creates frustration and interrupts the user’s flow.

Applying Postel’s principle in this context means designing the menu such that even if the user move few inches away the menu doesn’t disappear. This can be solved by adding extra padding. This aligns perfectly with Postel’s principle:

Be conservative in what you send → The menu remains clearly structured and visually precise.


Be liberal in what you accept → The system tolerates small, natural mouse movements.

Design Takeaway from Postel’s Because users make mistakes or input unexpected data, therefore developers make input fields tolerant (e.g., flexible formats, autocorrect, forgiving validation). Provide clear instructions, tooltips, and feedback messages before submission. Handle errors gracefully instead of crashing or rejecting immediately. Accept variations (like phone numbers with spaces, dashes, or parentheses). 

**Doherty Threshold**: The Doherty Threshold is a principle in human–computer interaction which proposes that systems should respond quickly enough to keep users actively engaged. When response times stay below a certain limit, users remain focused and productive. However, once performance already meets this optimal responsiveness level, making the system even faster or adding extra capability does not significantly enhance satisfaction or efficiency. The idea was introduced by Walter J. Doherty in 1976 in his paper “A Comparison of Programming Systems and Doherty Threshold.” His research showed that maintaining rapid system feedback fast enough to sustain continuous interaction has a stronger impact on productivity than simply increasing system power or features beyond that point. Walter J. Doherty proposes that this should not be greater than 400ms Rule: If the system responds within this window, the user feels in total control. If the response takes longer, the user's attention begins to wander, and their "train of thought" is broken. Don’t be the reason user think their wifi isn’t working

Sometimes a system cannot actually process a request in 400ms. In these cases, developers use "perceived performance" tricks to meet the threshold.  To achieve this speed I must stress on  best practices as a developer, Keep the number of HTML elements low to speed up rendering, Only render visible elements in scrollable lists, Split scripts, defer non-critical code, CSS transforms and opacity changes are faster than layout-triggering properties, Load images, videos, or scripts only when needed and etc.

**Design Takeaways**

**Instant Feedback**: When a user clicks a button, provide a visual change (like a button press animation or a spinner) immediately, even if the background task takes longer.

**Skeleton Screens**: Use placeholder blocks that mimic the layout of the page while data loads. This makes the app feel like it is responding instantly.

**Progressive Loading**: Load text and basic structures first, then "pop in" high-resolution images later.

**Optimistic UI**: When a user hits "Save," don't wait for the server. Update the UI instantly (Doherty) and handle the "messy" data formatting on the backend (Postel).

**Live Inline Validation**: Show a green checkmark or a helpful error message as the user types. This keeps them below the 400ms "thought-break" limit.

**Debouncing**: In search bars, start showing results after a few keystrokes so the user feels the app is "predicting" their needs.


https://drive.google.com/file/d/11Icxd_KJy6xXSO2Ri-SVWeu7alSx6RK7/view?usp=drive_linkSkeleton screen.MOV

An example of skeleton screens

**Serial Position Effect (Primacy and Recency)**: Murdock’s study investigated how the position of a word in a list affects recall, known as the serial position effect. He presented 103 psychology students with lists of 10 to 40 words, one at a time, at either 1 or 2 seconds per word. Participants were divided into six groups, each experiencing a different combination of list length and presentation rate, and were asked to recall as many words as possible in any order.

The results showed that participants were most likely to remember words at the beginning of the list (primacy effect) and at the end of the list (recency effect), while words in the middle were recalled less often. The recency effect persisted even in longer lists, and the middle section of the recall curve formed a flat asymptote.

Murdock explained this using the multi-store model of memory: early words were rehearsed and transferred to long-term memory, last words remained in short-term memory, and middle words were neither sufficiently rehearsed nor retained, leading to poorer recall. The experiment demonstrated that memory performance varies systematically with the position of information in a sequence.

This is the reason why the most important information or actions should never be buried in the middle.

**Design Takeaway**: Put your most critical navigation links (like "Home" or "Dashboard") at the far left or the top of a list. In a pricing table, put the most popular or recommended plan on the Place "Final Actions" (like "Log Out," "Cart," or "Support") at the end of a menu or the far right of a navigation bar. In a long onboarding flow, put the most exciting benefit of the app on the very last slide so the user enters the app feeling motivated. Avoid placing highly important buttons in the middle of a row. If you have a row of 7 buttons, the user is statistically likely to overlook the 4th one.

**Occam’s Razor**: Although formulated in the 14th century by the Franciscan friar William of Ockham, the philosophical principle known as Occam’s Razor remains one of the most vital tools in a designer’s arsenal. At its core, the principle suggests that "among competing explanations, the simplest one is usually the best." In the context of User Experience (UX) and interface design, this translates to a rigorous commitment to simplicity: the most effective design is the one that achieves its purpose with the fewest possible elements.

Please note If two interfaces achieve the same goal, the one with fewer visual elements is superior because it requires less processing power.

The fundamental takeaway for modern designers regarding Occam’s Razor is that complexity is a tax on the user’s cognitive resources. In an era of information density, the designer’s primary role is no longer to provide "more" features, but to curate the most direct path to a solution. 

In practice, this principle dictates a "less is more" approach to structural elements like navigation and data entry. A design takeaway for navigation is the Rule of Five: using 3–5 primary menu items rather than an exhaustive list. This prevents choice paralysis and aligns with human memory constraints. By asking only for essential information, designers respect the user’s time and reduce the likelihood of "form fatigue," which is a leading cause of service abandonment. 

Occam’s Razor teaches us to prefer the simplest solution that works. But why do we so often end up with complex systems in the first place? That tendency is explained by another principle: Parkinson’s Law. Parkinson’s Law states that "work expands to fill the time available for its completion". In design, this means projects often become overly complex or take longer than necessary if given too much time, resulting in inefficient, over-designed, or cluttered interfaces. 

In design, this manifests as Feature Creep. If you give yourself three months to build an app, you will spend three months adding "nice-to-have" animations, extra settings toggles, and niche edge cases that nobody asked for and in reality, what you have added isn’t that important. You just succeeded in adding layers of complexity that might ends up violating some of the laws we spoke about. Occam’s Razor reminds us that the simplest solution is often the most effective. By being aware of Parkinson’s Law and the tendency for work to expand, developers can manage their time intentionally and focus only on what truly matters. Time constraints encourage prioritization, helping teams eliminate unnecessary elements and keep the design clean, simple, and purposeful.

**Conclusion**

Human-centered design is deeply influenced by a set of psychological principles that explain how users perceive, process, and interact with digital systems. Among these, Fitts’s Law establishes that the time required to acquire a target depends on its size and distance. In practice, this means that larger and closer elements are easier and faster to interact with. Designers should therefore make primary call-to-action elements prominent, large, and easily reachable—especially in mobile interfaces where thumb accessibility is critical.

Closely related to decision-making is Hick’s Law, which states that the more choices a user is presented with, the longer it takes to make a decision. Excessive options can overwhelm users and lead to decision fatigue. To address this, designers should simplify interfaces, minimise unnecessary options, and guide users through processes step-by-step rather than presenting everything at once.

Another important cognitive principle is Miller’s Law, which suggests that the average person can hold approximately seven (plus or minus two) items in working memory at a time. This limitation highlights the need to present information in manageable chunks. By breaking content into smaller groups and avoiding information overload, designers can improve comprehension and usability.

User expectations are further shaped by Jakob’s Law, which explains that people spend most of their time on other websites and therefore expect similar patterns across digital products. Instead of reinventing interactions, designers should follow established conventions such as placing logos in the top-left corner, shopping carts in the top-right, and maintaining familiar scrolling behaviours.

The Gestalt Principles provide additional insight into how users visually organise information. The principle of proximity suggests that objects placed close together are perceived as related, so grouping related elements improves clarity. Similarity indicates that elements with consistent colours, shapes, or styles are seen as belonging together, reinforcing visual hierarchy and function. Closure explains that users can perceive incomplete shapes as complete, allowing for minimalistic designs where the brain fills in missing details. Continuity highlights that users naturally follow smooth visual paths, meaning layouts should guide the eye logically through alignment and structure.

Managing complexity is addressed by Tesler’s Law, which asserts that every system has inherent complexity that cannot be eliminated but only managed. Designers must therefore shift complexity away from the user by simplifying interfaces while handling intricate processes behind the scenes.

The Zeigarnik Effect reveals that people remember unfinished tasks better than completed ones, creating a sense of mental tension. This can be leveraged by incorporating progress indicators, checklists, and reminders that encourage users to complete tasks. Similarly, the Peak-End Rule suggests that users judge an experience based on its most intense moment and its conclusion. Designers should therefore create memorable highlights and ensure a smooth, satisfying ending to user journeys.

In terms of system interaction, Postel’s Law advises designers to be flexible in accepting user input while maintaining strict standards for output. This means allowing various input formats while ensuring consistent and reliable system responses. Performance is equally critical, as highlighted by the Doherty Threshold, which states that productivity increases when system response times are under 400 milliseconds. Fast systems enhance engagement and create a sense of ease.

Memory and attention are further explained by the Serial Position Effect, where users tend to remember the first and last items in a sequence more than those in the middle. Designers should therefore position key information or actions at the beginning or end of lists. Simplicity is reinforced by Occam’s Razor, which argues that the simplest solution is often the most effective. Eliminating unnecessary features reduces friction and enhances usability.

The Von Restorff Effect emphasizes that elements which stand out are more likely to be remembered. By using contrast in colour, size, or design, important features such as buttons or alerts can capture user attention. Meanwhile, Parkinson’s Law suggests that tasks expand to fill the time available, indicating the importance of setting constraints such as deadlines or timers to encourage timely action.

Aesthetic considerations also play a crucial role. The Aesthetic-Usability Effect demonstrates that users perceive visually appealing designs as easier to use, even if functionality is unchanged. Investing in clean and attractive interfaces can therefore improve both trust and perceived usability.

Finally, the Goal-Gradient Effect explains that users become more motivated as they approach the completion of a task. By showing progress—such as indicating that a process is “80% complete”—and breaking tasks into stages, designers can encourage users to finish what they have started.

In conclusion, these principles collectively highlight the importance of simplicity, clarity, performance, and user psychology in design. By applying them thoughtfully, designers can create intuitive, efficient, and engaging user experiences that align with both human behaviour and user expectations.

Design video

