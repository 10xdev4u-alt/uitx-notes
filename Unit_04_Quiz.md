---
title: "Unit IV Quiz: Web Scraping and HCI"
id: unit4-quiz
tags:
  - unit-4
  - quiz
  - assessment
  - web-scraping
  - hci
aliases:
  - "Unit 4 Assessment"
links:
  - "[[UITx/Unit_04_Topic_07_How_to_Design_Screens.md|How to Design Screens]]"
---

# Unit IV Quiz: Web Scraping and HCI

> [!note] This quiz is designed to test your understanding of the concepts covered in Unit IV, from the technical practice of Web Scraping to the human-centered principles of HCI.

## Section 1: Quiz Questions (Multiple Choice / Short Answer)

1.  What is the primary purpose of web scraping?
    a) To style web pages
    b) To automatically extract data from websites
    c) To secure websites from attacks
    d) To host websites
2.  Which Python library is commonly used for making HTTP requests to fetch a web page's content?
3.  When scraping a dynamic website where content is loaded by JavaScript, which type of tool is required?
    a) A simple HTTP client like `requests`
    b) A browser automation tool like Selenium or Puppeteer
    c) A database connector
    d) A CSS parser
4.  What is the purpose of a `robots.txt` file?
5.  HCI stands for ______.
6.  Which of the following is NOT one of the five main components of usability?
    a) Learnability
    b) Efficiency
    c) Aesthetics
    d) Satisfaction
7.  The design principle of arranging elements to imply importance and guide the user's eye is known as ______.
8.  What is the core principle of User-Centered Design (UCD)?
9.  A button that looks "pressable" is an example of good ______.
10. What is the "mobile-first" approach in responsive design?

## Section 2: Reasoning Questions

1.  Explain the four main steps of a typical web scraping process.
2.  A developer wants to scrape product prices from an e-commerce site. The prices load only after the page has been open for a few seconds. Why would a simple script using Python's `requests` and `BeautifulSoup` likely fail, and what would be a better approach?
3.  Discuss two major ethical considerations a developer must keep in mind when building a web scraper.
4.  Why is it said that usability is a part of User Experience (UX), but UX is more than just usability? Provide an example.
5.  Describe the iterative nature of the User-Centered Design (UCD) process. Why is iteration important?
6.  Choose two principles of screen design (e.g., Consistency, Feedback, Simplicity) and explain how they contribute to a better user experience.
7.  What is the difference between a low-fidelity prototype (e.g., paper sketch) and a high-fidelity prototype (e.g., interactive mockup)? When would you use each in the design process?
8.  Explain the F-Pattern and Z-Pattern of user scanning. How would this knowledge influence your design of a blog homepage?
9.  Why is it mandatory to perform server-side validation even if you have excellent client-side validation on your forms? (This is a review from Unit 3, but highly relevant to HCI).
10. A company's new software has high efficiency for expert users but very poor learnability for new users. From an HCI perspective, is this a successful design? Justify your answer.

## Section 3: Real-World Cases

1.  **Case: Price Comparison Website**
    A startup wants to build a website that compares the prices of smartphones from 10 different online stores. What technology would be at the core of their data gathering operation, and what is the most important ethical guideline they must follow to avoid disrupting the stores' websites?
2.  **Case: Redesigning a University Portal**
    A university's student portal is cluttered, confusing, and difficult to navigate. Students complain they can't find information about their grades or course schedules. If you were tasked with redesigning it using a User-Centered Design approach, what would be your first step?
3.  **Case: A "Submit" Button**
    A user fills out a long form and clicks a "Submit" button. After clicking, nothing on the screen changes, and the user is unsure if their submission was successful. They click the button several more times. Which core HCI principle has been violated here, and how could it be fixed?
4.  **Case: A Food Delivery App**
    A food delivery app's main screen shows a large, prominent search bar at the top, followed by a grid of images for different food categories (Pizza, Burgers, etc.), and finally a list of popular restaurants. How does this layout use the principle of visual hierarchy?
5.  **Case: Scraping Social Media**
    A researcher wants to scrape 1 million public posts from a social media site for a sentiment analysis project. What are the potential technical and ethical challenges they might face?
6.  **Case: A/B Testing a "Buy Now" Button**
    An e-commerce site wants to see if changing their "Buy Now" button from blue to green will increase sales. What HCI evaluation method would be most appropriate for this, and how does it work?
7.  **Case: Designing a Kiosk for Seniors**
    You are designing a touch-screen kiosk for a community center for senior citizens, many of whom are not tech-savvy. What design principles would be most critical to focus on? (Name at least two).
8.  **Case: A Confusing Icon**
    A new application uses a floppy disk icon to represent "send to cloud." Users are confused. Which design principle does this violate, and why?
9.  **Case: A Python Scraping Script Fails**
    A developer's scraping script, which worked perfectly for months, suddenly stops working and throws an `AttributeError`. What is the most likely cause of this error?
10. **Case: A "Smart" Thermostat**
    A smart thermostat has a beautiful, minimalist interface but hides the manual temperature controls inside a settings menu that is three levels deep. Users complain that it's hard to make a simple temperature change. This is a failure of which HCI concept?

## Section 4: Rapid Fire Questions

1.  What Python library is used for parsing HTML?
2.  What does `response.raise_for_status()` do in the `requests` library?
3.  What is the "U" in UCD?
4.  What are the five components of usability?
5.  What is a fictional user profile created during the design process called?
6.  What is the name for a prototype made with paper and pencil?
7.  What design principle involves grouping related items together?
8.  What does `pip` stand for?
9.  What is the name of the file that tells web crawlers which pages not to access?
10. What is the name for the perceived properties of an object that suggest how it's used?

## Section 5: All Possible 2-Mark Remember Questions

*From Unit IV, Topic 1: What is Web Scraping and Why Do It?*
1.  What is web scraping?
2.  List two common reasons for performing web scraping.
3.  What is the purpose of a `robots.txt` file?
4.  Why is it important to "rate limit" your web scraper?

*From Unit IV, Topic 2: Programming Languages for Web Scraping*
5.  Why is Python the most popular language for web scraping?
6.  Name two key Python libraries used for web scraping and their primary purpose.
7.  When would you need to use a browser automation tool like Selenium or Puppeteer for web scraping?
8.  What is the main advantage of using JavaScript (with Node.js) for web scraping?

*From Unit IV, Topic 3: Python Setup for Web Scraping*
9.  What is `pip` in the context of Python?
10. Why is it considered a best practice to use a virtual environment for Python projects?
11. Which command is used to create a virtual environment named `venv` using Python 3's built-in module?
12. Name two essential Python libraries you would install for a basic web scraping project.

*From Unit IV, Topic 4: Scraping Data from a Website using Python*
13. What is the role of the `requests` library in a Python web scraping script?
14. What is the role of the `BeautifulSoup` library?
15. What is the difference between `find()` and `find_all()` in BeautifulSoup?
16. Why is it important to handle exceptions in a web scraping script?

*From Unit IV, Topic 5: Introduction to Human-Computer Interaction (HCI)*
17. What is Human-Computer Interaction (HCI)?
18. List the five quality components of usability.
19. Briefly differentiate between Usability and User Experience (UX).
20. What is the core principle of User-Centered Design (UCD)?

*From Unit IV, Topic 6: How to Design Systems (HCI Perspective)*
21. What is User-Centered Design (UCD)?
22. List the four main activities in the UCD cycle.
23. What is the purpose of a low-fidelity prototype like a paper sketch?
24. What is the "Think-Aloud Protocol" in usability testing?

*From Unit IV, Topic 7: How to Design Screens (HCI Perspective)*
25. What is visual hierarchy in screen design?
26. Explain the principle of consistency in UI design.
27. What is "affordance" in the context of screen design?
28. What is the "mobile-first" approach in responsive design?

## Answers

### Section 1: Quiz Questions - Answers
1.  **1. b) To automatically extract data from websites** - **Concept:** Web Scraping Definition. **Reason:** Web scraping is fundamentally about the automated extraction of information from web pages.
2.  **2. `requests`** - **Concept:** Python Scraping Libraries. **Reason:** The `requests` library is the standard for making HTTP requests in Python, used to fetch the HTML content of a page.
3.  **3. b) A browser automation tool like Selenium or Puppeteer** - **Concept:** Scraping Dynamic Websites. **Reason:** These tools can control a real browser, execute the necessary JavaScript to load content, and then scrape the final, rendered HTML.
4.  **4. To provide instructions to web crawlers about which parts of a site should not be accessed.** - **Concept:** Scraping Ethics (`robots.txt`). **Reason:** It's a guideline for bots to prevent them from accessing sensitive or irrelevant pages and to manage server load.
5.  **5. Human-Computer Interaction** - **Concept:** HCI Definition. **Reason:** HCI is the study of how people design, implement, and use interactive computer systems.
6.  **6. c) Aesthetics** - **Concept:** Usability Components. **Reason:** While aesthetics contribute to overall User Experience, the five core, measurable components of usability are Learnability, Efficiency, Memorability, Errors, and Satisfaction.
7.  **7. Visual Hierarchy** - **Concept:** Screen Design Principles. **Reason:** Visual hierarchy uses cues like size, color, and placement to guide the user's attention to the most important elements first.
8.  **8. To focus on the users and their needs in each phase of the design process.** - **Concept:** User-Centered Design (UCD). **Reason:** UCD is a design philosophy that prioritizes the user's perspective, goals, and feedback from start to finish.
9.  **9. Affordance** - **Concept:** Screen Design Principles. **Reason:** Affordance is the quality of an object or environment that allows an individual to perform an action. A button that looks pressable has good affordance.
10. **10. A design strategy where you begin designing for the smallest screen (mobile) first and then progressively enhance the design for larger screens.** - **Concept:** Responsive Design. **Reason:** This approach forces prioritization of content and ensures a good experience on resource-constrained devices.

### Section 2: Reasoning Questions - Answers
1.  **1. Explanation:** The four main steps are: 1) **Request:** Send an HTTP request to the target URL to get the page content. 2) **Parse:** Convert the raw HTML into a structured object (like a DOM tree) that can be navigated. 3) **Extract:** Search the parsed structure for the specific data needed, using selectors like tags, classes, or IDs. 4) **Store:** Save the extracted data into a structured format like CSV, JSON, or a database. **Concept:** Web Scraping Process. **Reason:** This systematic process ensures that data is reliably fetched, understood, extracted, and saved for future use.
2.  **2. Explanation:** A simple script would likely fail because `requests` only fetches the initial HTML source code. If the prices are loaded later by JavaScript, they won't be present in that initial HTML. **Concept:** Static vs. Dynamic Scraping. **Reason:** A better approach would be to use a browser automation tool like **Selenium** or **Puppeteer**. These tools control a real browser, which executes the JavaScript, waits for the prices to load, and then allows the script to scrape the final, fully-rendered page content.
3.  **3. Explanation:** Two major ethical considerations are: 1) **Respect `robots.txt`:** This file outlines the site owner's wishes for what bots should and should not access. Ignoring it is disrespectful and can lead to being blocked. 2) **Rate Limiting:** A developer must not send too many requests too quickly, as this can overload the server and negatively impact the service for real users. **Concept:** Scraping Ethics. **Reason:** Responsible scraping is crucial to avoid causing harm to the target website and to prevent legal issues or getting your IP address banned.
4.  **4. Explanation:** Usability focuses on the effectiveness and efficiency of a task (e.g., "Can I easily buy this product?"). User Experience (UX) includes usability but also encompasses the user's entire emotional journey and perception of the product. **Concept:** Usability vs. UX. **Reason:** For example, a checkout process might be usable (you can complete the purchase), but if the design is ugly, the text is stressful, and the confirmation is unclear, the overall UX is poor. UX is about the "how it feels," while usability is about the "can it be done."
5.  **5. Explanation:** The UCD process is iterative because it's a cycle, not a straight line. After evaluating a design with users (Phase 4), the feedback and problems discovered are used to refine the design, leading back to the design phase (Phase 3) or even the requirements phase (Phase 2). **Concept:** User-Centered Design (UCD). **Reason:** Iteration is crucial because it's nearly impossible to create a perfect design on the first try. This cycle of building, testing, and learning ensures that the final product is progressively improved and truly meets user needs.
6.  **6. Explanation:**
    -   **Consistency:** Ensures that similar elements look and behave in the same way. This makes the interface predictable and reduces the user's cognitive load because they don't have to re-learn how things work in different parts of the application.
    -   **Feedback:** Informs the user about the result of their actions. Good feedback (like a success message or a loading indicator) provides reassurance, reduces uncertainty, and makes the user feel in control of the system.
    **Concept:** Screen Design Principles. **Reason:** These principles are rooted in human psychology and help create interfaces that feel intuitive and trustworthy.
7.  **7. Explanation:**
    -   **Low-fidelity prototypes** (paper sketches) are rough, quick, and cheap. They are used early in the design process to explore many different ideas for layout and user flow without committing to a specific direction.
    -   **High-fidelity prototypes** (interactive mockups) look and feel like the final product. They are used later in the process to test fine-grained interactions, visual design, and to get feedback on the near-final user experience.
    **Concept:** Prototyping Fidelity. **Reason:** Starting with lo-fi allows for cheap and easy iteration on core concepts, while hi-fi is for refining the details before development begins.
8.  **8. Explanation:** The **F-Pattern** describes how users read text-heavy pages: two horizontal scans across the top, followed by a vertical scan down the left side. The **Z-Pattern** applies to less dense pages, where the eye moves from top-left to top-right, then diagonally to bottom-left, and finally to bottom-right. **Concept:** Screen Layout Patterns. **Reason:** For a blog homepage, this means placing the most important elements (logo, main navigation, top headline) along the top bar. Key articles or a call-to-action could be placed along the left side to catch the user's eye during the F-pattern scan. The Z-pattern's corners are also prime real estate for important links or buttons.
9.  **9. Explanation:** Client-side validation is a convenience for the user, providing immediate feedback, but it is not a security measure. **Concept:** Client-Side vs. Server-Side Validation. **Reason:** A malicious user can easily bypass all client-side JavaScript validation by disabling JavaScript in their browser or by sending a direct HTTP request to the server. Therefore, the server must *always* re-validate all incoming data to protect against bad data, security vulnerabilities, and to ensure data integrity.
10. **10. Explanation:** From an HCI perspective, this is likely an unsuccessful design, depending on the target audience. **Concept:** Usability Components. **Reason:** While it excels in **efficiency** for experts, its poor **learnability** and **memorability** for new or infrequent users create a frustrating experience. A truly successful design balances all five components of usability. Unless the system is exclusively for a small group of dedicated power users who receive extensive training, the design fails because it is not accessible to a broader audience.

### Section 3: Real-World Cases - Answers
1.  **1. Case: Price Comparison Website**
    *   **Technology:** Web Scraping.
    *   **Ethical Guideline:** The most important guideline is **rate limiting**. They must scrape the sites at a reasonable, slow pace to avoid overwhelming the online stores' servers, which could disrupt service for actual customers and get their scraper's IP address banned.
    **Concept:** Web Scraping Application & Ethics. **Reason:** Aggressive scraping can be mistaken for a denial-of-service attack, so being a "good bot" is crucial for the long-term viability of the service.
2.  **2. Case: Redesigning a University Portal**
    *   **First Step:** The first step in a UCD process would be **Phase 1: Understand and specify the context of use**. This involves conducting user research—interviewing students, observing how they currently use the portal, and sending out surveys to understand their primary goals, pain points, and needs.
    **Concept:** User-Centered Design Process. **Reason:** Before any design or solutioning can happen, you must first develop deep empathy for the users and understand the problems you are actually trying to solve.
3.  **3. Case: A "Submit" Button**
    *   **Principle Violated:** The principle of **Feedback**.
    *   **Fix:** The system should provide immediate and clear feedback. This could be a loading indicator that appears after the click, which is then replaced by a success message (e.g., "Your submission was received!") or a specific error message. This reassures the user that the system has received their action and is processing it.
    **Concept:** HCI Design Principles (Feedback). **Reason:** Lack of feedback leaves the user in a state of uncertainty, leading to frustration and repeated, unnecessary actions.
4.  **4. Case: A Food Delivery App**
    *   **Explanation:** The layout uses size and position to create a clear visual hierarchy. The **search bar** is large and at the top, indicating it's the primary action. The **food category images** are large and visually appealing, drawing the eye next as a primary way to browse. The **list of restaurants** is further down, serving as secondary content for users who want to browse by name.
    **Concept:** Visual Hierarchy. **Reason:** This hierarchy guides the user from the most common action (searching) to other ways of exploring, making the interface intuitive and efficient.
5.  **5. Case: Scraping Social Media**
    *   **Technical Challenges:** The site is likely a dynamic Single Page Application, requiring a browser automation tool (like Selenium/Puppeteer). They will almost certainly have strong anti-scraping measures, including rate limiting, IP blocking, and requiring logins to view content.
    *   **Ethical Challenges:** Even if the posts are public, scraping at this scale may violate the site's Terms of Service. There are also privacy concerns related to collecting and analyzing user-generated content, even if it's public.
    **Concept:** Web Scraping Challenges. **Reason:** Large-scale scraping of major platforms requires sophisticated technical solutions and careful navigation of legal and ethical gray areas.
6.  **6. Case: A/B Testing a "Buy Now" Button**
    *   **Method:** **A/B Testing**.
    *   **How it works:** The website would randomly show 50% of users the blue button (Version A, the control) and the other 50% the green button (Version B, the variation). The system would then track the conversion rate (the percentage of users who click the button and complete a purchase) for each version. By comparing the conversion rates, the site can statistically determine which button color is more effective at driving sales.
    **Concept:** HCI Evaluation Methods. **Reason:** A/B testing is the ideal method for comparing two specific design variations to see which one better achieves a measurable business goal.
7.  **7. Case: Designing a Kiosk for Seniors**
    *   **Critical Principles:**
        1.  **Learnability/Simplicity:** The interface must be extremely simple and intuitive, with large, clear text and buttons. Avoid complex gestures or hidden menus.
        2.  **Feedback:** Provide clear, immediate, and often oversized visual and/or auditory feedback for every touch to confirm that the system has registered the user's action.
    **Concept:** Designing for Specific Audiences. **Reason:** This user group may have less experience with digital interfaces and may have visual or motor impairments, so prioritizing clarity, simplicity, and strong feedback is essential for usability.
8.  **8. Case: A Confusing Icon**
    *   **Principle Violated:** **Consistency**, specifically external consistency.
    *   **Why:** The floppy disk icon is a universally recognized metaphor for "save." Using it for a different action ("send to cloud") violates a deeply ingrained user convention, leading to confusion. The design fights against the user's existing mental model.
    **Concept:** HCI Design Principles (Consistency). **Reason:** Leveraging established conventions makes an interface instantly more intuitive.
9.  **9. Case: A Python Scraping Script Fails**
    *   **Most Likely Cause:** The website's HTML structure has changed.
    *   **Explanation:** An `AttributeError` typically occurs in this context when the script tries to access a property on a `None` object. This happens when `BeautifulSoup.find()` fails to find an element (e.g., because a class name was changed from `class="price"` to `class="product-price"`) and returns `None`. The subsequent attempt to access `.text` on this `None` object then throws the error.
    **Concept:** Web Scraping Maintenance. **Reason:** Scrapers are brittle and break easily when the target website's layout is updated.
10. **10. Case: A "Smart" Thermostat**
    *   **Concept Violated:** This is a failure of **Usability**, specifically efficiency and learnability.
    *   **Explanation:** While the design might be aesthetically pleasing (good UX in one sense), it fails a basic usability test. The primary function of a thermostat—changing the temperature—is made difficult and inefficient. The design prioritizes a minimalist aesthetic over the user's primary goal, violating a key HCI principle that systems should be designed to help users achieve their goals efficiently.
    **Concept:** Usability vs. Aesthetics. **Reason:** Good HCI is not just about how something looks, but how it works. An elegant design that is difficult to use is ultimately a poor design.

### Section 4: Rapid Fire Questions - Answers
1.  **1. What does the `<aside>` tag represent?** Content that is indirectly related to the main content, often in a sidebar.
2.  **2. Which input type provides a color picker?** `type="color"`.
3.  **3. What attribute on a `<video>` tag shows a static image before playback?** The `poster` attribute.
4.  **4. What JavaScript method is used to get the 2D drawing context of a canvas?** `getContext('2d')`.
5.  **5. What must you set on an element to make it draggable?** The `draggable="true"` attribute.
6.  **6. Which Web Storage object is cleared when the browser tab is closed?** `sessionStorage`.
7.  **7. What CSS property creates rounded corners?** `border-radius`.
8.  **8. What is the `transition-timing-function` value for a constant speed?** `linear`.
9.  **9. What `animation-iteration-count` value creates an endless loop?** `infinite`.
10. **10. Which transform function moves an element?** `translate()` (or `translateX()`, `translateY()`).

### Section 5: All Possible 2-Mark Remember Questions - Answers
1.  **1. What is web scraping?** - **Concept:** Web Scraping Definition. **Reason:** Web scraping is the automated process of extracting data from websites. It involves fetching the HTML content of a page and then parsing it to extract specific information into a structured format.
2.  **2. List two common reasons for performing web scraping.** - **Concept:** Web Scraping Applications. **Reason:** Market research (e.g., price monitoring) and data collection for academic research or machine learning.
3.  **3. What is the purpose of a `robots.txt` file?** - **Concept:** Scraping Ethics. **Reason:** A `robots.txt` file is a set of instructions for web crawlers (bots) that indicates which parts of a website should not be accessed or scraped.
4.  **4. Why is it important to "rate limit" your web scraper?** - **Concept:** Scraping Ethics. **Reason:** To avoid overwhelming a website's server with too many requests in a short period, which could slow down or crash the site for other users. It is a core principle of responsible scraping.
5.  **5. Why is Python the most popular language for web scraping?** - **Concept:** Scraping Languages. **Reason:** Python is popular due to its simple syntax, extensive ecosystem of powerful scraping libraries (like Beautiful Soup and Scrapy), and strong data processing capabilities.
6.  **6. Name two key Python libraries used for web scraping and their primary purpose.** - **Concept:** Python Libraries. **Reason:** **Requests** for making HTTP requests to fetch web pages, and **Beautiful Soup** for parsing the HTML content to extract data.
7.  **7. When would you need to use a browser automation tool like Selenium or Puppeteer for web scraping?** - **Concept:** Dynamic Scraping. **Reason:** When scraping dynamic websites (Single Page Applications) where the content is loaded or rendered using JavaScript after the initial page load.
8.  **8. What is the main advantage of using JavaScript (with Node.js) for web scraping?** - **Concept:** Scraping Languages. **Reason:** Its main advantage is its native ability to handle and execute the JavaScript on dynamic websites, making it highly effective for scraping modern web applications, often using tools like Puppeteer.
9.  **9. What is `pip` in the context of Python?** - **Concept:** Python Environment. **Reason:** `pip` is the standard package manager for Python, used to install and manage third-party libraries and dependencies.
10. **10. Why is it considered a best practice to use a virtual environment for Python projects?** - **Concept:** Python Environment. **Reason:** To create an isolated environment for each project, preventing dependency conflicts between projects and keeping the global Python installation clean.
11. **11. Which command is used to create a virtual environment named `venv` using Python 3's built-in module?** - **Concept:** Python Environment. **Reason:** `python3 -m venv venv`.
12. **12. Name two essential Python libraries you would install for a basic web scraping project.** - **Concept:** Python Libraries. **Reason:** `requests` (for making HTTP requests) and `beautifulsoup4` (for parsing HTML).
13. **13. What is the role of the `requests` library in a Python web scraping script?** - **Concept:** Scraping Process. **Reason:** The `requests` library is used to send HTTP requests (typically GET requests) to a URL to fetch the raw HTML content of the web page.
14. **14. What is the role of the `BeautifulSoup` library?** - **Concept:** Scraping Process. **Reason:** `BeautifulSoup` is used to parse the raw HTML content fetched by `requests`. It creates a parse tree that allows for easy navigation and extraction of data from the HTML structure.
15. **15. What is the difference between `find()` and `find_all()` in BeautifulSoup?** - **Concept:** BeautifulSoup Methods. **Reason:** `find()` returns only the first element that matches a given criteria, while `find_all()` returns a list of all elements that match the criteria.
16. **16. Why is it important to handle exceptions in a web scraping script?** - **Concept:** Robust Scraping. **Reason:** To make the script robust against issues like network errors (e.g., the website is down), HTTP errors (e.g., page not found), or changes in the website's HTML structure that could cause parsing errors.
17. **17. What is Human-Computer Interaction (HCI)?** - **Concept:** HCI Definition. **Reason:** HCI is a multidisciplinary field that studies the design and use of computer technology, focusing on the interaction between humans (users) and computers to create usable, useful, and enjoyable systems.
18. **18. List the five quality components of usability.** - **Concept:** Usability. **Reason:** Learnability, Efficiency, Memorability, Errors, and Satisfaction.
19. **19. Briefly differentiate between Usability and User Experience (UX).** - **Concept:** Usability vs. UX. **Reason:** Usability is a component of UX and focuses on whether a user can accomplish a goal effectively. UX is a broader concept that includes the user's overall feelings, perceptions, and satisfaction with the entire experience.
20. **20. What is the core principle of User-Centered Design (UCD)?** - **Concept:** UCD. **Reason:** The core principle of UCD is to involve users throughout the design process, focusing on their needs, goals, and feedback in every phase.
21. **21. What is User-Centered Design (UCD)?** - **Concept:** UCD Definition. **Reason:** UCD is an iterative design process that focuses on the users and their needs in each phase of the design, from understanding context to evaluation.
22. **22. List the four main activities in the UCD cycle.** - **Concept:** UCD Process. **Reason:** 1. Understand context, 2. Specify requirements, 3. Produce design solutions, 4. Evaluate the design.
23. **23. What is the purpose of a low-fidelity prototype like a paper sketch?** - **Concept:** Prototyping. **Reason:** To quickly and cheaply explore different design concepts, layouts, and user flows without getting invested in visual details early in the process.
24. **24. What is the "Think-Aloud Protocol" in usability testing?** - **Concept:** Usability Testing. **Reason:** It is a method where users are asked to verbalize their thoughts, feelings, and opinions as they interact with a system, providing deep insights into their mental processes and potential usability issues.
25. **25. What is visual hierarchy in screen design?** - **Concept:** Screen Design. **Reason:** Visual hierarchy is the arrangement of elements to imply importance, guiding the user's eye to the most critical information first using cues like size, color, and position.
26. **26. Explain the principle of consistency in UI design.** - **Concept:** Design Principles. **Reason:** Consistency means that similar elements should look and behave in similar ways, making the interface predictable and easier for users to learn.
27. **27. What is "affordance" in the context of screen design?** - **Concept:** Design Principles. **Reason:** Affordance refers to the perceived properties of an interface element that suggest how it should be used (e.g., a button that looks "pressable").
28. **28. What is the "mobile-first" approach in responsive design?** - **Concept:** Responsive Design. **Reason:** It is a design strategy where you begin by designing for the smallest screen size (mobile) first, which forces prioritization of content, and then progressively enhance the design for larger screens.
