---
title: "Unit IV: How to Design Systems (HCI Perspective)"
id: unit4-topic6-designing-systems
tags:
  - unit-4
  - hci
  - system-design
  - user-centered-design
  - design-process
aliases:
  - "System Design in HCI"
links:
  - "[[UITx/Unit_04_Topic_05_Intro_to_Human_Computer_Interaction.md|Introduction to Human-Computer Interaction]]"
  - "[[UITx/Unit_04_Topic_07_How_to_Design_Screens.md|How to Design Screens]]"
---

# Unit IV, Topic 6: How to Design Systems (HCI Perspective)

> [!quote] Designing a system is not merely an act of technical implementation; it is an act of empathy. To design a great system, we must first understand the people who will use it, the context they are in, and the goals they wish to achieve. This human-centered approach ensures that what we build is not only functional but also truly useful and usable.

## 1. The User-Centered Design (UCD) Process

Designing effective systems from an HCI perspective means adopting a **User-Centered Design (UCD)** process. UCD is an iterative design philosophy that places the user at the center of every stage. It's not a rigid set of steps but a cyclical process of understanding, designing, and evaluating.

The typical UCD cycle involves four main activities:

1.  **Understand and specify the context of use:** Who are the users? What are their goals? In what environment will they use the system?
2.  **Specify the user requirements:** What must the system do to meet the users' goals?
3.  **Produce design solutions:** Create design concepts, from low-fidelity sketches to high-fidelity prototypes.
4.  **Evaluate the design:** Test the design solutions with real users to see if they meet the requirements.

```
+-------------------------------------------------+
|                                                 |
|   +-----------------------------------------+   |
|   | 1. Understand Context (Research)        |   |
|   +-----------------------------------------+   |
|                       |                         |
|                       v                         |
|   +-----------------------------------------+   |
|   | 2. Specify Requirements (Analysis)      |   |
|   +-----------------------------------------+   |
|                       |                         |
|                       v                         |
|   +-----------------------------------------+   |
|   | 3. Produce Design Solutions (Design)    |   |
|   +-----------------------------------------+   |
|                       |                         |
|                       v                         |
|   +-----------------------------------------+   |
|   | 4. Evaluate Design (Testing)            |   |
|   +-----------------------------------------+   |
|                       |                         |
|                       +-------<--[Iterate]--<----+
|                                                 |
+-------------------------------------------------+
```

## 2. Phase 1: Understanding the User and Context

This is the research phase. The goal is to gain deep empathy for the users.

### Key Activities:
-   **User Interviews:** Conducting one-on-one interviews to understand users' needs, motivations, and pain points.
-   **Surveys and Questionnaires:** Gathering quantitative data from a larger user base.
-   **Observation (Contextual Inquiry):** Observing users in their natural environment to see how they currently perform tasks.
-   **Persona Development:** Creating fictional character profiles that represent your target user groups. A persona typically includes a name, photo, demographics, goals, and frustrations.
-   **Scenario and Storyboard Creation:** Writing short stories or creating visual storyboards that describe how a persona might interact with the system to achieve a goal.

## 3. Phase 2: Specifying Requirements

Based on the research, you define what the system must do to be successful.

### Key Activities:
-   **Functional Requirements:** What the system should *do* (e.g., "The system must allow users to search for products").
-   **Non-Functional Requirements:** The qualities of the system (e.g., "The search results must load in under 2 seconds").
-   **Usability Goals:** Defining specific, measurable usability targets (e.g., "A new user should be able to complete a purchase in under 3 minutes with a 95% success rate").
-   **User Journey Mapping:** Visualizing the end-to-end experience a user has with the system to identify key touchpoints and opportunities for improvement.

## 4. Phase 3: Producing Design Solutions (Ideation and Prototyping)

This is the creative phase where you generate ideas and build representations of the design. It's important to start with low-fidelity designs and gradually increase fidelity as you gather feedback.

### Levels of Fidelity:
-   **Low-Fidelity Prototypes (Lo-Fi):**
    -   **What:** Paper sketches, wireframes, storyboards.
    -   **Purpose:** To quickly explore different concepts, layouts, and information architecture without getting bogged down in visual details. They are cheap and fast to create and discard.
-   **Medium-Fidelity Prototypes (Mid-Fi):**
    -   **What:** Digital wireframes created with tools like Balsamiq or Figma, often with basic interactivity (clickable prototypes).
    -   **Purpose:** To test the user flow and interaction model in more detail.
-   **High-Fidelity Prototypes (Hi-Fi):**
    -   **What:** Visually detailed mockups created with tools like Figma, Sketch, or Adobe XD that look and feel very close to the final product.
    -   **Purpose:** To test the visual design, branding, and fine-grained interactions.

## 5. Phase 4: Evaluating the Design (Testing)

Evaluation is about testing your design solutions with real users to see what works and what doesn't. The feedback from this phase informs the next iteration of the design.

### Key Evaluation Methods:
-   **Usability Testing:** The cornerstone of evaluation. Observers watch a representative user attempt to complete tasks with a prototype. The goal is to identify usability problems.
    -   **Think-Aloud Protocol:** Users are encouraged to speak their thoughts aloud as they work through the tasks.
-   **Heuristic Evaluation:** A group of usability experts evaluates the interface against a set of recognized usability principles (the "heuristics," such as Nielsen's 10 Usability Heuristics).
-   **A/B Testing:** A method of comparing two versions of a web page or app against each other to determine which one performs better.
-   **Surveys:** Collecting user satisfaction data after a usability test or after product launch.

## 6. Exam-Oriented Insights

The UCD process is a fundamental concept in HCI.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is User-Centered Design (UCD)?**
>     *Answer:* UCD is an iterative design process that focuses on the users and their needs in each phase of the design, from understanding context to evaluation.
> 2.  **List the four main activities in the UCD cycle.**
>     *Answer:* 1. Understand context, 2. Specify requirements, 3. Produce design solutions, 4. Evaluate the design.
> 3.  **What is the purpose of a low-fidelity prototype like a paper sketch?**
>     *Answer:* To quickly and cheaply explore different design concepts, layouts, and user flows without getting invested in visual details early in the process.
> 4.  **What is the "Think-Aloud Protocol" in usability testing?**
>     *Answer:* It is a method where users are asked to verbalize their thoughts, feelings, and opinions as they interact with a system, providing deep insights into their mental processes and potential usability issues.

> [!tip] **For Higher Mark Questions:**
> Be prepared to describe the entire User-Centered Design process in detail, explaining the key activities and outputs of each phase. Discuss the importance of iteration in the UCD cycle. Compare and contrast different evaluation methods, such as usability testing and heuristic evaluation, explaining the pros and cons of each.
