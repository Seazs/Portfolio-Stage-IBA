---
title: Description of the work flow
draft: 
tags:
---
Since I was working on a project separate from the medical product, I wasn’t directly included in the main product’s workflow.

I will therefore describe my workflow with Adrien and Valentin, as well as the product’s workflow. While I wasn’t directly involved in the latter, my understanding is based on an external perspective.


# My workflow

Since I was the only one working on my project, we didn’t have a complex system for tracking tasks or assigning them, as all tasks were handled solely by me.

Still, each week, we held a three-person meeting with Adrien and Valentin to discuss progress, challenges, solutions, and the tasks I needed to complete.

I took notes from each meeting in a shared OneNote notebook. This gave us an updated list of tasks after each meeting, along with records of all discussions. I then organized these tasks in Microsoft To-Do, which allowed me to sort and mark off completed tasks more easily. This list was also shared with my two colleagues so they could track my progress at any time.

In the shared OneNote, we also documented our reflections and questions, particularly with Adrien, who was closely involved. We kept notes on technical aspects and the various solutions we had tested or planned to test. This approach enabled us to create comparison tables for the different solutions we considered. 


For **version control** (using GitFlow), managing branches wasn’t too complex since I was essentially working alone. At the start, while the application was still in its early stages, I worked directly on the main branch.

Once the project reached a more advanced stage, I began systematically creating separate branches for implementing features individually. This allowed me to avoid the risk of breaking existing functionality and to easily revert to a stable version if necessary. Merging back into the main branch was usually straightforward, as there were no concurrent changes to reconcile.

Toward the end of the project, Valentin and Adrien created branches to fix minor bugs and add some additional features. They then submitted merge requests so I could review and approve their changes before integrating them into the main branch. After making a few adjustments to their changes, I merged their branches.

--- 

This approach was sufficient for the project’s size and the number of people involved. More complex workflows would have been unnecessary and would have slowed down the work.

# Main Product workflow

The main product workflow respect the following V cycle.


![[cycleVIba.png]]

This diagram shows the V-Model workflow used in software development at IBA. The V-Model is a systems engineering approach that integrates both the development (left side of the "V") and testing (right side of the "V") phases. In this model, each stage on the left corresponds to a verification stage on the right, ensuring that each requirement and component has a dedicated validation phase. Here’s a breakdown of each component in this specific workflow:

### Left Side (Development and Design Stages)

1. **Stakeholder Requirements**: The initial phase involves gathering high-level requirements directly from stakeholders. These represent what the end users and other stakeholders expect from the system.
    
2. **PEMS: System Requirement Specification**: In this phase, the PEMS team specifies system-level requirements, breaking down the stakeholder requirements into more detailed system needs.
    
3. **PEMS: System Architecture**: The system architecture for PEMS is defined, outlining the overall structure and major components of the system.
    
4. **PESS Requirements**: PESS requirements are outlined here, focusing on specific needs that the PESS part of the project must fulfill.
    
5. **PESS Architecture**: The architecture for PESS is designed based on the PESS requirements, providing a more detailed structural and functional breakdown for this component.
    
6. **Software Requirement**: This step involves defining the requirements specifically for the software component, detailing what the software must accomplish to support the broader PEMS and PESS systems.
    
7. **Software Architecture**: Here, the architecture for the software is developed, structuring the software components and defining their interactions.
    
8. **Component Requirements**: Requirements are set at a finer, component level, specifying functionalities for individual software or hardware components.
    
9. **Implementation**: This is the stage where actual coding or development of components occurs, bringing all previous designs and requirements into a functional form.
    

### Right Side (Verification and Validation Stages)

In the V-Model, each development phase on the left side has a corresponding verification phase on the right. The individuals responsible for defining requirements or architecture are also involved in verifying them, ensuring consistency and correctness.

1. **Component Test**: Individual components are tested to ensure they meet the specific requirements defined in the "Component Requirements" phase.
    
2. **Software Integration Test**: The software components are integrated and tested as a whole, verifying interactions between modules and ensuring they function together according to the "Software Architecture."
    
3. **Software System Test**: This test checks the entire software system against the "Software Requirement" to confirm that it performs all specified functions correctly.
    
4. **PESS Integration Test**: This test validates the integrated components of the PESS system, ensuring they work together as intended based on the "PESS Architecture."
    
5. **PESS System Test**: Here, the PESS system is tested as a whole to verify that it meets all the defined "PESS Requirements."
    
6. **PEMS Integration Test**: The PEMS components are integrated and tested to ensure they operate correctly as a combined unit according to the "PEMS: System Architecture."
    
7. **PEMS System Test**: This test checks the entire PEMS system against the "PEMS: System Requirement Specification" to verify that it meets all system-level requirements.
    
8. **PEMS Validation**: The final step validates the system against the initial "Stakeholder Requirements" to confirm that the developed product satisfies all end-user and stakeholder expectations.
    

### Summary

In this V-Model workflow at IBA, the responsibility for verification lies with the team or individuals who initially specified the requirements or designed the components. This ensures that those who defined the requirements also confirm their implementation, maintaining accountability and alignment with the original objectives.

--- 

My team is at the lowest level, Software architecture and below. 

To track all the task, IBA uses JIRA. JIRA is a project management and issue-tracking software developed by Atlassian, widely used by teams to plan, track, and manage software development projects. It enables users to create, organize, and prioritize tasks, bugs, and feature requests. With customizable workflows, JIRA supports Agile methodologies like Scrum and Kanban, making it especially popular among software development teams to streamline collaboration and improve project visibility.

It also allow to connect task directly to Gitlab by linking a Jira task to a merge request for exemple or to a specific branch to track the evolution. This is very convenient and i used this once when i worked on my supervisors project.

